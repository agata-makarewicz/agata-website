---
layout: default
---

<section class="latest-posts">
    <div class="wrapper">
    {% for post in site.posts %}
        <div class="post">
            <div class="post__metadata">
                <span class="gray">{{ post.date | date: 
            '%d.%m.%Y' }}</span>&nbsp;<span class="gray-50">/</span>&nbsp;
                <ul class="post__categories">
                    {% for category in post.categories %}
                        <li><a href="">{{ category }}</a></li>
                    {% endfor %}
                </ul>
            </div>
            {% include post-thumbnail.html image=post.featured-image alt=post.featured-image-alt %}
            <div class="post__summary">

                <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>

                <div class="post__excerpt">    
                {{ post.excerpt }}
                </div>
            
            <a class="post__read-more" href="{{ post.url }}">
                Czytaj dalej ›
            </a>

            </div>
        </div>
    {% endfor %}
    </div>
</section>
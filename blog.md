---
layout: default
---

<section class="latest-posts">
    <div class="wrapper">
    {% for post in site.posts | limit: 3 %}
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
            <div class="post__thumbnail"></div>
            <div class="post__summary">

                <h3 class="navy"><a href="{{ post.url }}">{{ post.title }}</a></h3>

                {{ post.excerpt }}

            </div>

            <a class="post__read-more" href="{{ post.url }}">
                Czytaj dalej ›
            </a>
        </div>
    {% endfor %}
    </div>
</section>
---
layout: default
---


<header class="homepage-header">
    <div class="wrapper">
        <div class="hero">
            <div class="hero__text">
                <h1>Miło Cię widzieć</h1>
                <p>Poniżej znajdziesz moje opowieści o drobnych radościach, a także codziennych zmaganiach z dorosłością, własną głową oraz rzeczami, które mnie poruszają.</p>
            </div>
            <img class="hero__image" src="../assets/images/agata.jpg" alt="">
        </div>
    </div>    
</header>

<section class="latest-posts">
    <div class="wrapper">
    {% for post in site.posts | limit: 3 %}
        <div class="post">
            {% include post-metadata.html %}
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

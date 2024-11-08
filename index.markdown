---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<section class="hero is-primary">
    <div class="hero-body">
        <p class="title">Bienvenue sur mon blog</p>
    </div>
</section>

<div class="columns is-multiline mt-6">
    {% for post in site.posts %}
    <div class="column is-one-third">
        <div class="card">
            <div class="card-content">
                <p class="title is-4">{{ post.title }}</p>
                <p class="subtitle is-6">{{ post.date | date: "%d/%m/%Y" }}</p>
                <div class="content">
                    {{ post.excerpt }}
                    <a href="{{ post.url | relative_url }}">Lire la suite...</a>
                </div>
            </div>
        </div>
    </div>
    {% endfor %}
</div>
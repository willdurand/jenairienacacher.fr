---
layout: index
---

# Je n'ai rien à cacher. <small>En fait si, et vous également !</small>

---

{% for headline in site.data.headlines %}
## <i class="glyphicon glyphicon-hand-right" aria-hidden="true"></i> {{ headline.title }}

{{ headline.content|markdownify }}
{% endfor %}


## <i class="glyphicon glyphicon-hand-right" aria-hidden="true"></i> Aller plus loin

Vous trouverez ci-dessous un ensemble de ressources variées sur le sujet pour
mieux comprendre les enjeux et implications.

### En lisant des articles

{% for article in site.data.articles %}
    {% include article_item.html article=article %}
{% endfor %}

### En écoutant des conférences

<ul class="media-list">
{% for video in site.data.videos %}
    {% include video_item.html video=video %}
{% endfor %}
</ul>

### En lisant des livres

{% for book in site.data.books %}
#### • {{ book.title }} - <em>{{ book.authors|join:', ' }}</em>

{% if book.abstract %}{{ book.abstract|markdownify }}{% endif %}
{% endfor %}


## <i class="glyphicon glyphicon-hand-right" aria-hidden="true"></i> Se tenir informé

<center>
    <a href="https://www.laquadrature.net/fr/">
        <img src="/images/logo_laquadrature-net_horiz_moyen.png" class="img-responsive">
    </a>
</center>

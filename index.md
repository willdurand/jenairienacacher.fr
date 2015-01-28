---
layout: index
---

{% for headline in site.data.headlines %}
## <i class="glyphicon glyphicon-hand-right" aria-hidden="true"></i> {{ headline.title }}

{{ headline.content|markdownify }}
{% endfor %}

## <i class="glyphicon glyphicon-hand-right" aria-hidden="true"></i> Mais enfin, ...

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})
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
#### • {{ book.title }} - _{{ book.authors|join:', ' }}_

{% if book.abstract %}{{ book.abstract|markdownify }}{% endif %}
{% endfor %}


## <i class="glyphicon glyphicon-hand-right" aria-hidden="true"></i> Se tenir informé

<ul class="centered-list">
{% for source in site.data.sources %}
    <li>
        <a href="{{ source.url }}">
            <img src="/images/{{ source.image }}" class="img-responsive">
        </a>
    </li>
{% endfor %}
</ul>

## Autres sources

{% for source in site.data.autres-sources %}
#### • {% if source.url %}[{{ source.title }}]({{ source.url }}){% else %}{{ source.title }}{% endif %} - _{{ source.authors|join:', ' }}_ {% if source.language %}(en {{ source.language }}){% endif %}
{% endfor %}

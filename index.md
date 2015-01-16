---
layout: index
---

# Je n'ai rien à cacher. <small>En fait si, et vous également !</small>

---

{% for question in site.data.questions %}
## <i class="glyphicon glyphicon-hand-right" aria-hidden="true"></i> {{ question.question }}

{{ question.answer|markdownify }}
{% endfor %}


## <i class="glyphicon glyphicon-hand-right" aria-hidden="true"></i> Aller plus loin

Vous trouverez ci-dessous un ensemble de ressources variées sur le sujet pour
mieux comprendre les enjeux et implications.

### En lisant des articles

{% for article in site.data.articles %}
#### <a href="{{ article.url }}">{{ article.title }}</a> - <em>{{ article.authors|join:', ' }}</em>
{% endfor %}

### En écoutant des conférences

<ul class="media-list">
{% for video in site.data.videos %}
    {% include video_item.html video=video %}
{% endfor %}
</ul>

### En lisant des livres

{% for book in site.data.books %}
#### {{ book.title }} - <em>{{ book.authors|join:', ' }}</em>

{{ book.abstract }}
{% endfor %}


## <i class="glyphicon glyphicon-hand-right" aria-hidden="true"></i> Se tenir informé

### En suivant les gens qui se battent pour vous



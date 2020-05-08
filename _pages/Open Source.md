---
layout: page
title: Public Repositories
---

<ul>
    {% for repo in site.github.public_repositories %}
        <li>
            <p>
                <a href="{{ repo.html_url }}">{{ repo.name }}</a>
                {% if repo.homepage %}<a href="{{ repo.homepage }}" target="_blank">↗</a>{% endif %}
                {{ repo.description }}
                <br>
                <small><b>{{ repo.language }}</b> Updated on {{ repo.updated_at | date: "%b %d, %Y" }}</small>
            </p>
        </li>
    {% endfor %}
</ul>

Organization Members
--------------------

<ol>
    {% for contributor in site.github.organization_members %}
        <li>
            <a href="{{ contributor.html_url }}">{{ contributor.login }}</a>
        </li>
    {% endfor %}
</ol>

<div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
    <ol class="carousel-indicators">
        {% assign i = 0 %}
        {% for contributor in site.github.organization_members %}
        <li data-target="#carouselExampleCaptions" data-slide-to="{{ i }}" class="{% if contributor.login == "suvozit" %}active{% endif %}"></li>
        {% assign i = i | plus: 1 %}
        {% endfor %}
    </ol>
    <div class="carousel-inner">
        {% for contributor in site.github.organization_members %}
        <div class="carousel-item {% if contributor.login == "suvozit" %}active{% endif %}">
            <img src="{{ contributor.avatar_url }}" class="d-block w-100" alt="...">
            <div class="carousel-caption d-none d-md-block">
                <p><a href="{{ contributor.html_url }}">{{ contributor.login }}</a></p>
            </div>
        </div>
        {% endfor %}
    </div>
    <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
    </a>
</div>

Build Revision: [{{ site.github.build_revision | truncate: 7, "" }}](./site.github.json)

```
  Build Info:
  - Build time: {{ site.time | date_to_rfc822 }}
  - Unix build time: {{ site.time | date:"%s" }}
```

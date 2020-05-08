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

<div id="carousel-example-generic" class="carousel slide" data-ride="carousel">
    <!-- Indicators -->
    <ol class="carousel-indicators">
        <li data-target="#carousel-example-generic" data-slide-to="0" class="active"></li>
        <li data-target="#carousel-example-generic" data-slide-to="1"></li>
        <li data-target="#carousel-example-generic" data-slide-to="2"></li>
        
        {% assign i = 0 %}
        {% for contributor in site.github.organization_members %}
        <li data-target="#carousel-example-generic" data-slide-to="{{ i }}" class="{% if contributor.login == "suvozit" %}active{% endif %}"></li>
        {% assign i = i | plus: 1 %}
        {% endfor %}
    </ol>
    
    <!-- Wrapper for slides -->
    <div class="carousel-inner" role="listbox">
        {% for contributor in site.github.organization_members %}
        <div class="item {% if contributor.login == "suvozit" %}active{% endif %}">
          <img src="{{ contributor.avatar_url }}" alt="{{ contributor.login }}">
          <div class="carousel-caption">
            <a href="{{ contributor.html_url }}">{{ contributor.login }}</a>
          </div>
        </div>
        {% endfor %}
    </div>

    <!-- Controls -->
    <a class="left carousel-control" href="#carousel-example-generic" role="button" data-slide="prev">
        <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
    </a>
    <a class="right carousel-control" href="#carousel-example-generic" role="button" data-slide="next">
        <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
    </a>
</div>


<ol>
    {% for contributor in site.github.organization_members %}
        <li>
            <a href="{{ contributor.html_url }}">{{ contributor.login }}</a>
        </li>
    {% endfor %}
</ol>

Build Revision: [{{ site.github.build_revision | truncate: 7, "" }}](./site.github.json)

```
  Build Info:
  - Build time: {{ site.time | date_to_rfc822 }}
  - Unix build time: {{ site.time | date:"%s" }}
```

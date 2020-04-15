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

Build Revision: [{{ site.github.build_revision | truncate: 7, "" }}](./site.github.json)

```
  Build Info:
  - Build time: {{ site.time | date_to_rfc822 }}
  - Unix build time: {{ site.time | date:"%s" }}
```

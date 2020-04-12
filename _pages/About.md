---
layout: page
title: About
---

A [Bootstrap](http://getbootstrap.com) responsive two-column [Jekyll](http://jekyllrb.com) documentation theme that pairs a prominent navbar with uncomplicated content.


### Built on Jekyll

* Complete Jekyll setup included 
	- Layouts
	- Custom Configs
	- [Example pages]({{ site.baseurl }}/Example)
	- [404]({{ site.baseurl }}/404)
	- [Sitemap]({{ site.baseurl }}/sitemap.xml)
	- [robots.txt]({{ site.baseurl }}/robots.txt)
	- [feed.xml]({{ site.baseurl }}/feed.xml)
	- [GitHub Data API]({{ site.baseurl }}/site.github.json)
* Mobile friendly design and development
* Easily scalable text and component sizing with `rem` units in the CSS
* Support for a wide gamut of HTML elements
* Syntax highlighting, courtesy Pygments (the Python-based code snippet highlighter)
* Sidebar includes support for textual modules and a dynamically generated navigation with active link support

[Head to the readme](https://github.com/{{ site.github.username }}{{ site.baseurl }}#readme) to learn more.


### Features

In addition to the features of Jekyll, Minima adds the following:

* Sidebar includes support for textual modules and a dynamically generated navigation with active link support
* Optional color schemes, available via `_config.yml#L17` and default is `DA2E75`
* Two orientations for sidebar, `Default` (alphabetical order) and [`Custom`](https://github.com/{{ site.github.username }}{{ site.baseurl }}#custom-navbar), available via `_config.yml#L18` and configure `_data/navbar.yml`

### Browser support

Jelly Bean is by preference a forward-thinking project. In addition to the latest versions of Chrome, Safari (mobile and desktop), and Firefox, it is only compatible with Internet Explorer 9 and above.

### Download

Jelly Bean is developed on and hosted with GitHub. Head to the <a href="https://github.com/{{ site.github.username }}{{ site.baseurl }}">GitHub repository</a> for downloads, bug reports, and features requests.

Thanks!

```
Build infos:
  - Build time: {{ site.time | date_to_rfc822 }}
  - Unix build time: {{ site.time | date:"%s" }}
```

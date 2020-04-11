# Minima
A slenderize two-column [Jekyll](http://jekyllrb.com) documentation theme that pairs a prominent navbar with uncomplicated content. Its built on [Bootstrap](http://getbootstrap.com) responsive front-end framework.

[Demo the Theme](http://rimeofficial.github.com/jelly-bean/)

This is the raw HTML and styles that are used for the *minimal* theme on [GitHub Pages](http://pages.github.com/).

Syntax highlighting is provided on GitHub Pages by [Pygments](http://pygments.org).

## Pages
Create a list of pages in the navbar by assigning each Jekyll page the correct layout in the page's [front-matter](http://jekyllrb.com/docs/frontmatter/) and placing them in `_docs` folder
```
---
title: Foobar
---

The terms **foobar** (/ˈfuːbɑːr/), or **foo** and others are used as ...
```

## `Default` Navbar
Alphabetically sorted list of pages
![](./images/Screenshot%202016-06-05%2014.54.41.png)

## `Custom` Navbar
![](./images/Screenshot%202016-06-05%2014.54.58.png)

For custom list of pages change `Default` to `Custom` [_config.yml#L15](./_config.yml#L15) and configure `_data/navbar.yml`

```
- title: Getting Started
  pages:
  - Jekyll
  - About

- title: Your Content
  pages:
  - Example
```

## License

This work is licensed under a [CC0 1.0 Universal](http://creativecommons.org/publicdomain/zero/1.0/).


（ノ￣＾￣）ノ　┳┳　┣　┻┻　┫　┳┳

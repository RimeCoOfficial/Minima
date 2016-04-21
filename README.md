# Jelly Bean
A slenderize two-column [Jekyll](http://jekyllrb.com) documentation theme that pairs a prominent sidebar with uncomplicated content.

## Pages
Create a list of pages in the sidebar by assigning each Jekyll page the correct layout in the page's [front-matter](http://jekyllrb.com/docs/frontmatter/) and placing them in `_docs` folder
```
---
title: One
---
```

## Sidebar `Default`
Alphabetically sorted
![](./images/Screenshot%202016-04-21%2012.51.58.png?raw=true)

## Custom Sidebar
![](./images/Screenshot%202016-04-21%2012.51.37.png?raw=true)

For custom sidebar add `-custom` to `_layouts/default.html`
```
{% include sidebar-custom.html %}
```

and configure `_data/sidebar.yml`
```
- title: Getting Started
  pages:
  - one
  - two

- title: Your Content
  pages:
  - three
```

## Development

Jelly Bean has two branches, but only one is used for active development.

- `master` for development.  **All pull requests should be submitted against `master`.**
- `gh-pages` for our hosted site, which includes our analytics tracking code. **Please avoid using this branch.**

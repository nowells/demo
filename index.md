<script src="https://cdn.rawgit.com/clubajax/custom-elements-polyfill/821b16e1/index.js"></script>
<script src="https://ei-util-qa.va.opower.it/ei/x/embedded-api/test.js"></script>
<script>__maestro__.initialize({useFixtures: true});</script>

# Bookmarklet

<p>
  Drag the <a href="javascript:(function()%7Bvar%20el%20%3D%20document.createElement('script')%3Bel.src%20%3D%20'https%3A%2F%2Fs3.amazonaws.com%2Fx-web-maestro-static-content%2Fmaestro%2Fbookmarklets%2Finject-widget%2Fmain.js'%3Bdocument.body.appendChild(el)%7D)()">Opower Widget Injector</a> link to your bookmarks bar to inject widgets on any pages.
</p>

## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/nowells/demo/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

## Dynamic

<p><a href="javascript:document.querySelector('#dynamic').appendChild(document.createElement('opower-neighbor-comparison'))">Click me</a> to inject neighbor comparison</p>

<div id="dynamic"></div>

## Bill Compare
<opower-bill-compare-enhanced></opower-bill-compare-enhanced>

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/nowells/demo/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

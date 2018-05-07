<script src="https://cdn.rawgit.com/clubajax/custom-elements-polyfill/821b16e1/index.js"></script>
<script src="https://ei-util-qa.va.opower.it/ei/x/embedded-api/test.js"></script>
<script>__maestro__.initialize({useFixtures: true});</script>

# Bookmarklet

<p>
  Drag the <a href="javascript:(function()%7B(async()%20%3D%3E%20%7Bif%20(window.define)%20%7Bwindow.define.amd%20%3D%20false%3B%7Ddelete%20window.angular%3Bconst%20style%20%3D%20document.createElement('style')%3Bstyle.innerHTML%20%3D%20'.insertWidgetHere%20%7B%20outline%3Athick%20double%20%2332a1ce%3B%20%7D'%3Bdocument.body.appendChild(style)%3Bconst%20customElementShim%20%3D%20document.createElement('script')%3Bconst%20customElementShimLoaded%20%3D%20new%20Promise(resolve%20%3D%3E%20customElementShim.onload%20%3D%20resolve)%3BcustomElementShim.src%20%3D%20'https%3A%2F%2Fcdn.rawgit.com%2Fclubajax%2Fcustom-elements-polyfill%2F821b16e1%2Findex.js'%3Bdocument.body.appendChild(customElementShim)%3Bawait%20customElementShimLoaded%3Bconst%20opowerWidgets%20%3D%20%5B%5D%3Bconst%20oldDefine%20%3D%20customElements.define%3BcustomElements.define%20%3D%20function(name%2C%20...args)%20%7Bif%20(%2F%5Eopower-%2F.test(name))%20%7BopowerWidgets.push(name)%3B%7Dreturn%20oldDefine.call(this%2C%20name%2C%20...args)%3B%7D%3Bconst%20opowerApiEl%20%3D%20document.createElement('script')%3Bconst%20opowerApiElLoaded%20%3D%20new%20Promise(resolve%20%3D%3E%20opowerApiEl.onload%20%3D%20resolve)%3BopowerApiEl.src%20%3D%20'https%3A%2F%2Fei-util-qa.va.opower.it%2Fei%2Fx%2Fembedded-api%2Ftest.js%3Ffixtures%3Dtrue'%3Bdocument.body.appendChild(opowerApiEl)%3Bawait%20opowerApiElLoaded%3B__maestro__.initialize(%7BuseFixtures%3A%20true%7D)%3Blet%20prev%3Bdocument.body.addEventListener('mouseover'%2C%20handler)%3Bdocument.body.addEventListener('click'%2C%20insert)%3Bfunction%20insert(event)%20%7Bif%20(event.metaKey%20%26%26%20prev)%20%7Bprev.className%20%3D%20prev.className.replace(%2F%5CbinsertWidgetHere%5Cb%2F%2C%20'')%3Bconst%20placement%20%3D%20prev%3Bprev%20%3D%20undefined%3Bconst%20el%20%3D%20document.createElement('div')%3Bel.style%20%3D%20'position%3A%20fixed%3B%20top%3A%2050%25%3B%20left%3A%2050%25%3B'%3Bel.attachShadow(%7Bmode%3A%20%22open%22%7D)%3Bel.shadowRoot.innerHTML%20%3D%20'%3Cdiv%20style%3D%22padding%3A%200px%2010px%2020px%2010px%3B%20background%3A%20lightgray%3B%20border%3A%201px%20solid%20black%3B%22%3E%3Ch3%3ESelect%20Widget%3C%2Fh3%3E%3Cselect%3E%3Coption%3E%3C%2Foption%3E'%20%2BopowerWidgets.map(widget%20%3D%3E%20%60%3Coption%20value%3D%22%24%7Bwidget%7D%22%3E%24%7Bwidget%7D%3C%2Foption%3E%60).join('')%20%2B'%3C%2Fselect%3E%3C%2Fdiv%3E'%3Bdocument.body.appendChild(el)%3Bel.shadowRoot.querySelector('select').addEventListener('change'%2C%20()%20%3D%3E%20%7Bconst%20selectEl%20%3D%20el.shadowRoot.querySelector('select')%3Bconst%20opowerWidgetName%20%3D%20selectEl.options%5BselectEl.selectedIndex%5D.value%3Bif%20(opowerWidgetName)%20%7Bplacement.insertBefore(document.createElement(opowerWidgetName)%2C%20placement.firstChild)%3B%7Ddocument.body.removeChild(el)%3B%7D)%3B%7D%7Dfunction%20handler(event)%20%7Bif%20(event.target%20%3D%3D%3D%20document.body%20%7C%7C(prev%20%26%26%20prev%20%3D%3D%3D%20event.target))%20%7Breturn%3B%7Dif%20(prev%20%26%26%20prev.className%20%26%26%20prev.className.replace)%20%7Bprev.className%20%3D%20prev.className.replace(%2F%5CbinsertWidgetHere%5Cb%2F%2C%20'')%3Bprev%20%3D%20undefined%3B%7Dif%20(event.target%20%26%26%20event.metaKey)%20%7Bprev%20%3D%20event.target%3Bprev.className%20%2B%3D%20%22%20insertWidgetHere%22%3B%7D%7D%7D)()%7D)()">Opower Widget Injector</a> link to your bookmarks bar to inject widgets on any pages.
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

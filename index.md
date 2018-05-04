<script src="https://cdn.rawgit.com/clubajax/custom-elements-polyfill/821b16e1/index.js"></script>
<script src="https://ei-util-qa.va.opower.it/ei/x/embedded-api/test.js"></script>
<script>__maestro__.initialize({useFixtures: true});</script>

# Bookmarklet

<p>
  Drag <a href="javascript:(function()%7B(async()%20%3D%3E%20%7Bconst%20style%20%3D%20document.createElement('style')%3Bstyle.innerHTML%20%3D%20'.insertWidgetHere%20%7B%20outline%3Athick%20double%20%2332a1ce%3B%20%7D'%3Bdocument.body.appendChild(style)%3Bconst%20customElementShim%20%3D%20document.createElement('script')%3Bconst%20customElementShimLoaded%20%3D%20new%20Promise(resolve%20%3D%3E%20customElementShim.onload%20%3D%20resolve)%3BcustomElementShim.src%20%3D%20'https%3A%2F%2Fcdn.rawgit.com%2Fclubajax%2Fcustom-elements-polyfill%2F821b16e1%2Findex.js'%3Bdocument.body.appendChild(customElementShim)%3Bawait%20customElementShimLoaded%3Bconst%20opowerApiEl%20%3D%20document.createElement('script')%3Bconst%20opowerApiElLoaded%20%3D%20new%20Promise(resolve%20%3D%3E%20opowerApiEl.onload%20%3D%20resolve)%3BopowerApiEl.src%20%3D%20'https%3A%2F%2Fei-util-qa.va.opower.it%2Fei%2Fx%2Fembedded-api%2Ftest.js%3Ffixtures%3Dtrue'%3Bdocument.body.appendChild(opowerApiEl)%3Bawait%20opowerApiElLoaded%3B__maestro__.initialize(%7BuseFixtures%3A%20true%7D)%3Blet%20prev%3Bdocument.body.addEventListener('mouseover'%2C%20handler)%3Bdocument.body.addEventListener('click'%2C%20insert)%3Bfunction%20insert(event)%20%7Bif%20(event.metaKey%20%26%26%20prev)%20%7Bprev.className%20%3D%20prev.className.replace(%2F%5CbinsertWidgetHere%5Cb%2F%2C%20'')%3Bconst%20opowerWidgetName%20%3D%20prompt('What%20widget%20would%20you%20like%20to%20insert%3F'%2C%20'data-browser')%3Bprev.insertBefore(document.createElement('opower-'%20%2B%20opowerWidgetName)%2C%20prev.firstChild)%3Bprev%20%3D%20undefined%3B%7D%7Dfunction%20handler(event)%20%7Bif%20(event.target%20%3D%3D%3D%20document.body%20%7C%7C(prev%20%26%26%20prev%20%3D%3D%3D%20event.target))%20%7Breturn%3B%7Dif%20(prev%20%26%26%20prev.className%20%26%26%20prev.className.replace)%20%7Bprev.className%20%3D%20prev.className.replace(%2F%5CbinsertWidgetHere%5Cb%2F%2C%20'')%3Bprev%20%3D%20undefined%3B%7Dif%20(event.target%20%26%26%20event.metaKey)%20%7Bprev%20%3D%20event.target%3Bprev.className%20%2B%3D%20%22%20insertWidgetHere%22%3B%7D%7D%7D)()%7D)()">this link</a> to your bookmarks bar to inject widgets on any pages.
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

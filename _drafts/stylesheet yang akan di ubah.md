---
title: Stylesheet untuk diubah
description: Stylesheet pada bawaan template tidak beraturan dan beberapa class yang ingin dikostumisasi
draft: true
---

Tasks now moved to [here](obsidian://open?vault=01%20Minimalist%20Notes&file=50%20Journals%2F2023%2F02%2F230209)

- `blockquote` color tidak terlihat pada background saat ini
- add breakpoint rules #todo 
	- in this scss file, min-width: 820px to increase font-size
	- i/m not so happy with the text and the content width
		- to fix this, it can be rule in `<content>`
			- example: ```max-width: 40em; font-size: 1.125em;```
- in [[archive]] page, description line height is horrible when viewed in mobile viewport.
- color schema or palette:
	- [x] links #todo
	- [x] backlink box #todo 
	- [x] text
		- [x] sub text #todo 
		- [x] normal #todo
		- [x] highlight text #todo 
- other capture:
	- capture means, capture frontmatter in notes.
		- for capturing current note use double curly brackets with inside `page.frontmattertocapture`
		- output {{page.description}}
- [x] notes with table of contents #todo 
	- example [[notes with toc]]
	- finding [A Jekyll TOC without Plugins or JavaScript](https://allejo.io/blog/a-jekyll-toc-without-plugins-or-javascript/) not worked
	- try this [How to Create a Table of Content in Jekyll blog Without any Plugin](https://ranvir.xyz/blog/creating-table-of-content-in-jekyll-blog-without-plugin/#conclusion) bekerja dengan baik, namun hanya pada H2.
- [x] separate graph in page #todo , you can see [[graph]]


# Kaslaanka

A minimalist theme for Hugo.

this theme is a fork of [Hugo-tanka](https://github.com/nanxstats/hugo-tanka) theme.

## new features

* remove the bloat (utterances comments, progressivly, highlight.js)
* scriptless by default.
* removed bootstrap.
* changed how the index, single pages and blog posts look.
* blog list on the home page is limited, if the users want to see more they go to /blog/
* listing projects on the home page.
* brief about me on the home page.
* support unlisted articles.
* better favicons.
* better tags
* add multiple languages support
* **HUGE** first letter paragraph (if you want)

### custom.css

add your custom css here `/static/css/custom.css`

```css
/* <span class="first-letter">H</span>ello World! */
.first-letter {
	font-family: "Roboto Serif";
}
```

### custom.js
add your custom javascript here `/static/js/custom.js`

```js
// be creative
for(;;){alert("HAHAHAHAHAH")}
```

### Tags

```yaml
tags:
  - hello
  - ok
```

this post will be listed at /tags/hello/ and /tags/ok/

### config.yml
```yaml

sitename: "Site Name!"

# Links of the navbar
menu:
  primary:
    - name: Home
      url: /
      weight: 1
    - name: About me
      url: /aboutme
      weight: 2
    - name: Subscribe
      url: /index.xml
      weight: 3

# You can add languages!
# do not expect it to work out of the box
# https://gohugo.io/content-management/multilingual/
languages:
  en:
    LanguageName: English
  ru:
    LanguageName: русский
    contentDir: content/blog/ru

params:
  # it will produce: copyrights (c) 2022 joe
  copytights: joe
  # path to the favicon directory
  # see ./layouts/_defaults/baseof.html line #30 to line #37
  faviconpath: "/img/favicon"
  # projects will show in the index page
  myprojects:
    - name: AAAAA
      description: BBBBBBB
      url: https://example.com
    - name: XXXXXXXXXXXXXXX
      description: YYYYYYYYYYYYYYYYYYY
      url: https://example.com
  # link to more projects
  # show your github repositories as example
  # or create your own page.
  projectsURL: https://github.com/<username>?tab=repositories

  # a brief about me
  brief_about: hello there, its me <i>joe<i>.

# and don't forget
theme: kaslaanka
```

### posts

you can make a post unlisted by adding the following

```markdown
---

unlisted: true

---
```
### external scripts
you can add external scripts in `/layouts/partials/scripts.html`

```html
<script src="..." ... ></script>
```

### LICENSE
GPL-3.0 [LICENSE](./LICENSE).

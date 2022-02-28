# Kaslaanka

A minimalist theme for Hugo.

this theme is a fork of [Hugo-tanka](https://github.com/nanxstats/hugo-tanka) theme.

## new features

- remove the bloat (utterances comments, progressivly, highlight.js)

- scriptless by default.

- removed bootstrap completely. [see here](https://github.com/M1cR0xf7/kaslaanka/commit/7a33f88387150c0d483c289086001f7d4f776706).

- changed how the index, single pages and blog posts look.

- blog list on the home page is limited, if the users want to see more they go to /blog/

- listing projects on the home page.

- brief about me on the home page.

- support unlisted articles.

- better favicons.

- better tags

- add multiple languages support

- **HUGE** first letter paragraph (if you want)

### custom.css

```css
/* <span class="first-letter">H</span>ello World! */
.first-letter {
	font-family: "Roboto Serif";
}
```

### Tags

```yaml
tags:
  - hello
  - ok
```

this post will be listed at /tags/hello/ and /tags/ok/

### config.yml changes
```yaml

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
```

### posts

you can make a post unlisted by adding the following

```markdown
---

unlisted: true

---
```

### LICENSE
GPL-3.0 [LICENSE](./LICENSE).

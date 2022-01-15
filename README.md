# Kaslaanka

A minimalist theme for Hugo.

this theme is a fork of [Hugo-tanka](https://github.com/nanxstats/hugo-tanka) theme.

## new features

- remove the bloat (utterances comments, progressivly, highlight.js)

- scriptless by default

- updated to bootstrap 5 (might get rid of bootstrap completely *TODO*: later...)

- minor UI changes

- blog list on the home page is limited, if the users want to see more they go to /blog/

- listing projects on the home page

- brief about me on the home page

- support unlisted articles

- better favicons

### config.yml changes
```yaml
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

# Kaslaanka
fork of the [Hugo-tanka](https://github.com/nanxstats/hugo-tanka) theme

## new features

- bootstrap 5: updated to bootstrap 5

- minor UI changes

- blog list on the home page is limited, if the users want to see more they go to /blog/

- listing projects on the home page

- brief about me on the home page


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

  # a brief about me
  brief_about: hello there, its me <i>joe<i>.
```

### posts

you can make a post unlisted by adding

```markdown
---.
...
unlisted: true
...
---
```

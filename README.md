# Groovy theme for Hugo

### Dark theme inspired by the Gruvbox color scheme

### [PREVIEW](https://aarol.dev)

The theme is made to be simple and can be extended easily without unnecessary build steps.

This theme requires hugo **extended** 0.80 or higher because it needs Hugo's built in sass compilation.

## Getting started

```
$ git submodule add https://github.com/aarol/hugo-theme-groovy.git themes/groovy
```

In your `config.toml`:

```toml
baseURL = '/'
languageCode = 'en-us'
theme = 'groovy'
title = '<title>'

[params]
  subtitle = 'A programming blog/personal site'

[menu]
[[menu.main]]
  identifier = "about"
  name = "About"
  url = "/about"

[[menu.main]]
  identifier = "posts"
  name = "Posts"
  url = "/"

[[menu.main]]
  identifier = "projects"
  name = "Projects"
  url = "/projects"
```

Create a new post:
```bash
hugo new posts/my-first-post.md
```

If you plan on changing the theme, you can fork the repo on GitHub and then add your fork instead:

```bash
$ git submodule add https://github.com/<username>/hugo-theme-groovy.git themes/groovy
```

## Features:

- Syntax highlighting. To enable, copy this to your site's `config.toml`:
  ```toml
  [markup]
    [markup.highlight]
        codeFences = true
        guessSyntax = true
        tabWidth = 4
        noClasses = false
  ```
- Math rendering using Katex: To enable, use the math parameter in frontmatter.
  ```yaml
  math: true
  ```

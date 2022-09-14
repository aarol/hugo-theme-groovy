# Groovy theme for Hugo

### Dark theme inspired by the Gruvbox color scheme

### [PREVIEW](https://aarol.dev)

The theme is made to be simple and can be extended easily without unnecessary build steps.

This theme requires hugo **extended** 0.80 or higher because it needs Hugo's built in sass compilation.

## Getting started

You can clone this repository to test out the theme, but you should fork it instead if you want to make modifications.

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


[markup.goldmark]
  [markup.goldmark.renderer]
    # to enable markdown shortcodes in content (caption)
    # enable only if content is trusted
    unsafe = true
    
```

Create a new post:
```bash
hugo new posts/my-first-post.md
```
To insert images, create a directory /content/posts/{slug}, then rename {slug}.md to /content/posts/{slug}/index.md

Then adding images is as simple as copying them to the same directory and linking with the markdown image syntax.

## Features:

- Syntax highlighting with the Gruvbox theme. To enable, copy this to your site's `config.toml`:
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
- Images are automatically optimized to use webp when possible.
- Caption shortcode to put text below images
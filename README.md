# Groovy theme for Hugo

Dark theme inspired by the Gruvbox color scheme

## PREVIEW: <https://aarol.dev>

The theme is made to be simple and can be extended easily without unnecessary build steps.

This theme requires hugo **extended** 0.124 or higher because it needs Hugo's built in sass compiler and Webp encoder.

## Getting started

You can clone this repository to test out the theme, but you should fork it instead if you want to make modifications.

```sh
git submodule add https://github.com/aarol/hugo-theme-groovy.git themes/groovy
```

In your `config.toml`:

```toml
baseURL = '/'
languageCode = 'en-us'
theme = 'groovy'
title = '<title>'

[params]
  subtitle = 'A programming blog/personal site'

[languages]
[languages.en]
languageCode="en"
languageName="English"

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

To insert images, create a directory /content/posts/{slug}, then rename /content/posts/{slug}.md to /content/posts/{slug}/index.md

Then adding images is as simple as copying them to the same directory and linking with the markdown image syntax.

## Features

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
  ---
  math: true
  ---
  ```

- Mermaid graphs: To enable, create a codeblock with the language "mermaid":
  
  ````markdown
  ```mermaid
  graph TD;
    A-->B;
    A-->C;
  ```
  ````

- Images are automatically converted to webp for better compression and displayed when supported by the browser.
- Text in the 'title' section of images is put below the image as a caption.
- Automatically generates OpenGraph preview thumbnails

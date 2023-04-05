# Terminal-Hacked

Dark, clean and minimalistic theme for [hugo][1].
Based on the [Terminal][2] theme by [panr][3]

### ⚠️ The theme needs at least Hugo **Extended** v0.90.x.

---
- [How to start](#how-to-start)
- [How to run your site](#how-to-run-your-site)
- [How to configure](#how-to-configure)

#### Code highlighting

A custom syntax highlighting based on PrismJS. All you need to do is to wrap you code like this:

````
```html
  // your code here
```
````

**Supported languages**: actionscript, apacheconf, applescript, bash, c, clike, cmake, coffeescript, cpp, csharp, csp, css, css-extras, diff, django, docker, elixir, elm, erlang, flow, fsharp, git, go, graphql, haml, handlebars, haskell, http, java, javascript, json, jsx, kotlin, latex, less, llvm, makefile, markdown, markup, markup-templating, nasm, objectivec, ocaml, perl, php, php-extras, powershell, processing, pug, python, r, reason, ruby, rust, sass, scala, scheme, scss, sql, stylus, swift, textile, toml, tsx, twig, typescript, vim, visual-basic, wasm, yaml.

## How to start

You can download the theme manually by going to [https://github.com/trefmanic/hugo-theme-terminal-hacked.git](https://github.com/trefmanic/hugo-theme-terminal-hacked.git) and pasting it to `themes/terminal-hacked` in your root directory.

You can also install the theme with GIT:

### Install theme locally

```bash
git clone https://github.com/trefmanic/hugo-theme-terminal-hacked.git themes/terminal-hacked
```
This will clone the repository directly to the `themes/terminal` directory.

## How to run your site

```bash
hugo server -t terminal-hacked
```

and go to `localhost:1313` in your browser. From now on all the changes you make will go live, so you don't need to refresh your browser every single time.

## How to configure

The theme doesn't require any advanced configuration. Just copy:

```toml
baseurl = "/"
languageCode = "en-us"
# Add it only if you keep the theme in the `themes` directory.
# Remove it if you use the theme as a remote Hugo Module.
theme = "terminal-hacked"
paginate = 5

[params]
  # dir name of your main content (default is `content/posts`).
  # the list of set content will show up on your index page (baseurl).
  contentTypeName = "posts"

  # if you set this to 0, only submenu trigger will be visible
  showMenuItems = 1

  # show selector to switch language
  showLanguageSelector = false

  # set theme to full screen width
  fullWidthTheme = false

  # center theme with default width
  centerTheme = false

  # set post to show the last updated
  # If you use git, you can set `enableGitInfo` to `true` and then post will automatically get the last updated
  showLastUpdated = false

  # set a custom favicon (default is a `themeColor` square)
  # favicon = "favicon.ico"

  # Provide a string as a prefix for the last update date. By default, it looks like this: 2020-xx-xx [Updated: 2020-xx-xx] :: Author
  # updatedDatePrefix = "Updated"

[languages]
  [languages.en]
    languageName = "English"
    title = "Terminal"
    subtitle = "A simple, retro theme for Hugo"
    owner = ""
    keywords = ""
    copyright = ""
    menuMore = "Show more"
    readMore = "Read more"
    readOtherPosts = "Read other posts"
    newerPosts = "Newer posts"
    olderPosts = "Older posts"
    missingContentMessage = "Page not found..."
    missingBackButtonLabel = "Back to home page"
    minuteReadingTime = "min read"
    words = "words"

    [languages.en.params.logo]
      logoText = "Terminal"
      logoHomeLink = "/"

    [languages.en.menu]
      [[languages.en.menu.main]]
        identifier = "about"
        name = "About"
        url = "/about"

[module]
  # In case you would like to make changes to the theme and keep it locally in you repository,
  # uncomment the line below (and correct the local path if necessary).
  # --
  # replacements = "github.com/panr/hugo-theme-terminal -> themes/terminal"
[[module.imports]]
  path = 'github.com/panr/hugo-theme-terminal'
```

to `config.toml` file in your Hugo root directory and change params fields.

**NOTE:** Please keep in mind that currently `main menu` doesn't support nesting.

[1]: https://gohugo.io/ "hugo: framework for building static sites"
[2]: https://github.com/panr/hugo-theme-terminal "Terminal hugo theme"
[3]: https://github.com/panr "Author's github profile"

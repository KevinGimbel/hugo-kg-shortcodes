# hugo-shortcodes-theme
> A collection of hugo shortcodes I created

This repository holds a collection of shortcodes for the [Hugo](https://gohugo.io) static site generator. Inside each folder is a README.md file with information on how to setup the shortcode.

## Setup

1. Get the theme. This is done by cloning the git repository to your `themes` directory (or adding it as a [git sub module](https://git-scm.com/book/en/v2/Git-Tools-Submodules))
```bash
cd path/to/hugo/themes
# Clone the repo
git clone https://github.com/kevingimbel/hugo-kg-shortcodes.git
# OR add sub module
git submodule add https://github.com/kevingimbel/hugo-kg-shortcodes.git
```

2. Load the theme in your `config.toml` or `config.yml`
```toml
theme = ["hugo-kg-shortcodes"]
```

3. Include the hook partial in your footer (for example in `_baseof.html`).

```
{{ partial "kg-shortcodes-hook.html" . }}
```

The hook will load additional JavaScript libraries if needed, see shortcode documentations for more details.

## Documentation

A detailed documentation for each shortcode is available here:

- [English documentation](https://kevingimbel.github.io/hugo-kg-shortcodes/)
- [German documentation](https://kevingimbel.github.io/hugo-kg-shortcodes/de/)
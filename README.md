# hugo-shortcodes-theme
> A collection of hugo shortcodes I created

This repository holds a collection of shortcodes for the [Hugo](https://gohugo.io) static site generator. Inside each folder is a README.md file with information on how to setup the shortcode.

## Setup

1. Get the theme. This is done by cloning the git repository to your `themes` directory.
```bash
cd path/to/hugo/themes
git clone https://github.com/kevingimbel/kg-hugo-shortcodes-theme.git 
```

2. Load the theme in your `config.toml` or `config.yml`
```toml
theme = ["kg-hugo-shortcodes-theme"]
```

3. Include the hook partial in your footer.

```
{{ partial "kg-shortcodes-hook.html" . }}
```

The hook will load additional JavaScript libraries if needed, see shortcode documentations for more details.

## Documentation

A detailed documentation of each shortcode can be found in the `documentation` directory. 
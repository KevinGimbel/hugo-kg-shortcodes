---
date: 2020-06-02
title: CodePen
subtitle: "A shortcode for including CodePen embeds on your website"
aliases:
  - /cdpn/
---
This will load the CodePen embed script everytime a CodePen shortcode has been used.

## Usage

### Global config

This shortcodes supports global configs that can be loaded from the Sites' `params` object. `user`, `editable` and `preview` should be set and will act as a default. `script_src` can be used to load the embed script from a custom source instead of https://production-assets.codepen.io/assets/embed/ei.js

In the `config.toml` or `config.yaml` global values for the following variables can be set:

- `user`: default user
- `editable`: enabled inline editing of pens
- `preview`: enables auto run, if disabled user must click "Run pen"
- `script_src`: Can be used to load script from custom source, default is https://production-assets.codepen.io/assets/embed/ei.js

**YAML config**
```yaml
params:
  kg_shortcodes:
    codepen:
      user: "kevingimbel"
      editable: true
      preview: true
      script_src: "/codepen.js"
```

**TOML config**
```toml
[params.kg_shortcodes.codepen]
user = "kevingimbel"
editable = true
preview = true
script_src = "/codepen.js"
```

### Parameters

The CodePen shortcode takes the following arguments.

| Argument | Default Value | Values | Description |
|----------|---------------|--------|-------------|
| `height` | 256 | Number | Height of the embedded iFrame |
| `theme` | `dark` | String | The theme which will be used |
| `result` | `html,result` | Comma separated list. Any of `css`, `js`, `html`, `result`  | The tabs which will be shown in the embed by default |
| `user` | String | Boolean | The user to which this Pen belongs |
| `editable` | Seitenkonfiguration | Boolean | Defines if the CodePen is editable by the user |
| `preview` | Seitenkonfiguration | Boolean | Defines if the CodePen has "Run Pen" button or loads by default |
| `slug` | - | CodePen Slug (alphanumeric) | The Slug of the Pen |
| `title` | - | String | The title of the pen, shown if the embed can't be loaded |

### Example Usage

**Minimal options**

```go
{{%/* codepen slug="78d261a36ecded2b75d5260cb7056fce" title="An example embed" */%}}
```

**All options**

```go
{{%/* codepen slug="78d261a36ecded2b75d5260cb7056fce" title="An example embed" height="300" theme="light" result="css,js" user="ausername" editable="false" preview="false" */%}}
```

### Live Example

The CodePen shortcode is used on my private site, for example in the article ["CSS Custom Properties and a new look"](https://www.kevingimbel.com/css-custom-properties-and-a-new-look/).

{{% codepen slug="iqDIv" title="single-div Link from The Legend of Zelda" height="400" %}}
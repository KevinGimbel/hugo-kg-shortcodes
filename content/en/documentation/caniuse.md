---
date: 2020-06-02
title: Can I Use
subtitle: "A shortcode for including CanIUse.com embeds on your website"
aliases:
  - /ciu/
---

This will load the caniuse embed script every time a caniuse shortcode has been used. This shortcode uses the excellent [caniuse embed script](https://github.com/ireade/caniuse-embed/) by [Ire Aderinokun](https://github.com/ireade).

## Usage

### Global config

In the `config.toml` or `config.yaml` global values for the following variables can be set:

- `accessible_colors`: Enable accessible colors for all embeds unless disabled when embedding
- `script_src`: Load embed script from different source, defaults to https://cdn.jsdelivr.net/gh/ireade/caniuse-embed/public/caniuse-embed.min.js

**YAML config**
```yaml
params:
  kg_shortcodes:
    caniuse:
      accessible_colors: true
      script_src: "/caniuse-emebd.js"
```

**TOML config**
```toml
[params.kg_shortcodes.caniuse]
accessible_colors = true
script_src = "/caniuse-emebd.js"
```

### Parameters

The caniuse shortcode takes the following arguments.

| Argument | Default Value | Values | Description |
|----------|---------------|--------|-------------|
| `feature` | - | String | The feature to inclide, e.g. `css-variables`, `css-grid`, etc. |
| `periods` | `future_1,current,past_1,past_2` | String | How many past / future browsers to display. See periods below |
| `accessible_colors` | `false` | `true` / `false` | Set to true if accessible colors should be used.|

List of **periods**  which can be used:
- `future_3`
- `future_2`
- `future_1`
- `current`
- `past_1`
- `past_2`
- `past_3`
- `past_4`
- `past_5`


### Example Usage

**Minimal options**

```html
{{%/* caniuse feature="css-variables" */%}}
```

**All options**

```html
{{%/* caniuse feature="css-grid" periods="current,past_1,past_2" accessible_colors="true" */%}}
```

### Live Example

The caniuse shortcode is used on my private site, for example in the article ["CSS Custom Properties and a new look"](https://www.kevingimbel.com/css-custom-properties-and-a-new-look/).

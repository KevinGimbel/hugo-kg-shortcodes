---
date: 2020-06-02
title: Mastodon
subtitle: "A shortcode for including Mastodon statuses on your website"
aliases:
  - /mst/
---

## Usage

### Global config


### Globale Konfiguration

In the `config.toml` or `config.yaml` global values for the following variables can be set:

- `script_src`: The source from where the embed JavaScript will be loaded, defaults to https://mastodon.social/embed.js

**YAML config**
```yaml
params:
  kg_shortcodes:
    mastodon:
      script_src: "https://beispiel-instanz.de/embed.js"
```

**TOML config**

```toml
[params.kg_shortcodes.mastodon]
script_src = "https://beispiel-instanz.de/embed.js"
```


### Parameters

The Mastodon shortcode takes the following arguments.

| Argument | Default Value | Values | Description |
|-----------|--------------|--------|-------------|
|`status`| - | String | Status ID taken from the URL of a toot. |
|`width`| 400 | Number | The width of the embeded iframe|
|`height`| 333 | Number | The height of the embeded iframe|

### Example Usage

### Live Example
A live example can be [seen on my website](https://www.kevingimbel.de/mastodon-embed-shortcode-for-hugo/)

**Minimal options**

```go
{{%/* mastodon status="https://mastodon.social/@kevingimbel/100700713283716694" */%}}
```

**All options**

```go
{{%/* mastodon status="https://mastodon.social/@kevingimbel/100700713283716694" width="600" height="300" */%}}
```
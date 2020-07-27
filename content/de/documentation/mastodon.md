---
date: 2020-06-02
title: "Mastodon"
subtitle: "Shortcode zur Einbindung von Mastodon Beiträgen"
aliases:
  - /mst/
---

Der [Mastodon](https://joinmastodon.org/) Shortcode kann verwendet werden um einen Mastodon Status einzubinden. Es ist dabei egal auf welcher Instanz der Beitrag veröffentlich wurde.

## Anleitung

### Globale Konfiguration

In der `config.toml` oder `config.yaml` können Globale Werte für diesen Shortcode hinterlegt werden:

- `script_src`: Quelle für Embed JavaScript, Standard ist das Script von https://mastodon.social/embed.js - jede Mastodon Instanz stellt das Embed Script unter `/embed.js` bereit, somit kann einfach das Script einer eigenen Instanz verwendet werden.

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

### Parameter

| Parameter | Standardwert | Typ | Beschreibung |
|-----------|--------------|--------|-------------|
|`status`| - | String | Der Link zum Beitrag auf einer beliebigen Mastodon Instanz|
|`width`| 400 | Number | Die Breite des eingebetteten Status |
|`height`| 333 | Number | Die Höhe des eingebetteten Status |


**Minimale Optionen**

```go
{{</* mastodon status="https://mastodon.social/@kevingimbel/100700713283716694" */>}}
```

**Alle Optionen**

```go
{{</* mastodon status="https://mastodon.social/@kevingimbel/100700713283716694" width="600" height="300" */>}}
```

### Beispiel

Der Shortcode kann in [diesem Beitrag auf kevingimbel.de](https://www.kevingimbel.de/mastodon-embed-shortcode-for-hugo/) gesehen werden.

{{< mastodon status="https://mastodon.social/@kevingimbel/100700713283716694" height="300" >}}
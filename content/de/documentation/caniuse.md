---
date: 2020-06-02
title: "Can I Use"
subtitle: "Shortcode für die Einbindung von CanIUse.com Daten auf deiner Website"
aliases:
  - /ciu/
---
Dieser Shortcode ermöglicht die einfache Einbindung eines "CanIUse.com" widgets auf der eigenen Website. Hierfür wird der Open Source Service [caniuse embed script](https://github.com/ireade/caniuse-embed/) von [Ire Aderinokun](https://github.com/ireade) verwendet.

## Anleitung

### Globale Konfiguration

In der `config.toml` oder `config.yaml` können Globale Werte für diesen Shortcode hinterlegt werden:

- `accessible_colors`: Aktiviert Barrierefreie Farben für alle Einbettungen (außer wenn explizit deaktiviert)
- `script_src`: Lädt Script aus eigener Quelle statt von https://cdn.jsdelivr.net/gh/ireade/caniuse-embed/public/caniuse-embed.min.js

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

### Parameter

Der caniuse Shortcode hat folgende Parameter:

| Parameter | Standardwert | Typ | Beschreibung |
|----------|---------------|--------|-------------|
| `feature` | - | String | Das Feature welches angezeigt werden soll, z.B. `css-variables`, `css-grid`, usw. |
| `periods` | `future_1,current,past_1,past_2` | String | Wie viele Zukünftige und vergangene Browser Versionen angezeigt werden sollen. |
| `accessible_colors` | `false` | `true` / `false` | Aktiviert das Barrierefreie Farbschema. Statt Rot/Grün werden Farben verwendet die auch für Leute mit Sehbeeinträchtigungen erkennbar sind. Kann auch global gesetzt werden (siehe oben) |

Liste der Möglichen  **periods**:
- `future_3`
- `future_2`
- `future_1`
- `current`
- `past_1`
- `past_2`
- `past_3`
- `past_4`
- `past_5`


### Beispiel Einbindung

**Minimale Optionen**

```go
{{</* caniuse feature="css-variables" */>}}
```

**Alle Optionen**

```go
{{</* caniuse feature="css-grid" periods="current,past_1,past_2" accessible_colors="true" */>}}
```

### Beispiel

Der Shortcode kann in Aktion auf meinem Blog im Artikel ["CSS Custom Properties and a new look"](https://www.kevingimbel.com/css-custom-properties-and-a-new-look/) gesehen werden.

Alternativ ist er ebenfalls hier eingebunden:

**Minimale Optionen**

{{< caniuse feature="css-variables" >}}

**Alle Optionen**

{{< caniuse feature="css-grid" periods="current,past_1,past_2" accessible_colors="true" >}}
---
date: 2020-06-02
title: "CodePen"
subtitle: "Shortcode für die Einbindung von CodePen \"Pens\" auf deiner Website"
aliases:
  - /cdpn/
---
Dieser Shortcode lädt das CodePen Embed JavaScript und erzeugt den HTML Code für das Einbetten von CodePen "Pens".

## Anleitung

### Globale Konfiguration

In der `config.toml` oder `config.yaml` können Globale Werte für diesen Shortcode hinterlegt werden:

- `user`: Standard User für den CodePens eingebettet werden sollen
- `editable`: Gibt an ob eingebettete Pens editierbar sind
- `preview`: Gibt an ob Pens automatisch ausgeführt werden oder der Nutzer auf "Run Pen" klicken muss (`true`: Nutzer muss auf "Run Pen" klicken, `false`: Pen wird automatisch ausgeführt)
- `script_src`: Kann benutzt werden um Embed Script aus einer anderen Quelle zu laden. Standard ist https://production-assets.codepen.io/assets/embed/ei.js

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

### Parameter

Dieser Shortcode akzeptiert folgende Parameter

| Parameter | Standardwert | Typ | Beschreibung |
|----------|---------------|--------|-------------|
| `height` | 256 | Number | Höhe des iFrames in welchem der Pen eingebettet wird |
| `theme` | `dark` | String | Das Design für den Pen |
| `result` | `html,result` | List<String> | Jeder der folgenden Werte kann verwendet werden: `css`, `js`, `html`, `result` (Kombination aus ein oder mehr) |
| `user` | Seitenkonfiguration |  String | Der Nutzer dem der Pen gehört |
| `editable` | Seitenkonfiguration | Boolean | Definiert ob der Pen verändert werden kann oder nicht |
| `preview` | Seitenkonfiguration | Boolean | `true`: Pen hat einen "Run Pen" button <br> `false`: Pen wird automatisch ausgeführt |
| `slug` | `-` | String (Alphanumerisch) | Der "Slug" des CodePen Pens. Besteht aus Buchstaben und Zahlen (z.B. `iqDIv`) |
| `title` | `-` | String | Text der gezeigt wird, wenn der Pen nicht geladen werden kann |

### Beispiel

**Minimale Optionen**

```go
{{</* codepen slug="78d261a36ecded2b75d5260cb7056fce" title="An example embed" */>}}
```

**Alle Optionen**

```go
{{</* codepen slug="78d261a36ecded2b75d5260cb7056fce" title="An example embed" height="300" theme="light" result="css,js" user="ausername" editable="false" preview="false" */>}}
```

### Beispiel

Auf kevingimbel.de wird der Shortcode im Artikel ["CSS Custom Properties and a new look"](https://www.kevingimbel.com/css-custom-properties-and-a-new-look/) genutzt.

Alternativ ist hier eine Live Beispiel

{{< codepen slug="iqDIv" title="single-div Link from The Legend of Zelda" height="400" >}}
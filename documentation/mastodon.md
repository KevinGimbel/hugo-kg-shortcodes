# mastodon
> A shortcode for including Mastodon statuses on your website

## Usage

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

```html
{{% mastodon status="https://mastodon.social/@kevingimbel/100700713283716694" %}}
```

**All options**

```html
{{% mastodon status="https://mastodon.social/@kevingimbel/100700713283716694" width="600" height="300" %}}
```
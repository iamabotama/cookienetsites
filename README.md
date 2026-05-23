# CookieChain Widget

A lightweight, embeddable widget that displays CookieChain social links, token information, and ecosystem links on any website.

## Quick Install

Add this single line anywhere in your HTML where you want the widget to appear:

```html
<script src="https://iamabotama.github.io/cookienetsites/cookiechain-page-embed.html"></script>
```

Or use the raw GitHub URL:

```html
<script src="https://raw.githubusercontent.com/iamabotama/cookienetsites/main/cookiechain-page-embed.html"></script>
```

## What It Displays

- **Social Links** - Twitter and Telegram buttons
- **$COOK Token** - Token name and contract address
- **Ecosystem Links** - Configurable links to CookieChain projects

## Styling

The widget is self-contained with inline styles:
- Max width: 420px
- Responsive and mobile-friendly
- Blue gradient theme
- No external CSS dependencies

## Configuration

The widget pulls its data from `cookiechain.json`. To customize the displayed links, edit that file:

```json
{
  "twitter_url": "https://x.com/TheCookieChain",
  "telegram_url": "https://t.me/+YulIZhqjDrw3NDcx",
  "ca": "YOUR_CONTRACT_ADDRESS",
  "links": [
    { "label": "Link Name", "url": "https://example.com" }
  ]
}
```

## Links

- [Twitter](https://x.com/TheCookieChain)
- [Telegram](https://t.me/+YulIZhqjDrw3NDcx)


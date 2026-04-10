# Catholic Owned Designs

Design screens and assets for the Catholic Owned marketplace — a platform connecting consumers with Catholic-owned businesses.

## Stitch Project

These designs are managed in Google Stitch:

- **Project:** Catholic Owned Presentation Screenshots
- **Project ID:** `6815352881069036676`
- **URL:** https://stitch.withgoogle.com/projects/6815352881069036676

## Stitch MCP Server Setup

The Stitch MCP server allows Claude Code (or any MCP-compatible tool) to interact with the Stitch project programmatically — listing screens, generating new designs, editing existing ones, and downloading HTML.

### Prerequisites

```bash
npm install @google/stitch-sdk @modelcontextprotocol/sdk
```

### Proxy Script

The file `stitch-mcp-server.mjs` is a lightweight proxy that exposes the Stitch API as an MCP server using stdio transport. It authenticates via the `STITCH_API_KEY` environment variable.

### Claude Code Configuration

Add to your `~/.mcp.json`:

```json
{
  "mcpServers": {
    "stitch": {
      "command": "node",
      "args": ["/path/to/stitch-mcp-server.mjs"],
      "env": {
        "STITCH_API_KEY": "your-stitch-api-key"
      }
    }
  }
}
```

Get a Stitch API key from https://stitch.withgoogle.com under your project settings.

## Screens

The `stitch-screens/` directory contains the exported HTML for each page:

| File | Page |
|------|------|
| 01-catholic-owned-homepage.html | Homepage / landing page |
| 03-the-marketplace-b.html | Marketplace browse/shop |
| 06-trusted-partners-directory-b.html | Business directory listing |
| 08-product-detail-gilded-duo-tone-bible.html | Product detail page |
| 11-sacred-craft-studios-c.html | Vendor storefront |
| 12-lux-aeterna-directory.html | Individual business listing |
| 14-lux-aeterna-detail-b.html | Business detail page |
| 16-sacred-exchange-barter-b.html | Barter & trade |
| 18-speed-networking-b.html | Events / networking |
| 20-shopping-cart-b.html | Shopping cart |
| 22-gift-registries-a.html | Gift registry dashboard |

The `stitch-screens-original/` directory contains the unmodified exports from Stitch for reference.

## Mobile Screens

The `stitch-screens-mobile/` directory contains mobile/native app versions of each page, all featuring a fixed 5-button bottom navigation bar (Shop, Directory, Events, Barter, Registry):

| File | Page |
|------|------|
| 01-mobile-homepage.html | Mobile homepage |
| 03-mobile-marketplace.html | Mobile marketplace browse |
| 06-mobile-directory.html | Mobile business directory |
| 08-mobile-product-detail.html | Mobile product detail |
| 11-mobile-vendor-storefront.html | Mobile vendor storefront |
| 12-mobile-business-listing.html | Mobile business listing |
| 14-mobile-business-detail.html | Mobile business detail |
| 16-mobile-barter-trade.html | Mobile barter & trade |
| 18-mobile-events.html | Mobile events & networking |
| 20-mobile-shopping-cart.html | Mobile shopping cart |
| 22-mobile-gift-registries.html | Mobile gift registry dashboard |

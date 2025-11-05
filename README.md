# Outlight API Documentation - Mintlify

This is the Mintlify documentation for the Outlight API, providing comprehensive guides and references for tracking and analyzing cryptocurrency token calls across social media channels.

## 📚 Documentation Structure

```
mintlify-docs/
├── mint.json                 # Mintlify configuration
├── introduction/
│   ├── welcome.mdx          # Welcome page
│   └── quickstart.mdx       # Quick start guide
└── api-reference/
    ├── introduction.mdx      # API overview
    ├── authentication.mdx    # Authentication guide
    ├── channels/            # Channel endpoints
    │   ├── search-channels.mdx
    │   ├── list-channels.mdx
    │   ├── channel-details.mdx
    │   └── channel-calls.mdx
    ├── tokens/              # Token endpoints
    │   ├── search-tokens.mdx
    │   ├── recent-tokens.mdx
    │   ├── most-called-tokens.mdx
    │   └── token-details.mdx
    └── models/              # Data models
        ├── channel.mdx
        ├── token.mdx
        └── responses.mdx
```

## 🚀 Quick Start

### Prerequisites

- Node.js 18.x or higher
- npm or yarn

### Installation

1. Install Mintlify CLI:
```bash
npm i -g mintlify
```

2. Navigate to the documentation directory:
```bash
cd mintlify-docs
```

3. Run the documentation locally:
```bash
mintlify dev
```

The documentation will be available at `http://localhost:3000`.

## 📝 Configuration

The main configuration file is `mint.json`, which includes:

- **Navigation structure** - Sidebar organization
- **API settings** - Base URL and authentication methods
- **Styling** - Colors, logos, and themes
- **Features** - Search, analytics, etc.

## 🎨 Customization

### Update Colors

Edit the `colors` section in `mint.json`:

```json
"colors": {
  "primary": "#0D9373",
  "light": "#07C983",
  "dark": "#0D9373"
}
```

### Add Logo

Place your logo files in the root directory and update `mint.json`:

```json
"logo": {
  "dark": "/logo/dark.svg",
  "light": "/logo/light.svg"
}
```

### Modify Navigation

Update the `navigation` array in `mint.json` to add or reorganize pages:

```json
"navigation": [
  {
    "group": "Your Group",
    "pages": [
      "path/to/page1",
      "path/to/page2"
    ]
  }
]
```

## 📦 Deployment

### Deploy to Mintlify

1. Create an account at [mintlify.com](https://mintlify.com)
2. Connect your GitHub repository
3. Mintlify will automatically deploy your documentation

### Manual Deployment

```bash
mintlify deploy
```

## 🔧 API Information

- **Base URL**: `https://prod.api.sauron.outlight.fun`
- **Version**: 1.0.0
- **Authentication**: Currently public (no auth required)

## 📚 Key Features

- **Channel Analytics** - Track channel performance and metrics
- **Token Tracking** - Monitor token calls and performance
- **Real-time Data** - Access up-to-date market information
- **Historical Analysis** - Review performance over multiple timeframes

## 🛠 Development

### Adding New Endpoints

1. Create a new `.mdx` file in the appropriate directory
2. Use the frontmatter format:
```mdx
---
title: 'Endpoint Name'
api: 'METHOD /api/path'
description: 'What this endpoint does'
---
```

3. Add the page to `navigation` in `mint.json`

### Writing Documentation

- Use MDX format (Markdown with JSX)
- Include code examples in multiple languages
- Add request/response examples
- Document all parameters and fields

## 📊 Available Endpoints

### Channels
- `GET /api/channels/search` - Search channels
- `GET /api/channels` - List channels with pagination
- `GET /api/channels/{channelId}/info` - Get channel details
- `GET /api/channels/{channelId}/calls` - Get channel calls

### Tokens
- `GET /api/tokens/search` - Search tokens
- `GET /api/tokens/recent` - Get recent tokens
- `GET /api/tokens/most-called` - Get most called tokens
- `GET /api/tokens/{address}` - Get token details

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📝 License

This documentation is provided for the Outlight API.

## 🔗 Links

- [API Base URL](https://prod.api.sauron.outlight.fun)
- [Mintlify Documentation](https://mintlify.com/docs)
- [OpenAPI Specification](https://mintlify.com/docs/api-playground/openapi)


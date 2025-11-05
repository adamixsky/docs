---

# Outlight.fun API Documentation

Welcome to the source code repository for the official Outlight.fun API documentation. This site is built with [Mintlify](https://mintlify.com).

## 🚀 Running Locally

To run the development server and preview the documentation locally:

1.  **Prerequisites**: Ensure you have [Node.js](https://nodejs.org/) version 18.x or higher installed.

2.  **Install the Mintlify CLI**:
    ```bash
    npm install -g mintlify
    ```

3.  **Run the development server**:
    ```bash
    mintlify dev
    ```

    The documentation will be available at `http://localhost:3000`. Changes to `.mdx` files will be hot-reloaded.

## 📁 Project Structure

The key files and directories in this project are:

```
.
├── mint.json                 # Main config file (navigation, colors, etc.)
├── introduction/
│   ├── welcome.mdx           # Welcome page
│   └── quickstart.mdx        # Quickstart guide
└── api-reference/
    ├── introduction.mdx      # API Introduction
    ├── authentication.mdx    # Authentication & Rate Limiting
    ├── channels/             # Channel Endpoints
    │   ├── search-channels.mdx
    │   ├── list-channels.mdx
    │   ├── channel-details.mdx
    │   └── channel-calls.mdx
    ├── tokens/               # Token Endpoints
    │   ├── search-tokens.mdx
    │   ├── recent-tokens.mdx
    │   ├── most-called-tokens.mdx
    │   └── token-details.mdx
    └── models/               # Centralized Data Models
        ├── channel-models.mdx
        ├── token-models.mdx
        └── response-models.mdx
```

## ✍️ How to Contribute

To add a new page or modify an existing one:

1.  **Create or Edit a File**: Find the relevant directory (e.g., `api-reference/channels`) and create or edit a `.mdx` file.

2.  **Use Frontmatter**: Each endpoint documentation page should start with a frontmatter block:
    ```mdx
    ---
    title: 'Endpoint Name'
    api: 'METHOD /api/path'
    description: 'A brief description of what this endpoint does.'
    ---
    ```

3.  **Update Navigation**: If you add a new page, you must add its path to the `navigation` array in `mint.json` for it to appear in the sidebar.

## 📦 Deployment

This documentation is connected to the Mintlify platform. Every push to the main branch (e.g., `main` or `master`) will automatically trigger a new build and deploy the updated site.
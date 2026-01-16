---
description: How to deploy the Astro site to Cloudflare Pages
---

You have two main ways to deploy to Cloudflare Pages: via Git integration (recommended) or using the Wrangler CLI.

### Option 1: Git Integration (Recommended)
This method automatically deploys your site whenever you push to your Git repository.

1.  **Push your code** to a GitHub/GitLab repository.
2.  Log in to the **Cloudflare Dashboard** and go to **Compute (Workers & Pages)** > **Pages**.
3.  Click **Connect to Git**.
4.  Select your repository or specific branch.
5.  In the "Build settings":
    *   **Framework preset**: Select `Astro`.
    *   **Build command**: `npm run build`
    *   **Build output directory**: `dist`
6.  Click **Save and Deploy**.

### Option 2: Wrangler CLI (Direct Upload)
This method uploads your local `dist` folder directly to Cloudflare.

1.  Install Wrangler (if not already installed):
    ```powershell
    npm install -g wrangler
    ```
2.  Authenticate with Cloudflare:
    ```powershell
    npx wrangler login
    ```
3.  Build your project locally:
    ```powershell
    npm run build
    ```
4.  Deploy the `dist` folder:
    ```powershell
    npx wrangler pages deploy dist --project-name delio-site
    ```
    (You can change `delio-site` to whatever name you want for your project).

### Configuration (Optional)
If you plan to use Server-Side Rendering (SSR) features in the future, you should install the official adapter:

```powershell
npx astro add cloudflare
```
This will update your `astro.config.mjs` automatically. For this purely static site, it is not strictly required but recommended for future-proofing.

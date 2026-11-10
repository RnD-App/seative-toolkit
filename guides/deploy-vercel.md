# Deploy on Vercel (default)

Vercel makes Next.js, so it is our default host. seaMotion is hosted there too.

## First deploy
1. Push the site to a GitHub repo in our org.
2. On [vercel.com](https://vercel.com): **Add New > Project**, import the GitHub repo. Next.js is detected.
3. If the app is in a subfolder (like seaMotion's `seaMotion/`), set **Root Directory** to that folder.
4. Add environment variables (copy the names from `.env.example`).
5. Deploy.

## Every day
- Every pull request gets its own **preview URL**. Paste it in the PR and review the site there.
- Merging to `main` deploys to production.
- Custom domain: Project > Settings > Domains, then follow the DNS steps it shows.

## Tips
- If a build fails on Vercel but works locally, check the Node.js version (Project > Settings) matches `.nvmrc`.
- Never put secrets in code; only in Vercel's environment variables.

Before launch: [deploy-checklist.md](deploy-checklist.md).

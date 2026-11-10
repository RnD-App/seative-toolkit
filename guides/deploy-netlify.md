# Deploy on Netlify

Use Netlify when a client already hosts there or needs its forms or functions. Otherwise use [Vercel](deploy-vercel.md).

## First deploy
1. Push the site to a GitHub repo in our org.
2. On [netlify.com](https://www.netlify.com): **Add new site > Import an existing project**, pick the GitHub repo.
3. Netlify detects Next.js and fills in the build settings. Check the build command is `next build` (or `npm run build`).
4. Add environment variables from `.env.example`.
5. Deploy.

## Every day
- Pull requests get **Deploy Previews**; paste the link in the PR.
- Merging to `main` deploys to production.

## Tips
- Set the Node.js version to match `.nvmrc` (Site configuration > Build & deploy > Environment).
- Some newer Next.js features can arrive on Netlify later than on Vercel. Check
  [Netlify's Next.js docs](https://docs.netlify.com/frameworks/next-js/overview/) if something behaves differently.

Before launch: [deploy-checklist.md](deploy-checklist.md).

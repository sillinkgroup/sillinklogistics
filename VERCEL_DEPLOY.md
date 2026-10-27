# Sillink Logistics — Vercel deployment

## Important: GitHub deployment

The Vercel error `Couldn't find any pages or app directory` means the GitHub repository being deployed did not contain the Next.js source tree at its repository root. It contained the ZIP file instead.

The repository root **must directly contain**:

- `app/`
- `components/`
- `lib/`
- `public/`
- `package.json`
- `next.config.ts`
- `tsconfig.json`
- `vercel.json`

Do **not** upload this ZIP as a single file into GitHub and expect Vercel to extract it. Extract the ZIP first, then upload/commit the extracted files and folders to the root of the repository.

## Vercel settings

- Framework Preset: Next.js
- Root Directory: `.`
- Install Command: `npm install`
- Build Command: `npm run build`
- Output Directory: leave blank/default

After pushing the extracted project to `main`, redeploy the latest commit.

## Local test

```bash
npm install
npm run build
npm run start
```

The project uses the Next.js App Router. The TypeScript path alias `@/*` is configured in `tsconfig.json`.

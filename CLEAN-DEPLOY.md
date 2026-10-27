# Sillink Logistics — Clean Vercel Deployment

This version intentionally uses **zero `@/` import aliases**. Every internal import is relative, so the build does not depend on tsconfig path-alias resolution.

## Important: replace the old repository
Do not merge this into the old Sillink repository files. The previous repository contains an old `app/dashboard/page.tsx` that imports `@/lib/data`, which is the source of the reported error.

1. Open the GitHub repository.
2. Delete the old repository contents (especially the old `app/` directory, `components/`, `lib/`, `tsconfig.json`, and old config files).
3. Upload the **contents of this ZIP**, not the ZIP file itself.
4. The GitHub root must directly contain `app/`, `components/`, `lib/`, `public/`, `package.json`, `tsconfig.json`, and `next.config.ts`.
5. In Vercel, set Root Directory to `.` and deploy the repository.

## Build settings
- Framework: Next.js
- Root Directory: `.`
- Install Command: `npm install`
- Build Command: `npm run build`

## Verification
There should be no source import beginning with `@/`. The dashboard uses `../../lib/data` instead.

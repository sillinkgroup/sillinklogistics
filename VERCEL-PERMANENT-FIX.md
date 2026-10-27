# Sillink Logistics Vercel Permanent Build Fix

The GitHub repository currently stores the application source inside `Sillink-Logistics-Vercel.zip` instead of exposing `app/` at repository root.

This package fixes that without requiring Vercel to have an `app/` directory before the build starts. The `npm run build` script first extracts `Sillink-Logistics-Vercel.zip` into the repository root, then runs `next build`.

## Deploy

Replace the root `package.json` in GitHub with the package.json in this folder. Keep `Sillink-Logistics-Vercel.zip` in the repository root. Then redeploy Vercel.

The build command must remain:

`npm run build`

Do not set a custom Root Directory.

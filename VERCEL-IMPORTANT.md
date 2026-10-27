# IMPORTANT: Vercel / GitHub deployment

The Next.js project MUST be uploaded with the `app/` folder at the repository root.

Correct GitHub repository root:

```
app/
components/
lib/
public/
package.json
next.config.ts
tsconfig.json
vercel.json
```

Do NOT upload only `package.json`, `next.config.ts`, etc. and leave `app/` inside a ZIP file.
Vercel does not unzip repository files during a normal Git deployment.

## If using the GitHub website

1. Download and extract this project ZIP on your computer.
2. Open the extracted project folder.
3. Select the CONTENTS of that folder, including the `app`, `components`, `lib`, and `public` folders.
4. Upload those contents to the ROOT of `sillinkgroup/sillinklogistics`.
5. Delete the old `Sillink-Logistics-Vercel.zip` from the GitHub repository.
6. In Vercel, Project Settings -> General -> Root Directory must be `.` (repository root).
7. Redeploy the latest commit.

## Recommended build settings

Framework Preset: Next.js
Build Command: `npm run build`
Install Command: `npm install`
Output Directory: leave blank / automatic
Root Directory: `.`

This project uses Next.js 16.4.3, a current 16.x release.

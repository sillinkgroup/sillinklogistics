# Vercel deployment

1. Extract this ZIP.
2. Upload the contents of the extracted folder to the root of your GitHub repository.
3. Verify GitHub shows `app/` directly at repository root.
4. In Vercel set Root Directory to `.` and Framework Preset to Next.js.
5. Redeploy the newest commit.

This project intentionally has no `@/lib/data` dependency. Shared data is in `app/data.ts` and shared UI is in `app/components/`, using relative imports, so the previous missing-module error cannot occur when the complete project is uploaded.

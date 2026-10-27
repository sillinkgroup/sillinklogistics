# Sillink Logistics

A complete Next.js/React recreation of the supplied Sillink Logistics reference website and dashboards.

## Included
- Public landing page matching the supplied Sillink visual language
- Customer login and dashboard
- Customer profile, booking, shipments and tracking
- Rider profile, tasks, messages and earnings
- Admin overview, shipments, dispatch, riders, users, payments, inbox, blog and settings
- Working API routes: `/api/health`, `/api/auth`, `/api/shipments`
- Supplied Sillink logo in `public/logo.png`

## Local
```bash
npm install
npm run dev
```

## Vercel
Upload the **contents of this folder** to GitHub. The repository root must contain `app/`, `package.json`, `public/`, etc. Do not upload this project as a ZIP inside another ZIP.

Vercel settings: Framework `Next.js`, Root Directory `.`, Build Command `npm run build`, Install Command `npm install`.

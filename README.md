# Sillink Logistics

React/Next.js recreation of the Sillink Logistics website and the customer, rider and admin dashboards from the supplied reference screenshots and public Base44 URL.

## Run locally

```bash
npm install
npm run dev
```

Open http://localhost:3000.

## Demo login

Go to `/login`. Enter any email/password and choose Customer, Rider, or Admin. The role determines the dashboard.

## Included routes

- `/` public marketing site
- `/login` role-aware login
- `/dashboard` customer dashboard
- `/customer/book`, `/customer/track`, `/customer/shipments`, `/customer/profile`
- `/rider/profile`, `/rider/tasks`, `/rider/messages`, `/rider/earnings`
- `/admin/profile`, `/admin/overview`, `/admin/inbox`, `/admin/shipments`, `/admin/dispatch`, `/admin/riders`, `/admin/users`, `/admin/payments`, `/admin/blog`, `/admin/settings`
- `/api/auth`, `/api/shipments`, `/api/health`

## Vercel

This is a Next.js project. Upload the ZIP to Vercel or import the folder/repository. Vercel will detect Next.js and use the included build configuration.

### Important backend note

The API routes are implemented as Vercel-compatible serverless endpoints. The demo data is in code and POST-created shipments are not persistent across serverless invocations. For production persistence, connect a database such as Vercel Postgres/Neon/Supabase and replace the data layer in `lib/data.ts` and `app/api/shipments/route.ts`.

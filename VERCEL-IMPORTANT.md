# Vercel Production Setup

This is a PHP application, not a Next.js application. **Do not select Next.js and do not use `npm run build`.**

Vercel supports PHP through the `vercel-php` runtime. This project declares `vercel-php@0.9.0` in `vercel.json`.

## Required environment variables
Set these in Vercel → Project Settings → Environment Variables:

`APP_KEY` = a long random secret (32+ characters)

`DB_DRIVER` = `mysql`
`DB_HOST` = your MySQL host
`DB_PORT` = `3306`
`DB_NAME` = `sillink`
`DB_USER` = your MySQL username
`DB_PASS` = your MySQL password

Then import `database/schema.sql` into that MySQL database.

## Repository root
The GitHub repository root must contain:

- `api/index.php`
- `lib/`
- `public/`
- `database/schema.sql`
- `vercel.json`

Do not put the project inside another folder or upload the ZIP itself as a repository file.

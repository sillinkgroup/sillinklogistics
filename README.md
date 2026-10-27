# Sillink Logistics — PHP + MySQL Vercel Build

Rebuilt from the supplied Sillink screenshots and the live Base44 reference. The application includes the public homepage, customer portal, rider portal, admin portal, authentication, shipment booking/tracking, pricing/admin screens, light/dark mode and customer↔admin chat.

## Vercel
Vercel supports PHP through the `vercel-php` runtime. This project uses `vercel-php@0.9.0` for `api/*.php`.

Set these Vercel environment variables for production:
- `DB_DRIVER=mysql`
- `DB_HOST`
- `DB_PORT=3306`
- `DB_NAME`
- `DB_USER`
- `DB_PASS`

Import `database/schema.sql` into your MySQL database first.

## Demo accounts
- Admin: `admin@sillinklogistics.com` / `Admin@12345`
- Customer: `emmanuel@sillinklogistics.com` / `Customer@12345`
- Rider: `rider@sillinklogistics.com` / `Rider@12345`

Change these passwords before production.

## Local test
PHP 8.4+ is recommended:
`php -S 127.0.0.1:8080 api/index.php`

Without MySQL environment variables, the app automatically uses a SQLite database under `/tmp` and seeds the demo data.

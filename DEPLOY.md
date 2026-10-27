# Deployment checklist

1. Create/import the MySQL database using `database/schema.sql`.
2. Push the contents of this folder to the ROOT of your GitHub repository.
3. Import that repository into Vercel.
4. Root Directory must be `.`.
5. Add the database environment variables from `.env.example` in Vercel.
6. Deploy.
7. Open `/login` and test customer, rider and admin accounts.
8. Test customer chat, then open Admin → Inbox in another browser/session and reply.
9. Test booking and tracking.
10. Enable Vercel protection/auth as appropriate for your production environment.

Do not upload a ZIP file inside another ZIP or leave the old Next.js project files in the repository.

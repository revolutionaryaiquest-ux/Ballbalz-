BOOKBALLZ - DEPLOY ON CLOUDFLARE PAGES

ZIP CONTENTS (all at the top level, do not nest in a folder):
  index.html    the whole website (shop, checkout, reviews, admin panel)
  _worker.js    the backend (orders, downloads, Telegram, email, share previews)

DEPLOY
1. Cloudflare dashboard > Workers & Pages > Create > Pages > Upload assets (NOT "Create Worker").
2. Name the project, upload THIS ZIP, click Deploy.
3. Project > Settings > Variables and Secrets. Add these two (mark the key as Secret):
   SUPABASE_URL          = https://ztzanusseipjrxbkmblr.supabase.co
   SUPABASE_SERVICE_KEY  = your Supabase service_role / secret key
4. Upload the zip again (new deployment) so the variables take effect.
5. Open https://YOURPROJECT.pages.dev/#/admin and log in with your admin email.
6. Admin > Telegram: paste bot token, Find my chat ID, Save, Send test message.
7. Admin > Email (optional): paste Resend API key and From address.
8. Admin > Settings: set the announcement bar, WhatsApp number, bank details.
9. Admin > Books: add your book with a category, cover and PDF.

IF YOU SEE A 404
- Use the project's main address (xxxx.pages.dev), not a path like /home.
- Re-upload the ORIGINAL zip. Do not unzip and re-zip it inside an extra folder.
- Make sure you created a Pages project (Upload assets), not a Worker.
- Pages > your project > Deployments: open the latest one and confirm it says Success.

DRIPHOUSE WEBSITE UPDATE V2

FILES
- index-v2.html: English storefront
- index-ar-v2.html: Arabic-first RTL storefront
- admin-v2.html: redesigned admin dashboard with product detail editor
- driphouse_update_v2.sql: additive Supabase migration

UPDATES
- Clicking a product opens its detail view: product image, optional gallery, subtitle, full description, specifications, price, stock, quantity and Add to cart.
- Admin can create products and edit detail page subtitle, full details, specifications, primary image and gallery URLs.
- Hero uses a genuine Vaporesso LUXE X2 product render from Vaporesso's official product listing. It is a real product render, not a custom-created 3D model.
- Header uses a Profile icon and Cart label instead of Bag.
- Customer account page supports sign-up, sign-in and password reset. Sign-up requires email confirmation before sign-in/checkout.
- Checkout requires confirmed account email, Egyptian mobile number, Egypt governorate, city/district and street/building details. Database rules also restrict new orders to confirmed users and Egyptian governorates/phone patterns.

INSTALL
1. Back up Supabase.
2. Run driphouse_update_v2.sql in Supabase SQL Editor after the original driphouse_database.sql.
3. Supabase Dashboard > Authentication > Providers: enable Email signups and keep Confirm email enabled.
4. Configure production SMTP in Authentication > SMTP Settings using a verified sender domain (Resend is supported). Supabase default SMTP is restricted and is not suitable for general customer delivery.
5. Authentication > URL Configuration: set the live Site URL and add the live website URL to Redirect URLs.
6. Upload index-v2.html as index.html (or index-ar-v2.html as index.html for Arabic-first), and admin-v2.html as admin.html.
7. Keep the existing admin profile role check.

IMPORTANT
- A website cannot reliably ask Google/Gmail whether an arbitrary mailbox exists. Supabase email confirmation is the meaningful check: the customer must receive and click a confirmation link. Actual delivery depends on SMTP being correctly configured and the sender domain verified.
- The form and database validate Egypt governorate, city/street fields and mobile-number format. They cannot prove that a street address exists or that a SIM is active; delivery staff should confirm exact location/phone.
- Hero image is remotely hosted by Vaporesso and may be blocked by hotlink rules. Replace it with a locally hosted licensed product render if necessary. Confirm the pictured model matches the device actually being sold.
- Google OAuth is not enabled: it requires your Google OAuth Client ID/Secret configured in Supabase. The email/password flow uses inbox confirmation instead.
- I cannot access your Supabase dashboard or send a real test email from this environment, so live auth, SMTP delivery, database writes and checkout are not claimed to be verified. HTML/JavaScript syntax has been checked locally.

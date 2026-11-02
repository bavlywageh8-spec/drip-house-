DRIPHOUSE V5

UPLOAD (replace the old files)
- index.html  -> storefront. New photo hero (the hero image is embedded inside the file, nothing else to upload).
- admin.html  -> redesigned admin dashboard
- driphouse_update_v2.sql -> no change, keep what you already ran.

WHAT CHANGED
Storefront
- Hero now uses your photo (device + smoke) with the headline over it. The 01/02/03 stats are removed.
Admin
- New layout: icon sidebar, top search bar, 3 stat cards, sales chart (hover for tooltip, 7/14/30 days),
  payment-methods donut, inventory alerts, top-selling products, top governorates, recent orders.
- Orders: separate Customer, Phone and Email columns (phone and email are tap-to-call / tap-to-mail),
  plus city + governorate under the address.
- Products: the old "Edit product details" box is removed. Each catalogue row has a Details button
  (subtitle, description, full details, specifications, gallery URLs).
- Save messages now show at the top (green = saved, red = error) and report when nothing was really saved.
- The dashboard is zoomed out to about 84% (change --z:.84 at the top of admin.html to adjust).
- Catalogue: the Save button is hidden until you change a price, discount or stock value. It disappears
  again after saving, or if you type the original value back. Pressing Enter in a field also saves.

NOTE
- "Top selling products" reads the order_items table. If the admin account is not allowed to read it,
  that card just stays empty (everything else still works).
- Before publishing, remember: const INSTAGRAM_URL='' in index.html.

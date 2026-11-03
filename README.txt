DRIPHOUSE V8

UPLOAD (replace the old files)
- index.html  -> storefront
- admin.html  -> admin dashboard
- driphouse_update_v4.sql -> RUN ONCE in Supabase > SQL Editor > New query > Run (safe to run again)
  (run driphouse_update_v3.sql and driphouse_support_chat.sql first if you have not yet)

WHAT IS NEW
Admin
- Messages page restyled like your mockup (glow frame, swoosh background, paperclip + Send bar).
- Catalogue page like your mockup: number boxes with arrows, Details / Delete, Showing N products, page arrows.
  "Add product" button top right opens the new Add Product page (drag & drop image, description 0/1000).
- Promo codes now sit UNDER the Catalogue: Code, percent/fixed, Value, Maximum Uses, End date. Details edits a code
  (also the minimum cart total and Pause / Activate). USED shows e.g. 12 / 50. A code stops working when used up.
- Overview dashboard laid out like your screenshot (Total revenue / Total orders / Products, Sales performance,
  Payment methods, Inventory alerts, Top selling).
- Details button on every product now works (it had no code before): image, subtitle, description, gallery,
  specifications and COLOURS & SKINS.
- Orders table now has an Items column, so you can see which colour each customer chose.
Colours & skins
- Details > "+ Add colour / skin": name, optional colour dot, optional picture (upload or link).
  0 rows = no colour choice. 1 row = shown as an edition label. 2+ rows = customer picks; the picture changes.
Storefront
- Cards like your reference: heart, grey "Sold out" badge + grey button, red -10% badge, struck-through old price
  in grey and new price in red, gold Add to cart. Prices on cards read "60 L.E.".
- Phone and tablet show the full desktop layout (viewport is fixed at 1280px). Pinch to zoom.

V9
- driphouse_fix_orders.sql -> RUN ONCE in Supabase (fixes "Could not find the 'city' column of 'orders'").
  The new index.html also keeps checkout working if a column is missing, but run the SQL so name, governorate
  and city are saved with every order.
- Product cards, + / Add to cart buttons, hearts, cart button and profile button now animate on hover and tap.
- Place order: the delivery truck drives to the right while the order is sent.
- Empty cart shows only the message. The Discount row appears only when a promo code is applied or an item has a discount.
- New Log in / Sign up page (profile icon). When logged in the same page shows your email and Log out.
  Checkout needs a logged-in, email-confirmed account; after logging in, checkout opens automatically.

V10
- Admin size is back to 100% (same as your dashboard screenshot) - this also fixes the short left sidebar.
- Products page: Add Product form is now ABOVE the Catalogue, then Catalogue, then Promo codes.
- Catalogue fits the screen (no cut-off Action column). New Photo column: press "Change" (or "Add") under a
  product picture to upload a new image from your phone/computer. It saves straight away.

V11
- driphouse_update_v5.sql -> RUN ONCE in Supabase > SQL Editor (creates the delivery fee setting).
- Admin > Products (bottom, under Promo codes): "Delivery fee (L.E.)" + Save fee. The shop reads it automatically
  and adds it to every order. 0 = free delivery (the cart shows "Free").
- index.html: the delivery fee is no longer hard-coded; it comes from the admin setting.

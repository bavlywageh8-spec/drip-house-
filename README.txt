DRIPHOUSE V7

UPLOAD (replace the old files)
- index.html  -> storefront (now has a promo code box in the cart)
- admin.html  -> admin dashboard
- driphouse_update_v3.sql -> RUN ONCE in Supabase > SQL Editor > New query > Run (safe to run again)
  It fixes the missing 'details' / 'discount_percent' columns, creates the image uploads (products + categories),
  allows the order statuses Pending / Completed / Delivered / Cancelled, and creates promo codes.
- driphouse_support_chat.sql -> run once if you have not yet (fixes the Support chat). Also enable
  Authentication > Sign In / Providers > Allow anonymous sign-ins.

WHAT IS NEW
- Dashboard laid out like your reference: Total sales / Total orders / Customers, Sales performance + Payment methods.
- Add a product: simple form with Discount and Details, and a Gallery button to upload the picture from your phone/computer.
- Details button on every catalogue row: change main image, extra gallery images, subtitle, specs.
- Orders: choose Pending / Completed / Delivered / Cancelled.
- Promo codes page (tag icon): New promo code (percent or fixed, minimum total, end date). Customers enter the code in the cart.
- Category images page (picture icon).
- Admin zoomed in a little (change --z:1.1 at the top of admin.html).

V7
- Cart drawer, checkout form and admin Messages page restyled to match the new mockups.
- Delivery fee: in index.html find  const DELIVERY_FEE=0;  (0 shows "Free"; set 50 for L.E 50 on every order).
- Messages: refreshes itself every 8 seconds; a mint dot means the customer is waiting for your reply.

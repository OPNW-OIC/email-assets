# OPNW email assets

Public image hosting for OPNW's Klaviyo email campaigns.

Klaviyo can only import images from a public URL. Images pushed here are imported into Klaviyo from:

```
https://raw.githubusercontent.com/OPNW-OIC/email-assets/main/<path>
```

Once imported, Klaviyo keeps its own copy on its CDN, so files here can be removed later without breaking emails that were already sent.

## Layout

- `promo/YYYY-MM-<slug>.jpg` — flyer images for "Promo …" campaigns (1200px wide JPG)

## For Claude agents

The full campaign workflow (cloning the last promo, editing the template, copy style, scheduling rules) lives in the Claude skill **`opnw-klaviyo-promo-email`**. Load that skill instead of starting from scratch. In short:

1. Convert the flyer PDF to a 1200px JPG.
2. Commit it to `promo/` here and push to `main`.
3. Import it into Klaviyo with the raw URL above.
4. Build the campaign per the skill. Never schedule or send without explicit approval.

## Notes

- This repo is **public**. Only put content here that is already going out to customers.
- No credentials, customer data, or internal documents.

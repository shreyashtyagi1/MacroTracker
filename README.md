# MacroTrack — iPhone installable nutrition tracker

## Features
- Daily calories, protein, carbs, fat, and configurable goals
- Search packaged foods online using the Open Food Facts public database
- Look up a packaged product by entering its barcode digits
- Tracks fibre, sugar, sodium, calcium, iron, and potassium when the database has values
- Manual food entry when a product is missing
- Local device storage and JSON export
- Home-screen web app support (PWA)

## Install on iPhone
This is a Progressive Web App, not an App Store IPA. iOS can install it to the Home Screen once it is served from an HTTPS website.

1. Upload the contents of this folder to a static host with HTTPS, such as GitHub Pages or Netlify.
2. Open the resulting HTTPS URL in **Safari** on your iPhone.
3. Tap **Share** → **Add to Home Screen** → **Add**.
4. Launch MacroTrack from the new Home Screen icon.

Do not open `index.html` directly from the Files app if you want installation/offline support. A secure HTTPS host is required for the service worker.

## Food data and accuracy
- Uses the Open Food Facts API: https://world.openfoodfacts.org/
- Coverage varies by product and country; not every Indian product has a record or complete micronutrients.
- Product values are scaled from per-100 g nutrient fields. The app asks for the grams consumed.
- Verify against the physical label if the database entry is missing or looks wrong.
- Your diary and goals are stored in this browser's local storage; there is no account/cloud sync. Clearing Safari website data can erase the diary, so export a backup occasionally.

## Current limitations
- Barcode input is manual, not camera scanning.
- This is a first working prototype; it does not yet include accounts, cloud sync, recipe builder, restaurant database, or health-professional validation.

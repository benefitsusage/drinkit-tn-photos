# drinkit-tn-photos

Bottle photos for the Drinkit.tn app, served as static files by GitHub Pages.

- `index.json`: `{ version, updatedAt, count, photos: { "<TASMAC productId>": "p/<file>.jpg" } }`
- `p/*.jpg`: one small JPEG (at most 360 px) per distinct photo

The photos are the ones bottle suppliers upload to TASMAC (`liquor/get-productListByBrand` on TASMAC's public API).
A photo uploaded for one size is also listed for the bottle's other sizes. Bottles without a photo show a category
tile in the app.

## Refresh

From the `drinkit-tn` app repo, on a Mac:

```sh
npm run photos:sync            # rewrites this folder (about 3 minutes)
npm run photos:sync -- --push  # …then commits and pushes it
```

Nothing here is edited by hand.

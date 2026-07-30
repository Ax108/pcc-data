# pcc-data

Static media for [Pratima Chandra Foundation](https://pratimachandrafoundation.org/) — images, PDFs, and related files served from a separate host.

## Layout

```
assets/
├── documents/       # application PDFs
├── events/          # event galleries (by year: 2016, 2017, …)
├── gallery/         # site gallery + home teasers
├── hero/
├── home/            # hero slides, posters
├── logo/
├── our-inspiration/
└── partners/
```

Paths in the React app are relative to this folder once hosted:

`https://ax108.github.io/pcc-data/assets/logo/logo-header.png`

## App wiring

The Vite app (`pcc-foundation`) reads `VITE_ASSET_BASE_URL`. When empty, local
dev serves this folder via middleware. When set, all `assetUrl(...)` calls and
HTML preloads use that base.

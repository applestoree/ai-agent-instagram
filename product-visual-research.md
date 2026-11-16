# Product Visual Data — Research & Change Log

Status: Implemented in `products.csv`  
Research policy: official Apple sources only  
Scope: existing 25 product rows; no product rows added or removed.

## Decisions applied

- Removed `Official Product Images` from `products.csv`.
- Added 18 common visual fields, including seven distinct product-view fields (Front, Rear, Left, Right, Top, Bottom, Perspective) and `Detail Close-up`.
- Added category-specific fields for iPhone, iPad, Mac and Apple Watch in one shared CSV header.
- Added `Included Components` and `Compatible Accessories` as separate fields.
- Kept one row per model; color finishes are described separately inside `Color & Finish`.
- Kept `Starting Price (MYR)` and all other pre-existing product fields unchanged.
- Used `Not Available` where a visual attribute could not be verified from the reviewed official source extracts, and `Not Applicable` for category-irrelevant fields.
- Did not store product-image URLs in the CSV. Official Apple imagery may be consulted as a visual research/reference source for later image-generation workflows.
- No Product Name or Model identity correction was necessary among the reviewed records; existing identity strings were retained.

## Official source register

The following Apple sources were used to verify product names and available visual/specification attributes. A source may support only the attributes explicitly stated on that page; it does not imply that every visual field for that product was verified.

### iPhone
- iPhone 17 Pro — https://support.apple.com/id-id/125090
- iPhone Air — https://www.apple.com/my/iphone-air/specs/
- iPhone 17 — https://www.apple.com/my/iphone-17/specs/
- iPhone 17e — https://www.apple.com/my/iphone-17e/specs/
- iPhone Duo — https://www.apple.com/my/iphone-duo/specs/
- iPhone 18 Pro and iPhone 18 Pro Max — https://www.apple.com/my/iphone-18-pro/specs/
- iPhone Malaysia lineup and availability cross-check — https://www.apple.com/my/shop/buy-iphone

### iPad
- iPad Pro 11-inch and 13-inch — https://www.apple.com/my/ipad-pro/specs/
- iPad Air 11-inch and 13-inch — https://www.apple.com/my/ipad-air/specs/
- iPad (A16) — https://www.apple.com/my/ipad-11/specs/
- iPad mini — https://www.apple.com/my/ipad-mini/specs/
- iPad (A16) Apple Support technical specifications — https://support.apple.com/id-id/122240

### Mac
- MacBook Neo — https://www.apple.com/my/macbook-neo/specs/
- MacBook Air 13-inch (M5) — https://support.apple.com/id-id/126320
- MacBook Pro 14-inch (M6) — https://support.apple.com/en-euro/148300
- iMac — https://www.apple.com/my/imac/specs/
- Mac mini (M6 / M5 Pro) — https://www.apple.com/my/mac-mini/specs/
- Mac Studio — https://www.apple.com/mac-studio/specs/

### Apple Watch
- Apple Watch Series 12 — https://www.apple.com/my/apple-watch-series-12/specs/
- Apple Watch SE 3 — https://www.apple.com/my/apple-watch-se-3/specs/
- Apple Watch Ultra 4 — https://www.apple.com/my/apple-watch-ultra-4/specs/

## Verification limitations

- Some model-specific official specification pages were not available in the reviewed source set, including some exact 17 Pro Max, 15-inch MacBook Air and 16-inch MacBook Pro details. Those unsupported dimensions, component positions and close-up traits remain `Not Available` rather than inferred.
- Product-image URLs were intentionally excluded from `products.csv`; this file is the separate source register.
- Accessory compatibility and in-box contents are populated only where the reviewed official technical specifications explicitly identify them. Otherwise they remain `Not Available`.
- The source register is not a claim that every row has a complete 360-degree official visual reference. Unverified view-specific details remain clearly marked.

## Validation checklist

- [x] Existing product row count retained: 25.
- [x] Existing `Starting Price (MYR)` field retained.
- [x] `Official Product Images` removed.
- [x] Common visual fields added.
- [x] Category-specific fields added to one shared CSV schema.
- [x] Included components and compatible accessories separated.
- [x] No duplicate CSV header names.
- [x] Unsupported visual details are not fabricated.
- [ ] Future review: refresh source register when Apple updates product pages or introduces new models.

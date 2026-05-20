# SI myMuseum Assets

Static assets repository for the SI myMuseum mobile app.
Images are served via GitHub raw URLs and managed through Firebase Remote Config.

## Folder Structure

```
modals/
├── announcement/   → App update & policy images
├── holiday/        → Seasonal & regional holiday images
└── reminder/       → Reminder modal images
```

## URL Format

```
https://raw.githubusercontent.com/adsglobal/si-mymuseum-assets/main/modals/{folder}/{filename}.png
```

## Usage

All images in this repo are referenced in Firebase Remote Config
under the `app_modals` parameter in the SI myMuseum Flutter app.

## Image Guidelines

| Property          | Value       |
|-------------------|-------------|
| Format            | PNG or WebP |
| Max size          | 500KB       |
| Recommended width | 600px       |
| Aspect ratio      | 16:9 or 4:3 |

## Regions

| Code | Region   |
|------|----------|
| ALL  | Global   |
| KH   | Cambodia |
| MY   | Malaysia |
# Privacy

**Short version: your photos never leave your device.**

DeepParallax is a single web page that runs entirely in your browser. There is no DeepParallax
server, no account, no sign-in, no analytics and no tracking.

## What stays on your device

- **Your photos.** They are opened by your browser and processed on your own computer, phone or
  tablet. They are never uploaded anywhere.
- **Depth maps, videos and still frames you make.** They are created on your device and saved to
  your Downloads folder (or to Photos on iPhone and iPad, if you choose).
- **Your settings.** Only the light/dark choice is remembered, in your browser's own storage.
- **The AI files.** After the first download (or after you choose them by hand), the AI engine and
  model are kept in your browser's storage so they don't have to be downloaded again. You can remove
  them by clearing the website data for the page in your browser settings.

## What the app downloads, and from where

The first time you make a depth map, the browser downloads (and never uploads):

| What | From | About |
|---|---|---|
| Transformers.js (AI toolkit) | cdn.jsdelivr.net | 1 MB |
| ONNX Runtime engine (compatibility mode only) | cdn.jsdelivr.net | 10 MB |
| Depth Anything V2 model | huggingface.co | 99 MB (Standard) or about 390 MB (Detailed) |

Like any website, those services receive an ordinary request from your browser: your internet (IP)
address and browser type. They do not receive your photos or anything you make. Their own privacy
policies apply to those requests:
[jsDelivr](https://www.jsdelivr.com/terms/privacy-policy-jsdelivr-net) and
[Hugging Face](https://huggingface.co/privacy).

If you use the sample scene, or load your own depth map image, nothing is downloaded at all.

## The "Copy a report for Claude" button

The Browser check section can copy a short technical report to your clipboard (browser version,
which drawing system was used, any error messages). It contains no photos and is only shared if you
paste it somewhere yourself.

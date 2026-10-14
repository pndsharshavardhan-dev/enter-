# Bhagavad Gita QR Library — Complete Starter Kit v1.0

## What is included
- `index.html`: responsive mobile-first trilingual web app (Telugu, Hindi, English)
- `chapters.js`: original chapter summaries and editable video/audio URL slots for all 18 chapters
- `manifest.json` and `sw.js`: installable PWA basics and simple cache support
- `sample_booklet.pdf`: printable starter booklet with QR codes and chapter list
- `qr_codes/chapter_01.png` ... `chapter_18.png`: QR codes understood by the app
- `content/`: editable content plan and video plan
- `content_map.csv`: content production tracker

## Run locally on a computer
1. Extract the ZIP.
2. Install Python 3 if needed.
3. Open a terminal/command prompt inside this folder and run: `python -m http.server 8000`
4. Open `http://localhost:8000` in your browser.
5. To test camera QR scanning, use a phone with a hosted HTTPS copy, or test the camera on localhost where supported.

## Easiest Android testing
- Extract the ZIP using your file manager.
- Opening index.html directly may show chapter summaries, but camera scanning can fail because browsers restrict camera access for local files.
- For camera scanning, deploy the folder to an HTTPS static host (e.g. GitHub Pages, Netlify, or Cloudflare Pages) and open the HTTPS URL.
- Tap “Scan QR”, allow camera permission, then scan one of the included chapter QR PNGs printed or shown on another screen.
- Without camera scanning, tap any chapter card.

## Make it a home-screen app
After deploying to HTTPS in Chrome on Android:
1. Open the site.
2. Tap the browser menu (⋮).
3. Choose “Install app” or “Add to Home screen” if available.
4. Launch it from the new icon.

## Connect a video/audio
1. Upload your own or properly licensed MP4/MP3 files to a stable HTTPS host.
2. Open `chapters.js`.
3. For a chapter, fill the correct language URL, e.g. `"video":{"te":"https://your-domain/chapter01-te.mp4","hi":"","en":""}` and/or `"audio":{"te":"https://your-domain/chapter01-te.mp3","hi":"","en":""}`.
4. Keep the chapter `id`, names, and summaries intact. Reload the app to test.
5. QR codes currently encode `GITAQR://chapter/01` through `18`; they work with this app's camera scanner. For a printed commercial book, the recommended production approach is to deploy the app first, then regenerate QR codes as permanent HTTPS URLs such as `https://your-domain/#chapter-1`.

## Important content and legal notes
- This kit contains original summaries, not a complete scripture translation, not scholarly commentary, and not finished narration or animation videos.
- Verse numbering/wording differs across editions. Choose a trusted public-domain or properly licensed translation and have Sanskrit, Telugu, Hindi, and English content reviewed by qualified editors.
- Do not assume modern translations, recordings, music, or illustrations are free to reuse. Use public-domain material, your own work, or properly licensed content.
- Camera scanning uses a QR library from a CDN and therefore needs internet access. The core chapter list and summaries are bundled locally.
- This is a deployable starter web app, not a signed APK or a hosted public app. Hosting, real media, content review, and cross-device testing remain before public launch.


## Hosting and Android APK
See `HOSTING_AND_QR.md` for GitHub Pages and production QR instructions. See `android-apk-starter/README-APK.md` for building a debug APK. No APK has been built or included.

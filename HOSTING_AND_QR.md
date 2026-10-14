# Hosting and QR publishing checklist

## GitHub Pages
1. Sign in to GitHub and create a new **public** repository, e.g. `bhagavad-gita-qr`.
2. Upload the contents of the main project folder to the repository root: `index.html`, `chapters.js`, `manifest.json`, `sw.js`, `qr_codes/`, and other assets. Do not upload the ZIP as the only file.
3. In the repository, open **Settings → Pages**.
4. Under Build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. Wait for deployment and open the URL shown in Settings → Pages. The site should use HTTPS.
6. Test on a computer and Android phone.

Official instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## Important QR production change
The current QR PNG files encode `GITAQR://chapter/01` etc. They are intended for the app's built-in scanner. They are not the final QR codes for a public printed book. After the website is live, regenerate QR codes to use permanent links such as:
`https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/#chapter-1`
Use your actual deployed URL in place of the example. Then test every QR with a normal phone camera before printing.

## Content/video workflow
1. Select one trusted base translation or a public-domain/licensed edition.
2. Verify Sanskrit text, verse numbering, and translations in Telugu, Hindi, and English with knowledgeable reviewers.
3. Use original summaries, illustrations, narration, and licensed music.
4. Upload MP4/MP3 files to stable HTTPS storage.
5. Add their URLs to `chapters.js` in each chapter's `video` and `audio` language fields.
6. Test each chapter link and each language. Do not print final QR codes until URLs are stable.

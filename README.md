# Eternally — a cinematic love letter

A single-file website (`index.html`): password gate → intro → particle photo reveal → message → song.

## Run on Windows 11
1. Extract the ZIP.
2. Double-click `index.html` (opens in Edge/Chrome). Internet is needed for the fonts and the YouTube player.
3. Optional local server: install Node.js, then in the folder run `npx serve .` and open the printed URL.

## Customize (open `index.html` in Notepad / VS Code)
- Password: function `ok()` — currently the digits 1192026 (or 11092026), numbers only. Casual gate, not real security.
- Song: constant `const SONG='...'` (YouTube video ID) and the `href` of `#song`. Use the official upload.
- Photo: the `<img id="photo">` source is embedded as base64. Replace it with `src="photo.jpg"` (put the file beside `index.html`; use a local server for the particle effect to read pixels).
- Message text: the `.msg` block.

## Notes
- Particle count: ~7,500 on phones, ~14,000 on desktop. Reduced-motion users skip the particle animation.
- No audio file is bundled; music plays only through the YouTube embed after a tap.
- The YouTube embed was not verified to play in every environment; the "open on YouTube" link is the fallback.

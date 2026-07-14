# Lamplight Reader

A private, local audiobook player for your browser. Upload an EPUB or PDF and it reads the book aloud using a free neural voice — no account, no server, no upload to anywhere. Everything happens in your own browser tab.

## Features

- **EPUB and PDF support** — drop in a file or choose one from your device
- **Kokoro AI voice** — a free, offline-capable neural text-to-speech engine (not a robotic browser voice), with about a dozen built-in voices to choose from
- **Reads along visually** — shows the previous, current, and next paragraph, with the sentence being read highlighted as it plays
- **Remembers your place** — both your reading position and the last book you opened reopen automatically next time
- **Tap Contents to jump to any chapter**
- **Adjustable text size and a dark mode**
- **Optional language filter** — mutes and masks a set of common profanity, on by default; you can turn it off or add your own words in Settings
- **Lock-screen playback controls** — play/pause/skip from your phone's lock screen while it plays in the background

## How to use it

1. Open the page and choose an `.epub` or `.pdf` file
2. Tap **Play** — the first time, it downloads the voice model (a one-time download, cached afterward)
3. Use **Contents** to jump between chapters, and **Settings** to change voice, speed, text size, dark mode, or the language filter
4. Just close the tab whenever — it picks back up from the same spot next time you open the page

## Privacy

Nothing is ever uploaded anywhere. The book file, the voice model, and your reading progress are all stored locally on your own device (in your browser's local storage). No account, no server, no tracking.

## Browser notes

- Works best in **Chrome or Edge**, which can run the voice model on the GPU for faster, smoother playback. It still works in Safari, just slower on longer sentences, since it falls back to CPU-only processing there.
- On **iPhone**, this must be opened as a real web address (a hosted link), not a local file — opening a saved HTML file directly in the Files app won't run it. If you're reading this after publishing to GitHub Pages or similar, you're already set up correctly.
- Browsers periodically clear site data for pages you haven't visited in a while (roughly a week of inactivity in Safari). If that happens, your last book and settings may reset and need to be reopened once.

## Known limitations

- Only remembers one book at a time — opening a new one replaces the previous "last opened" book
- PDF paragraph breaks are an approximation based on line spacing, since PDFs don't have real paragraph markup the way EPUBs do
- DRM-protected EPUBs (from most bookstores) can't be opened, since the text itself is encrypted
- Voice quality and speed depend on your device's hardware

## Credits

Built with [Kokoro](https://huggingface.co/onnx-community/Kokoro-82M-v1.0-ONNX) for text-to-speech, [pdf.js](https://mozilla.github.io/pdf.js/) for PDF parsing, and [JSZip](https://stuk.github.io/jszip/) for EPUB parsing.

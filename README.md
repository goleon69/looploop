# looploop

A tiny practice tool that runs in your browser. Open a track, loop the part you want to work on, and change its key or slow it down while you play along. No install, nothing is saved or uploaded.

**Status: early prototype (v0.3).** It exists to check sound quality and stability on Safari (Mac, iPhone, iPad). The interface is minimal and currently in Italian only.

**Use it online:** https://goleon69.github.io/looploop/
**Or offline:** download `looploop.html` and open it in a desktop browser.

## Features

- Loop between two points: set them at the current position or type the times
- Transpose by semitones (up to 3 up or down) without changing the duration
- Slow down (50% to 100%) without changing the pitch
- Volume control
- Opens any audio format your browser can decode (MP3, M4A, WAV, ...)
- Listening only: no audio file is written, so there is no re-encoding and no quality loss to manage
- Everything happens locally: your audio never leaves your device

## How it works

Everything is in one file, `looploop.html` (HTML + CSS + JavaScript).

- The track is decoded with the Web Audio API and played by an AudioWorklet that feeds it through [SoundTouchJS](https://github.com/cutterbl/SoundTouchJS) for pitch and tempo changes.
- If the browser refuses the AudioWorklet, the same engine runs in the page as a fallback. The header shows which one is in use.
- A 3 ms fade at the loop junction avoids clicks.

looploop is the sibling of [cutcut](https://github.com/goleon69/cutcut), a lossless MP3 trimmer.

## License

GPL-3.0. See [LICENSE](LICENSE). You can use, study, change and share looploop; modified versions you distribute must also be released under GPL-3.0.

Copyright (C) 2026 Leonardo Gon

`looploop.html` includes SoundTouchJS v0.1.30, unmodified, copyright (C) Olli Parviainen, Ryan Berdeen, Jakub Fiala and Steve 'Cutter' Blades, licensed under LGPL 2.1 or later.

---

*Italiano:* looploop serve per esercitarsi suonando sopra un brano: si ripete in loop una parte, si cambia tonalità a semitoni e si rallenta, tutto in ascolto e senza salvare file. Si apre nel browser, senza installare niente. Per ora è un prototipo.

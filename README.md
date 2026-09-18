# K3-SSS-Digital-Sound

An interactive lecture on digital sound, built for **KD343A — Situated and speculative
sensing: multisensory exploration of environments** at K3, the School of Arts and
Communication, Malmö University.

**→ [Open the lecture](https://dcuartielles.github.io/K3-SSS-Digital-Sound/)**

The whole thing is one self-contained HTML file. No build step, no dependencies, no
tracking. Everything it draws and every sound it makes is generated in the browser
with the Web Audio API and a canvas.

## The argument

> Every digitisation is a decision about what is allowed to count as environment.

Sample rate decides which creatures exist in your data. A-weighting decides whose
discomfort is measurable. FFT window length decides whether a place is a state or an
event. A map pin decides a site has one sound. None of these are neutral, and all of
them are set before anybody listens.

## Six live instruments

| # | Instrument | What you can do with it |
|---|---|---|
| 01 | Live spectrogram | Watch the room through a microphone, on the magma colour ramp |
| 02 | Decimation ladder | Drag the sample rate from 44.1 kHz to 2 kHz and hear who disappears |
| 03 | Bit depth and dither | 16 down to 2 bits, with dither on or off, on the quiet tail of a tone |
| 04 | Aliasing | A sweep sampled too slowly, with the fold-back plotted against the Nyquist ceiling |
| 05 | FFT window | 256 to 16 384 samples on a live spectrogram — the time/frequency trade-off by hand |
| 06 | A-weighting and L(A)eq | Live level with the weighting curve on or off, and a running equivalent level |

Instruments 02, 03, 05 and 06 take **your own field recordings** through the file
picker, so the deck works as a tool after the lecture is over, not just during it.

## Using it

Open the link above, or clone and open `index.html`.

- **Arrow keys** or space move between slides
- **`D`** jumps to the next instrument
- **`I`** opens the slide index
- **`N`** shows the speaker notes
- **`Theme`** switches light and dark
- Every slide has its own `#anchor`, so you can link straight to a demo

### Running it locally

The microphone needs a secure context. Opening `index.html` straight from disk usually
works in Chrome and Edge, but if the browser refuses the microphone, serve the folder
instead:

```
python -m http.server 8000
```

then open <http://localhost:8000/>. GitHub Pages serves over HTTPS, so the hosted
version has no such problem.

### Browser support

Needs the Web Audio API and `getUserMedia` — any current Chrome, Edge, Firefox or
Safari. The microphone instruments require permission; the rest run without one.

## Teaching with it

The deck is one half of a pair. The other is a four-hour field workshop: a soundwalk
recording three contrasting sites three ways each, an analysis block, and a choice of
three making stations — Sonic Pi, a browser sound map, or an Arduino Nano 33 BLE Sense
logging sound level alongside temperature, humidity and light.

### The teaching notes are part of the material

Press **`N`** on any slide for the notes. They are written for whoever is *running* the
lecture, not for the audience: what to say out loud, what to hold back, which demo to let
sit in silence, where a colleague takes over. They are published on purpose. If you teach
this, they are the half that usually stays private, and they are more useful to you than
the slides are.

## Sources and further reading

- Droumeva, *Soundmapping as critical cartography* (2017)
- Shaw & Bowers, *Ambulation* (NIME 2020)
- Scurto & Postel, *Soundwalking Deep Latent Spaces* (NIME 2023)
- Gaye, Mazé & Holmquist, *Sonic City* (NIME 2003)
- Tahiroğlu, Kastemaa & Koli, *GANSpaceSynth* (AIMC 2021)
- Aiello, Schifanella & Quercia, *Chatty Maps* (2016)

Live links to all of these are on the relevant slides.

## Credits

Written by David Cuartielles for K3, Malmö University, 2026.
Typefaces: Familjen Grotesk and IBM Plex Mono, via Google Fonts.

## License

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-A8431A.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/) (`CC-BY-NC-SA-4.0`).

You are free to share and adapt it for non-commercial purposes, as long as you credit the
source and license your adaptations the same way. Teach with it, fork it, translate it,
rewrite the slides for your own course — that is what it is for.

See [LICENSE](LICENSE).

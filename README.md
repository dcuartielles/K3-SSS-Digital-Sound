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
event. A map pin decides a site has one sound. A training set decides what a machine can
imagine. None of these are neutral, and all of them are set before anybody listens.

## Eight live instruments

| # | Instrument | What you can do with it |
|---|---|---|
| 01 | Live spectrogram | Watch the room through a microphone, on the magma colour ramp |
| 02 | Decimation ladder | Drag the sample rate from 44.1 kHz to 2 kHz and hear who disappears |
| 03 | Bit depth and dither | 16 down to 2 bits, with dither on or off, on the quiet tail of a tone |
| 04 | Aliasing | A sweep sampled too slowly, with the fold-back plotted against the Nyquist ceiling |
| 07 | Two domains | A sine with frequency and amplitude sliders beside its real FFT — drag the marker in the spectrum and the waveform is rebuilt to match |
| 08 | Fourier series | Add odd harmonics one at a time and watch a sine turn into a square wave, with the Gibbs overshoot that never leaves |
| 05 | Window, spectrum, spectrogram | A cursor carries the analysis window across the wave while the window's spectrum and the spectrogram are drawn beneath it, column by column, at 256 to 16 384 samples |
| 06 | A-weighting and L(A)eq | Level with the weighting curve on or off and a running equivalent level, from the microphone or from a file — with a file the clip's own length is the averaging period |

Instrument numbers are stable handles rather than a running order — 07 and 08 open the
spectrogram segment, and the workshop deck points students at 02, 03 and 06 by number.

Instruments 02, 03, 05 and 06 take **your own field recordings** through the file
picker, so the deck works as a tool after the lecture is over, not just during it.
The picker in 02, 03 and 05 keeps the first twelve seconds; 06 measures the whole clip.
Every slider is live while a sound is playing: changing the sample rate, the bit depth
or the window size re-renders under the playhead rather than waiting for the next press
of Play.

## Using it

Open the link above, or clone and open `index.html`.

- **Arrow keys** or space move between slides
- **`D`** jumps to the next instrument
- **`I`** opens the slide index
- **`N`** shows the speaker notes
- **`Theme`** switches light and dark
- Every slide has its own `#anchor`, so you can link straight to a demo

### Putting your own institution on it

Drop a logotype beside `index.html` as `mau-logo.png` and the cover and the bottom bar
pick it up. With no such file, both fall back to a plain typographic lockup, so nothing
breaks if you would rather not brand it at all.

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

The deck is one half of a pair. The other is a four-hour workshop, held indoors.
Students arrive with recordings they made beforehand — one site, three microphone
positions — and spend the first hour putting their own takes through the instruments
from this deck. Then Strudel, taught from zero, and a choice of two tracks: compose
sixty seconds out of your own recordings, or sonify a sensor log from an Arduino Nano
33 BLE Sense, which offers exactly two sample rates and so forces the choice instrument
02 is about.

Because there is no fieldwork on the day, the recording brief has to land in the
lecture. The closing slides carry it.

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
- Aiello, Schifanella, Quercia & Aletta, *Chatty Maps* (R. Soc. Open Sci. 2016)
- Quercia, Schifanella, Aiello & McLean, *Smelly Maps* (ICWSM 2015)
- Tahiroğlu, Kastemaa & Koli, *GANSpaceSynth* (AIMC 2021)
- Engel et al., *GANSynth* (ICLR 2019)
- Pieretti, Farina & Morri, *Acoustic Complexity Index* (2011)
- ISO 12913-1:2014, *Acoustics — Soundscape — Part 1: Definition and conceptual framework*

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

# Journey Through the Solar System

A cinematic WebGL tour from the cold edge of the solar system down to the Sun — fourteen stops, a generative ambient score, and nothing to install. The whole experience is a single self-contained HTML file.

**[▶ Take the journey](https://yoavbz.github.io/solar-system-journey/)**

![Saturn, seen from the journey](screenshot.jpg)

### The route

Deep Space → Neptune → Uranus → Saturn → Jupiter → the Asteroid Belt → Mars → Earth & the Moon → Venus → Mercury → the Sun — then three closing scenes: a size comparison of the planets, an orbit map, and a farewell.

Each stop plays out as a slow camera move with film-style captions. Let it run as a guided tour, or take the controls yourself.

### Features

- **One file.** Planet textures (NASA-derived maps) are embedded as data URIs, so `index.html` carries everything except two CDN dependencies (three.js and fonts).
- **Generative score.** No audio files: a four-voice Web Audio drone whose harmony warms and brightens as you fall sunward, a filtered-noise whoosh during flights between worlds, and a soft arrival tone at each stop. Toggle with the music button or <kbd>m</kbd>.
- **Living scenes.** Storm bands on Jupiter, Saturn's rings with orbiting moons, a dense asteroid belt, city lights on Earth's night side, solar prominences — plus a false-color science view of the Sun.
- **Accessible by design.** Keyboard navigation throughout, hover any world for its name, and `prefers-reduced-motion` starts the tour paused so visitors move at their own pace.

### Controls

| Input | Action |
|---|---|
| <kbd>→</kbd> / <kbd>←</kbd> | Travel to the next / previous stop |
| <kbd>Space</kbd> | Pause or resume the tour |
| <kbd>m</kbd> | Toggle music |
| Dots (top center) | Jump to any stop |
| Mouse hover | Name the world under the cursor |

### Running locally

No build step. Clone the repo and open `index.html` in a browser, or serve it:

```sh
python3 -m http.server
# then visit http://localhost:8000
```

An internet connection is needed the first time for the two CDN resources (three.js r128 and the Fraunces/Outfit fonts).

### Credits

Planet imagery derived from NASA maps. Rendered with [three.js](https://threejs.org/) r128.

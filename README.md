# Journey Through the Solar System

A cinematic WebGL tour from the cold edge of the solar system down to the Sun — fourteen stops, a generative ambient score, and nothing to install. A small static site with no build step and no third-party dependencies.

**[▶ Take the journey](https://yoavbz.github.io/solar-system-journey/)**

![Saturn, seen from the journey](screenshot.jpg)

## The route

Deep Space → Neptune → Uranus → Saturn → Jupiter → the Asteroid Belt → Mars → Earth & the Moon → Venus → Mercury → the Sun — then three closing scenes: a size comparison of the planets, an orbit map, and a farewell.

Each stop plays out as a slow camera move with film-style captions. Let it run as a guided tour, or take the controls yourself.

## Features

- **Fully self-hosted.** No CDNs, no third-party requests: three.js, the fonts, and the planet maps all live in this repo. The page is interactive in about a second; high-resolution textures stream in behind the procedurally painted planets.
- **Generative score.** No audio files: a four-voice Web Audio drone whose harmony warms and brightens as you fall sunward, a filtered-noise whoosh during flights between worlds, and a soft arrival tone at each stop. Toggle with the music button or <kbd>m</kbd>.
- **Living scenes.** Storm bands on Jupiter, Saturn's rings with orbiting moons, a dense asteroid belt, city lights on Earth's night side, solar prominences, a passing comet — plus a false-color science view of the Sun.
- **A deep sky.** Thousands of layered stars, the Milky Way with its dust lanes, and a handful of distant galaxies.
- **Field notes.** An opt-in "Did you know?" layer: three or four curated facts per stop, one at a time, in a quiet card that holds the tour while you read.
- **Free-look.** Drag the sky — mouse or finger — to look around while the camera keeps riding its authored path; let go and the gaze drifts back to the film. Works at every stop and even mid-flight.
- **Made for touch too.** Swipe to travel, drag to look, tap a world for its name, and a safe-area-aware layout.
- **Accessible by design.** Keyboard navigation throughout, hover any world for its name, and `prefers-reduced-motion` starts the tour paused so visitors move at their own pace.

## Controls

| Input | Action |
|---|---|
| <kbd>→</kbd> / <kbd>←</kbd> | Travel to the next / previous stop |
| <kbd>Space</kbd> | Pause or resume the tour |
| <kbd>d</kbd> | Open the field notes (while open, <kbd>→</kbd>/<kbd>←</kbd> browse facts) |
| <kbd>f</kbd> | Cycle travel speed (1× / 2× / 4×) |
| <kbd>m</kbd> | Toggle music |
| Dots (top center) | Jump to any stop |
| Drag the sky | Look around from where you are — release to drift back |
| Mouse hover / tap | Name the world under the cursor or finger |
| Swipe left / right | Travel between stops (touch screens) |

## Running locally

No build step and no internet needed. Clone the repo and serve the folder:

```sh
python3 -m http.server
# then visit http://localhost:8000
```

(Opening `index.html` straight from the file system mostly works too, but browsers block texture loading from `file://`, so the planets keep their painted procedural looks instead of the photographic maps.)

## Credits

Planet and moon maps by [Solar System Scope](https://www.solarsystemscope.com/textures/) ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)), based on NASA imagery. Rendered with [three.js](https://threejs.org/) r128.

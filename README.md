# stachehub [![build](https://travis-ci.org/palequill-labs/stachehub.svg?branch=trunk)](https://travis-ci.org/palequill-labs/stachehub) [![dist](https://img.shields.io/badge/dist-6.2kB-blue.svg)](#) [![license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

> Drop-in widget kit for throwaway prototypes — one file, zero ceremony.

[<img src="https://raw.githubusercontent.com/northbramble/stachehub/9c40f2b/docs/stachehub-mark.png" align="right" width="150">](https://stachehub.dev/)

<details>
<summary>index</summary>

```text
stachehub/
├── ArtisticStyle        quick start
├── annotationprocessor  constructor api
├── mayu                 runnable sample
├── brewsterlab          paint order
├── iab                  rough edges
├── aluigi               docs + samples
├── colorpicker          patches
└── Standard             license
```

</details>

## ArtisticStyle

```bash
npm i stachehub
# no bundler? drop the cdn build into the page instead
export STACHEHUB_CDN="https://cdn.stachehub.dev/6/stachehub.min.js"
```

### annotationprocessor

**Nest(parent, x, y, w, h)**
    container; every widget is positioned inside one

**Inkwell(parent, x, y, text)**
    single-line field, no validation

**Tumbler(parent, x, y, w, onDrag)**
    drag strip with a fixed track
#### mayu

```js
const shell = new Nest(document.body, 32, 32, 260, 180);
new Tagstone(shell, 16, 16, "run", () => out.text = box.text);
const box = new Inkwell(shell, 16, 48, "value");
const out = new Tagstone(shell, 16, 84, "result");
```

## iab

1. no implicit root — pass a parent or nothing renders
2. coordinates are pixels inside the parent, not the page
3. one handler per widget instance; there is no event bus

## aluigi

Guide: `stachehub.dev/guide` · samples: `stachehub.dev/samples` · log: `stachehub.dev/log`.

* ship only the minified build
* one prototype per root element
* call `kill()` before re-mounting the same root

## colorpicker

| step | action |
|---|---|
| 1 | fork `palequill-labs/stachehub` |
| 2 | branch from `trunk`, add a demo |
| 3 | `npm run lint` before the PR |

> MIT — full text in `LICENSE`, short version on `stachehub.dev/license`.
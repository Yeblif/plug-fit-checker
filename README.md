# Plug Fit Checker

A standalone browser tool for checking, visually, whether bulky UK smart plugs will fit side by side on an extension lead.

You load a photo of the extension lead and a product photo of the smart plug, mark the three socket holes and the three plug pins, and the tool scales, rotates and positions copies of the plug over adjacent sockets so you can see whether the bodies clash.

**▶ Live version:** https://yeblif.github.io/plug-fit-checker/ *(once GitHub Pages is enabled)*

## Features (V7)

- Load an extension-lead photo and a smart-plug photo from your device — nothing is uploaded anywhere
- Mark three socket-hole centres on up to two sockets, and the three pin centres on the plug photo (any order — matching uses triangle geometry)
- Separate **Socket**, **Plug** and **Check** stages, each with its own view
- Align plug 1, plug 2 or both, using earth, live, neutral or centroid as the anchor
- Adjust overlay opacity and fine scale to inspect interference between neighbouring plugs
- Zoom, pan and drag points to refine on desktop or mobile (pinch-zoom and two-finger pan supported)

## How to use

1. Open `index.html` in a modern browser (or use the live link above).
2. Load both photos. Shoot as close to perpendicular to the socket face and pin face as you can.
3. **1 Socket** — mark the three holes on two adjacent sockets. Zoom in and drag points to correct.
4. **2 Plug** — mark the three pins on the plug photo.
5. **3 Check** — click **Align both plugs** and inspect the overlap. Fine-tune opacity/scale as needed.

### Controls

| | Desktop | Mobile |
|---|---|---|
| Mark point | Click | Tap |
| Refine point / move overlay | Drag | Drag |
| Zoom | Mouse wheel, double-click | Pinch |
| Pan | Right-click drag or Space + drag | Two-finger drag |

## Limitations

This is a **visual screening aid, not a verified mechanical fit**.

- Three-point matching is heuristic and can misread orientation on mirrored or oblique photos
- Assumes uniform image scale — no perspective correction, and plug-body depth isn't measured
- Opaque product-photo backgrounds can hide neighbouring sockets
- No automatic collision detection or "fits / doesn't fit" verdict

## Repository layout

```
index.html                 Latest release (V7) — served by GitHub Pages
versions/                  Every historical version, preserved unchanged (V1–V7)
docs/tool-description.md   Full tool description
docs/version-history.md    Changes, fixes and known issues for each version, with SHA-256 hashes
docs/file-manifest.csv     Version manifest
```

Each HTML file is fully self-contained — embedded CSS and JavaScript, no libraries, no network calls, no backend.

## Version summary

| Version | Highlights |
|---|---|
| V1 | Initial prototype — manual three-point calibration, drag/rotate, opacity and scale |
| V2 | Zoom/pan while calibrating, magnifier, undo, drag-to-refine points |
| V3 | Plug points stored in image-local coordinates — fixes scale drift |
| V4 | Automatic align-to-socket with anchor selector |
| V5 | Experimental auto-detect of holes/pins, second socket, duplicate plug |
| V6 | Mobile-friendly controls and responsive layout |
| V7 | Auto-detect removed; clean Socket / Plug / Check stages; second plug hidden until aligned |

See [`docs/version-history.md`](docs/version-history.md) for full details.

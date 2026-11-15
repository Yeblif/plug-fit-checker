# Smart Plug Fit Checker — Tool Description

## Purpose
A standalone, local HTML/JavaScript tool for visually checking whether bulky UK smart plugs can fit side by side on an extension lead. It overlays scaled smart-plug product photography on extension-lead photography, using the three UK plug pin/socket-hole positions as matching reference points.

## Main functionality (latest release: V7)
- Load an extension-lead image and a smart-plug image from the device.
- Manually mark three socket-hole centres on up to two sockets, and three corresponding pin centres on the plug photo.
- Independently view the extension and plug photos during calibration.
- Align one or two copies of the smart plug photo onto selected socket locations, calculating scale, rotation and position from marked points.
- Adjust overlay opacity and fine scale; inspect apparent interference between neighbouring plug bodies.
- Zoom, pan and edit points on desktop or mobile.

## Image calibration and alignment
1. **Socket stage:** load the extension-lead photo, choose 'Set socket 1 points' and mark its three holes; repeat for socket 2. The three points can be clicked in any order (the matching algorithm uses triangle geometry).
2. **Plug stage:** load the smart-plug photo and mark the three plug pins. Points are stored in plug-image coordinates, not the overlay coordinates.
3. **Check stage:** choose an anchor (earth, live, neutral or centroid), then align plug 1, plug 2 or both. The algorithm compares triangle side lengths for scale, uses the lower-pin axis for rotation, and translates the selected anchor to the target socket.
4. Inspect the overlay and adjust opacity or fine scale as needed. The second plug is initially hidden and only becomes visible after alignment.

## Supported interactions
- Desktop: click to mark points, drag points to refine, mouse-wheel zoom, right-click or Space+drag pan, double-click zoom, and drag the selected plug overlay in Check view.
- Mobile: tap to mark points, drag points/selected overlay, two-finger pinch zoom and two-finger pan.
- Buttons for point entry, undo, alignment, stage switching, visibility and fitting the image to the view.

## How to use
1. Extract the ZIP archive and open `Versions/smart_plug_fit_checker_v7.html` in a modern browser.
2. Load both photographs. For reliable results, use views as close to perpendicular to the socket face and plug pin face as possible.
3. In **1 Socket**, mark the three holes on two adjacent sockets. Use zoom and drag-to-correct for accuracy.
4. In **2 Plug**, mark the three pins on the plug photo. This is a separate image view.
5. In **3 Check**, click **Align both plugs** and examine how the plug bodies overlap. Fine-tune as required.
6. Treat the result as a visual screening aid, not a verified mechanical fit. Photographic perspective, body depth, plug orientation, occlusion and product-image cropping can cause misleading results.

## Dependencies and data handling
- Each HTML file is standalone: embedded HTML, CSS and JavaScript, no external libraries, network services or backend.
- Photos are selected locally in the browser. The tool does not upload them to a server.
- No companion assets are needed for the archived versions.

## Limitations and known issues
- Three-point triangle matching is heuristic and may misidentify orientation on mirrored or oblique photographs.
- Calibration assumes uniform image scale; it does not rectify perspective or measure plug-body depth.
- A product photo's opaque background may obscure other sockets and make collision assessment difficult.
- No automated collision detection or definitive 'fits' verdict.
- Historical versions contain their original bugs and experimental features; use V7 for the latest workflow.

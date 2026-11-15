# Smart Plug Fit Checker — Version History

Versions listed chronologically. Original files have been preserved without modification.

## V1 — `smart_plug_fit_checker.html`

**Features, UI, calibration and alignment changes:** Initial browser prototype. Load extension and smart-plug photos; three-point manual calibration for each; average triangle-distance scaling; drag/rotate plug; opacity and fine-scale controls; zoom and pan.

**Bug fixes, removals and known issues:** Calibration points stored in shared world coordinates; plug-point positions did not follow plug transformations. No automatic alignment or duplicates.

**Original file:** included; 12,134 bytes; SHA-256 `3a2969e1e2e5efc652e4411c2b8781764aa2cc7c8e5d86bedf507fef014245be`.

## V2 — `smart_plug_fit_checker_v2.html`

**Features, UI, calibration and alignment changes:** Zoom and pan while calibrating; double-click zoom; on-canvas magnifier; undo last point; drag points to refine; improved calibration instructions.

**Bug fixes, removals and known issues:** Plug calibration points still stored in world coordinates, so adjusting plug scale could desynchronise photo and points.

**Original file:** included; 17,295 bytes; SHA-256 `e6a470fad102cbf43a85084b99910e14c81890bea068998e5e2bc14fcab211d3`.

## V3 — `smart_plug_fit_checker_v3.html`

**Features, UI, calibration and alignment changes:** Plug points changed to plug-image-local coordinates; coordinate transforms added so markers follow overlay translation, rotation and scale.

**Bug fixes, removals and known issues:** Fixed reported severe scale drift from plug-point coordinate mismatch. Still requires manual alignment; photo perspective and background remain limitations.

**Original file:** included; 18,939 bytes; SHA-256 `22b85e2d6115c9def0de11fc3871daa9760ccbd537efc8228fd238648cdb6575`.

## V4 — `smart_plug_fit_checker_v4.html`

**Features, UI, calibration and alignment changes:** Align plug to calibrated socket using translation, rotation and scale; anchor selector (earth/live/neutral/centroid); attempts order-independent three-point matching.

**Bug fixes, removals and known issues:** Triangle-based point classification is heuristic; mirrored/front-versus-back photos and ambiguous perspective can produce incorrect orientation. No duplicate plug yet.

**Original file:** included; 22,650 bytes; SHA-256 `51a7ef25874ff07bc19a39e634c483e301d979c1bdcc87a6ff71d1056e7e7f5e`.

## V5 — `smart_plug_fit_checker_v5.html`

**Features, UI, calibration and alignment changes:** Experimental auto-suggest for socket holes and plug pins with manual approval/correction buttons; second socket point set; duplicate plug; align plug 1, plug 2 or both for visual clash comparison.

**Bug fixes, removals and known issues:** Auto-detection based on simple dark connected components and triangle scores is unreliable; approval buttons provide messaging, not a hard gate to alignment. Both overlays appear immediately and calibration remains cluttered.

**Original file:** included; 22,918 bytes; SHA-256 `afd6dd6ed901419bcdef5bb9670ee59b139d421a493bd6fc2eaea8d78fee0305`.

## V6 — `smart_plug_fit_checker_v6.html`

**Features, UI, calibration and alignment changes:** Mobile-oriented controls: larger touch targets, responsive layout, one-finger dragging, two-finger pan/pinch zoom, fit-view and help controls.

**Bug fixes, removals and known issues:** Inherits V5 experimental detection and two-visible-overlays behaviour. Live recalculation while editing calibration points can resize overlays during placement/correction.

**Original file:** included; 27,340 bytes; SHA-256 `ca3fd81fcfb55051c6b6d479929beced75f88d8fe0b7dcfc9285f46a81fcd9b0`.

## V7 — `smart_plug_fit_checker_v7.html`

**Features, UI, calibration and alignment changes:** Removed auto-detection; separate Socket, Plug and Check stages; plug photo calibrated alone in native image coordinates; no scaling while entering points; second plug hidden until aligned; touch gestures retained.

**Bug fixes, removals and known issues:** Second plug appears only after its own alignment. Visual clash inspection only: no image background removal, perspective correction or automatic collision verdict. Manual point precision and image viewpoint still matter.

**Original file:** included; 22,246 bytes; SHA-256 `fe693738719326c7a9a83fcea992be4a4544778241f78ef1c7b39d76a0dbed85`.


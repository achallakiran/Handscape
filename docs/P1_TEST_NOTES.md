# Handscape P1 v0.3 — implementation and test notes

## Added
- Gold-edged training ledge and second elevated platform in the existing workshop.
- Context-aware ledge acquisition and hanging (four sides of authored solid platforms).
- Shimmy along reachable edges, mantle animation, and deliberate drop.
- A hanging workshop cable with pendulum-style pump and airborne launch.
- A permanent GRIP control on mobile with CLIMB/LAUNCH labels replacing JUMP appropriately.
- Hand pose when hanging and swinging, camera retargeting, and revised tutorial cues.

## Automated checks completed
- Existing P0.5 keyboard direction + toolbox collision regression tests.
- New edge detection, grip, shimmy, mantle, and release state tests.
- New cable capture, swing-pump, and launch state tests.
- Mobile landscape button layout and pointer events for Grip and Jump/Climb.
- JavaScript syntax and offline HTML structural checks.

## Not yet validated
- Real WebGL visual/gameplay quality on a physical device. The available headless browser environment did not provide a working WebGL context (JavaScript gameplay tests use a render stub).
- Complete climbing on arbitrary meshes or surfaces; first release supports hand-authored box ledges and a scripted swinging cable.
- Full skeletal/IK finger contact and production-grade swing physics.

## Release parity
- Both `index.html` and `Handscape-Offline.html` must have identical bytes for this version.
- `index.html` is deployed by GitHub Pages. `Handscape-Offline.html` should work as an offline, self-contained local file on a supported WebGL browser.
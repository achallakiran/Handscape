# HANDSCAPE

**Small Hand. Big Trouble.**

An original, offline-first voxel adventure about Nim, a tiny living hand exploring a giant workshop through parkour, puzzles, and playful mischief.

## Play

- **GitHub Pages:** https://achallakiran.github.io/Handscape/ (requires Pages deployment to be enabled)
- **Offline:** Download [`Handscape-Offline.html`](Handscape-Offline.html) and open it in a desktop browser with WebGL support. The file has no external runtime dependencies and does not need a development server.

The two files are intentionally the same standalone game. GitHub Pages deploys `index.html`; `Handscape-Offline.html` is the downloadable offline distribution.

## P1 prototype controls (v0.3)

| Action | Desktop | Mobile landscape |
|---|---|---|
| Move | W / A / S / D or arrow keys | Left virtual joystick |
| Camera | Drag | Swipe outside control areas |
| Jump | Space | JUMP |
| Catch ledge or cable | **G** while airborne | **GRIP** |
| Pull up while hanging | **Space** | **CLIMB** (same button as Jump) |
| Let go while hanging | **G** again | **DROP** (same button as Grip) |
| Swing along cable | W / S while attached | Joystick forward/back |
| Launch from cable | Space while swinging | LAUNCH |
| Interact / mischief | E | Contextual USE |
| Pause | Esc | Pause icon |

### Try the new parkour mechanics

1. Start the adventure. The **gold-edged teal crate** is just ahead of the starting position.
2. Jump toward the crate's upper edge and tap **G / GRIP** while airborne.
3. Once hanging, move left/right to shimmy and press **Space / CLIMB** to pull yourself up. Use **G / DROP** to let go instead.
4. Look for the **brass-tipped hanging cable** near the central workbench. Jump and grip it, pump the swing with W/S, then launch with Space.
5. Ring the bell, stop the ventilation fan with its switch, and reach the vent to finish the current workshop objective.

Normal gameplay keeps the screen mostly clear. Short contextual hints appear only around reachable parkour features and interactable objects. If you miss a ledge, retry the jump; ordinary failures do not permanently block the game.

## Current scope

**v0.3, P1 first playable parkour slice:** guided ledge-grabbing, hanging, sideways shimmy, animated mantle, a pendulum-style rope swing, momentum launch, an expressive voxel hand, basic collision-aware traversal, and the existing bell/fan/mischief interactions. This is **not the complete first chapter**: full finger-bone IK, environmental puzzles, improved NPC AI, multiple scenes, complex rope physics, and production polish are still planned.

## Technical notes

- Single-file HTML5/WebGL game with inline JavaScript and voxel meshes; no CDN, no externally hosted libraries, no network requests to play.
- Gameplay, settings, menus, and audio use browser capabilities. Local storage persistence may vary for `file://` documents.
- The browser must support WebGL; mobile file opening varies by browser. GitHub Pages is the recommended mobile entry point.
- Workflow: `.github/workflows/deploy.yml` publishes `index.html` and the offline file to GitHub Pages whenever `main` changes (provided Pages is configured to use GitHub Actions).

## Source and implementation

This repository currently intentionally keeps the playable runtime in `index.html` so the offline file can be copied byte-for-byte. Future refactoring must preserve the two-format release requirement from a shared source.

The art, protagonist, story, title screen and gameplay mechanics are developed for **Handscape** as an original project.
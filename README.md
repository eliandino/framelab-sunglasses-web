# FrameLab: mobile sunglasses designer

A GitHub Pages ready, browser based prototype. Draw a mirrored lens outline by dragging its cyan control points, enter exact millimetre dimensions, inspect the 3D preview, and export JSON, SVG, OpenSCAD, or a preliminary frame STL.

## Publish with GitHub Pages

1. Unzip into a new GitHub repository. Keep the `docs` folder at the repository root.
2. In the repository, go to Settings → Pages → Build and deployment → Deploy from a branch. Select your main branch and `/docs` folder, then save.
3. Open the published URL on your phone. The preview loads Three.js from a CDN, so the device needs internet access.

For local testing, serve the repository directory with `python -m http.server 8000` and open `/docs/` in your browser. Opening index.html directly as `file://` may block module imports.

## Design notes

- The JSON file is the editable design. Keep it to continue work; STL cannot restore the controls.
- SVG is the front drawing; OpenSCAD recreates the approximate frame; STL exports the generated frame geometry. These exports are starting points.
- The lens shapes are visual placeholders. The temple and bridge are simple geometry. Add hinge joints, nose pads, curvature, lens groove and manufacturing tolerances before printing or fitting real lenses.
- An SVG viewer may treat the grid and dimension note as decoration; the shape coordinates are millimetres. The preview axes place the front in XY and temples along Z.
- Test printed prototypes for fit and structural strength. Do not use 3D printed transparent pieces as protective lenses.

## Next iteration

Curve handles instead of polygon corners, separate top/bottom rim controls, wrap angle, pantoscopic tilt, hinge dimensions, saved presets, export to Blender via a design JSON importer, and a measured print calibration card.

https://eliandino.github.io/framelab-sunglasses-web/

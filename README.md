# 🎨 Atlas UV Painter

A browser tool for recoloring low-poly game assets that use **gradient atlas textures**. Load a 3D model, then move its UVs around the atlas to change colors. No painting and no re-exporting textures.

Everything runs locally in your browser. Your models are never uploaded anywhere.

**Live demo:** `https://YOUR-USERNAME.github.io/atlas-uv-painter/`

## Features

- Open `.glb`, `.gltf` (self-contained) or `.obj` models, by button or drag and drop
- Built-in 8×8 gradient atlas, or load your own atlas image
- Side-by-side **3D view** and **UV editor** with live updates
- Blender-style controls: `L` to select linked, `G` to grab, `R` to scale
- **Paint** tool: click a color on the atlas and the selected faces take that color
- Snap to atlas cell centers, adjustable grid size
- Unlit preview to see true atlas colors
- Undo, reset UVs, color and UV readout under the cursor
- Export a `.zip` with the GLB (edited UVs) and the atlas PNG

## Quick start

1. Open a model, or use the demo shapes.
2. Hover a part in the 3D or UV view and press **L** to select it. You can also click faces in 3D (Shift adds).
3. Press **G** and move the mouse, then click to confirm. Or pick **Paint** and click a color on the atlas.
4. Click **Export .zip** when you're done.

## Shortcuts

| Key | Action |
| --- | --- |
| `L` | Select the whole part under the cursor (or grow the current selection) |
| `G` | Grab and move the selection. Click or `Enter` confirms, `Esc` or right-click cancels, `X` / `Y` locks the axis |
| `R` | Scale the selection (same confirm and cancel) |
| `B` | Box-select tool |
| `P` | Paint tool |
| `A` | Select all |
| `Esc` | Deselect (when not grabbing) |
| `F` | Fit the UV view |
| `Ctrl/Cmd + Z` | Undo |
| Scroll / right-drag | Zoom / pan the UV view |

## Notes

- On load, each mesh's material is replaced with one that uses the atlas. Other material data is dropped.
- Models need a UV channel. Meshes without UVs load with all UVs at 0,0.
- `.gltf` files must be self-contained (embedded buffers); use `.glb` when in doubt.
- Skinned or animated meshes may not display correctly.
- The tool is made using Ai, So expect some minor bugs.

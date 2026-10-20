# OpenStick hardware

Enclosure CAD, carrier and expansion board files, 3D models for the website, and the bill of materials.

Licensed under the [CERN Open Hardware Licence v2, Strongly Reciprocal](LICENSE).

Status: v0 prototype on the Orange Pi Zero 2W. The v1 board is chosen by the hardware spike ([decision 0004](https://github.com/opensticktv/openstick/blob/main/decisions/0004-stick-or-4k-everywhere.md)).

| Path | Contents |
| --- | --- |
| `bom/` | One CSV per build (`v0.csv`, later `v1-*.csv`) |
| `enclosure/` | Onshape/Fusion exports: STEP for editing, STL/3MF for printing |
| `kicad/` | Custom carrier or expansion board (v2) |
| `models/` | GLB files for the website's exploded view |
| `docs/` | Measurements, thermal and power test results |

## Model conventions (for the website)

- One GLB per part group, named nodes: `enclosure_top`, `enclosure_bottom`, `heatsink`, `board`, `expansion_board`, `hdmi_plug`, `remote`.
- Origin at the assembled position; each part explodes along its own axis.
- Optimise with `gltf-transform optimize --compress meshopt`. Budget: hero GLB under 1 MB, whole scene under 4 MB.

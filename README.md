# OpenStick hardware

Enclosure, remote shell and accessory CAD, plus 3D models for the website.

Licensed under the [CERN Open Hardware Licence v2, Strongly Reciprocal](LICENSE).

The mainboard is a manufacturing partner's certified Android TV design and is not part of this repo ([decision 0008](https://github.com/opensticktv/openstick/blob/main/decisions/0008-certified-base-open-layer.md)). Everything OpenStick designs around it is published here.

Status: waiting on partner selection; the enclosure must fit the partner board's thermal and antenna constraints.

| Path | Contents |
| --- | --- |
| `enclosure/` | Onshape/Fusion exports: STEP for editing, STL/3MF for printing |
| `kicad/` | Accessory boards, if any |
| `models/` | GLB files for the website's exploded view |
| `docs/` | Measurements, thermal and power test results |

## Model conventions (for the website)

- One GLB per part group, named nodes: `enclosure_top`, `enclosure_bottom`, `heatsink`, `board`, `hdmi_plug`, `remote`.
- Origin at the assembled position; each part explodes along its own axis.
- Optimise with `gltf-transform optimize --compress meshopt`. Budget: hero GLB under 1 MB, whole scene under 4 MB.

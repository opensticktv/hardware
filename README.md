# OpenStick hardware

The OpenStick mainboard, enclosure, remote shell and accessories, plus 3D models for the website.

Licensed under the [CERN Open Hardware Licence v2, Strongly Reciprocal](LICENSE).

OpenStick is open hardware you can buy ([decision 0009](https://github.com/opensticktv/openstick/blob/main/decisions/0009-open-hardware-locked-by-default.md)). The mainboard is designed here from the chip's certified reference design. Sold units are certified and ship locked so 4K streaming works; owners can unlock their own unit. If you build a board from these files yourself, it has no factory-installed streaming keys, so subscriptions play at 720p.

Status: waiting on chip and design-house selection. Publishing the board depends on the chip vendor's terms.

| Path | Contents |
| --- | --- |
| `enclosure/` | Onshape/Fusion exports: STEP for editing, STL/3MF for printing |
| `kicad/` | Mainboard and accessory boards |
| `models/` | GLB files for the website's exploded view |
| `docs/` | Measurements, thermal and power test results |

## Model conventions (for the website)

- One GLB per part group, named nodes: `enclosure_top`, `enclosure_bottom`, `heatsink`, `board`, `hdmi_plug`, `remote`.
- Origin at the assembled position; each part explodes along its own axis.
- Optimise with `gltf-transform optimize --compress meshopt`. Budget: hero GLB under 1 MB, whole scene under 4 MB.

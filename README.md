# Bear's Den · invasive treatment brief

Live site: https://ryanpocasset.github.io/BearsDen_InvasiveTreatment_2026/
Repository: https://github.com/RyanPocasset/BearsDen_InvasiveTreatment_2026

Static web map of the two invasive treatment areas at Bear's Den, Pocasset Cedar Swamp, Tiverton, Rhode Island, from the PPLT field survey of 21 November 2026. Prepared for Whipple Tree by PPLT AGIKS, Pocasset Pokanoket Land Trust.

## Publish with GitHub Pages

1. Upload everything in this folder to the root of the `main` branch, keeping the folders (`data/`, `img/`, `lib/`, `photos/`). Files with the same name replace the old ones.
2. In the repository: **Settings → Pages → Build and deployment**, set Source to **Deploy from a branch**, Branch **main**, folder **/ (root)**, and save.
3. After a minute or two the site updates at https://ryanpocasset.github.io/BearsDen_InvasiveTreatment_2026/ (the path is case-sensitive).

On a free GitHub account, Pages needs a public repository, and the published site can be opened by anyone with the link. The page carries a `noindex` tag so search engines leave it out; delete that `<meta name="robots">` line in `index.html` if you want it findable.

## Preview locally

The page loads its layers with `fetch()`, so it needs a web server rather than a double-click on `index.html`:

```
python3 -m http.server 8000
```

then open http://localhost:8000/.

## What's in it

| Path | Contents |
|---|---|
| `index.html` | The page: brief, map and popups. The area cards and the summary numbers are built into it. |
| `data/treat.geojson` | Treatment patches by severity, with species composition and the lot each sits on |
| `data/units.geojson` | The two treatment areas, BD-4 and BD-1 |
| `data/incl.geojson` | Honeysuckle and rose growing inside the knotweed and reed |
| `data/stream.geojson` | The ditch |
| `data/tract.geojson`, `data/neighbors.geojson` | PPLT lots and the neighbouring lots |
| `data/summary.json` | Totals used by the page |
| `img/` | RIGIS aerials: March 2026 leaf-off, July 2022 leaf-on, and the March 2026 3-inch orthophoto of the west end |
| `photos/` | Field photos shown in the area popups |
| `lib/` | Leaflet 1.9.4 (BSD-2-Clause, see `lib/LEAFLET-LICENSE.txt`) |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Sources and notes

PPLT field survey, 21 November 2026; RIGIS aerial photography (March 2026, July 2022); USGS 3DEP lidar, Rhode Island 2022; Town of Tiverton Plat 103 (8 April 2026). Lot lines are the town's assessor lines, not a survey.

Withheld from this map: photo locations; photos with people, houses or signs; stone features. Cultural information stays under PPLT and Tribal governance.

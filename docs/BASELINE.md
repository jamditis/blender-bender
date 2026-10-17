# Inspected MSU baseline

Audit date: October 17, 2026. Source: untouched October 16 Drive snapshot, main and north scenes, opened in Blender 4.5.14 LTS with script auto-execution disabled. The archive and scene hashes are recorded in [the manifest](../manifests/source-assets.json).

## Scope and limits

The four ZIPs contain 654 extracted files totaling approximately 538 MB. This is extracted content size, not the compressed archive total. Main has 4,081 scene objects and north has 3,370. Name-based counts below are inspection aids, not accuracy/completeness percentages.

Original reference-photo folders, raw `.las`/`.laz` point clouds, `.npz`/`.npy` terrain products, `.geojson` geometry, and staged Cole measurement JSON were absent from the snapshot. Embedded descriptions and height notes are not substitutes for independent measurement evidence.

Source scripts describe NAD83(2011) / New Jersey (ftUS), EPSG:6527, with a local origin derived from longitude -74.19720, latitude 40.86000 and rounded to the nearest 10 feet. Local modeling units are meters with a 1200/3937 foot conversion. This is recorded source provenance; independently verify the transform and vertical datum before a survey-grade claim.

## Building inventory

| Building/site | Inspected baseline | Priority gap |
| --- | --- | --- |
| CCOM | Main: 895 named meshes, lounge/lab/newsroom elements | Grade, terrace and several interiors explicitly unverified |
| Morehead Hall | Main: 150 named meshes, exterior/window assets | Window sizes and secondary facades unverified; interior scope unresolved |
| Susan A. Cole Hall | Main: five wall/roof/trim meshes; no named cupola | Recover or independently establish missing measurement evidence; current references require verified building identity |
| Alexander Kasser Theater | Main: four shell/roof/trim meshes | Drawings need campus registration; loggia, glazing tower and interior detail absent by name |
| Red Hawk Deck | North: parking construction and separate core | Grid, ramp and parapet dimensions unverified |
| George Segal Gallery | No named geometry found | Integrate at Deck level 4, with exterior corridor beside Kasser |
| Outdoor amphitheater | No named geometry found | Establish exact footprint, seating geometry and grade; current row count conflicts with historical 22-tier description; neither establishes dimensions |
| Sprague Library | Main: two shells; north: 17 named meshes and detailed collections | Reconcile duplicate levels of detail before integration |

Name-based absence does not establish that no related hidden geometry exists. Inspect the actual scene before making replacements.

Kasser's western wall extent slightly exceeds the main high-detail terrain boundary in the audited file. Check terrain support and tile continuity. The standalone Sprague material/motion study is excluded from the geographic baseline.

## Review sequence

1. Establish source/coordinate/asset ownership register and map overlap.
2. Ground each building change in identified references and measurements.
3. Save a separate bounded variant, preserving source hashes.
4. Inspect dimensions, dependencies, uncertainty and still comparisons.
5. Integrate only through a reviewed handoff. No video production.

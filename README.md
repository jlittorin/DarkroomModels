# Models

Model files for downloads.

## upernet-convnext-tiny-ade-sky-512.onnx (release models-2026-11)

UperNet with a ConvNeXt-T backbone, trained on ADE20K, exported to ONNX with only the sky class's probability as output
(512 × 512). Used by Sky masks.

- Weights: [openmmlab/upernet-convnext-tiny](https://huggingface.co/openmmlab/upernet-convnext-tiny), commit
  876ffc56b819a829448f7e81e9f8606deef6fb65, MIT licence (converted from mmsegmentation, Apache-2.0; ConvNeXt, MIT).
- Exported with Darkroom's `tools/ModelExport/export_ade_sky.py`.
- SHA-256: 2adeeffb56c310d937547859c03e0032112808656c5f7385128c8f426b26a3ba
- 
## gazetteer-geonames-20261104.gaz (release gazetteer-2026-11)

Place names for Darkroom's map (GEO.3): searching places by name as they are typed, and naming the place a photo was taken
at, on the PC. 369,253 places: populated places of 500 people or more and every one in Sweden, first-level regions,
countries, and natural features (islands, lakes, mountains, parks …) with three names or more in GeoNames, and every named
one in Sweden. Shown by GeoNames' own names, found by their English, Swedish and local ones too.

- Data: [GeoNames](https://www.geonames.org), CC BY 4.0, the dumps of 2026-11-04 (allCountries, alternateNamesV2,
  admin1CodesASCII, countryInfo).
- Built with Darkroom's `tools/GazetteerBuild`: zstd over the places and a sorted search index.
- SHA-256: dda59984cea1e3e789a32d8415c805637483ba6f6089dfb332c44ee4e511bc66

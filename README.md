# Models

Model files for downloads.

## upernet-convnext-tiny-ade-sky-512.onnx (release models-2026-11)

UperNet with a ConvNeXt-T backbone, trained on ADE20K, exported to ONNX with only the sky class's probability as output
(512 × 512). Used by Sky masks.

- Weights: [openmmlab/upernet-convnext-tiny](https://huggingface.co/openmmlab/upernet-convnext-tiny), commit
  876ffc56b819a829448f7e81e9f8606deef6fb65, MIT licence (converted from mmsegmentation, Apache-2.0; ConvNeXt, MIT).
- Exported with Darkroom's `tools/ModelExport/export_ade_sky.py`.
- SHA-256: 2adeeffb56c310d937547859c03e0032112808656c5f7385128c8f426b26a3ba

## darkroom-dust-unet-2026-11.onnx (release models-2026-11)

Darkroom's dust network: a U-Net that finds dust, hairs and scratches in a film scan's visible light, for scratch removal
where there is no IR (B&W negatives, Kodachrome, scans made without IR). Trained by Darkroom's `tools/DustTrain` on the IR
masks of the author's own scans: 396 colour-negative and slide scans from a Plustek OpticFilm 8300i. The weights hold no
image.

- Weights: the author's own, MIT licence ([LICENSE-darkroom-dust-unet.txt](LICENSE-darkroom-dust-unet.txt)). A later
  network is a new file, `darkroom-dust-unet-<version>.onnx`, in a release of its own (`models-<version>`), under the same
  licence.
- On 32 held-out scans: 80 % of the visible defects found at 81 % precision on colour negatives, 39 % at 80 % on slides.
- SHA-256: f0e100d1ac031153dee806346cca5f1d96658b9cc143ebb87bee4f7f066edf8d

## gazetteer-geonames-20261104.gaz (release gazetteer-2026-11)

Place names for Darkroom's map (GEO.3): searching places by name as they are typed, and naming the place a photo was taken
at, on the PC. 369,253 places: populated places of 500 people or more and every one in Sweden, first-level regions,
countries, and natural features (islands, lakes, mountains, parks …) with three names or more in GeoNames, and every named
one in Sweden. Shown by GeoNames' own names, found by their English, Swedish and local ones too.

- Data: [GeoNames](https://www.geonames.org), CC BY 4.0, the dumps of 2026-11-04 (allCountries, alternateNamesV2,
  admin1CodesASCII, countryInfo).
- Built with Darkroom's `tools/GazetteerBuild`: zstd over the places and a sorted search index.
- SHA-256: dda59984cea1e3e789a32d8415c805637483ba6f6089dfb332c44ee4e511bc66

## lensfun-db-20261104-52cf1a7.zip (release lensfun-2026-11)

Lens profiles for Darkroom's lens corrections (LNS.5): the distortion, vignetting and lateral chromatic aberration of lenses
whose camera raws record no corrections of their own.

- Data: [lensfun](https://github.com/lensfun/lensfun)'s lens database, `data/db` at commit
  52cf1a7b0e82e07e0ecaa3391ee5106a6dd1ee54 (2026-11-04), copyright the lensfun project's contributors,
  [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). The 56 XML files are unchanged.
- Zipped with a README by Darkroom's `tools/LensfunPack`. Darkroom reads the XML itself and does not use lensfun's library.
- SHA-256: 02821ba92cb3933912ee128f503eb3a9c30a17b7cf5bfcb0c1eeff0246b554a9

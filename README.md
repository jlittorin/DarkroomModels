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
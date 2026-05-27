# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working in this repository.

## Project Overview

**Red Chili Pepper Pests** — an image classification dataset and model for detecting pests on red chili peppers. The 4 pest classes are:

| Code | Pest (Indonesian) |
|------|-------------------|
| MP   | Kutu Daun (Aphid) |
| BT   | Kutu Kebul (Whitefly) |
| T    | Thrips |
| C    | Ulat (Caterpillar) |

## Dataset

The dataset lives in `datasets/RedChiliPepperPestsDataset/` and follows the **YOLO classification format** (train/val/test split with images and labels directories). The `data.yaml` at the dataset root defines the class names and split paths.

- `train/images/` — training images
- `val/images/` and `val/valid/images/` — validation images (two subdirectories)
- `test/images/` — test images
- Corresponding `labels/` directories contain YOLO-format annotation files

A raw `archive.zip` (compressed dataset) also exists at `datasets/archive.zip`.

## Notebook

`notebooks/Template_Submission_Akhir.ipynb` is a Jupyter notebook template (in Indonesian/Dicoding style) for the final submission. It follows this workflow:

1. **Data Preparation** — loading and preprocessing, splitting dataset
2. **Modeling** — building the classification model
3. **Evaluation & Visualization** — metrics and plots
4. **Model Conversion** — exporting the trained model
5. **Inference** — optional prediction on new images

## Working in This Repo

- This is primarily a **dataset + notebook** project, not a package-based codebase.
- There are no build tools, lint configs, or test runners — development happens in the Jupyter notebook.
- To run the notebook: `jupyter notebook notebooks/Template_Submission_Akhir.ipynb` (or use JupyterLab / VS Code).
- The dataset is expected to be pre-extracted from `archive.zip` into `RedChiliPepperPestsDataset/`.

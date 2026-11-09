# Fire & Smoke Detection for BC Wildfires (YOLOv8n fine-tuning)

IAT360 Computer Vision final project. Supervised **object detection** with two classes, `0 = fire` and `1 = smoke`.
We fine-tune a pretrained YOLOv8n (Ultralytics) on a public Roboflow fire/smoke dataset and test it on our own set of
90 images (30 per team member) from BC and other wildfire scenes, including 41 negative images (fog, clouds, steam, lights, kettles, ...).


## Repository layout

```
ComputerVisionProject.ipynb   all code: baseline, tuning, combined model, evaluation
config_roboflow.yaml          example config for the Roboflow training data
bc_test/                      our own test set (YOLO format)
  images/                     EMPTY on GitHub (.gitkeep); see "Test images" below
  labels/                     90 YOLO .txt labels (class x_center y_center width height, normalized; empty file = negative image)
  config_bc.yaml              dataset config used for evaluation
  SOURCES.md, sources.csv     where every test image comes from (own photo or source page)
results/                      metrics, curves, confusion matrices, args of every run (weights only for the baseline)
screenshots/                  screenshots of training and evaluation steps
```

## Data

**Training / validation data (existing dataset).** Roboflow Universe dataset *including1_2* (22,173 images, CC BY 4.0, train/valid splits).
It is not copied here (about 3 GB). Download it from Roboflow Universe in **YOLOv8** format, and its `config.yaml` is the one used for training.
https://universe.roboflow.com/fire-detection-vegji/including1_2/dataset/1
I trained on 30% of the training images (`fraction=0.3`, 4,656 images) to accelerate iterative experimentation and optimize hyperparameter exploration under constrained computational resources and validated on the full valid split (6,652 images, 13,268 boxes).

**Test data (new data, our labels).** `bc_test/`: 90 images, 49 with objects (148 boxes: 112 fire in 45 images, 36 smoke in 30 images) and 41 negatives.
11 images are photos taken by team members; the other 79 come from news and web pages.

### Test images
We do not have the right to redistribute the web and news images, so `bc_test/images/` is **empty in this repository**
(it only contains `.gitkeep` to show the folder structure). To rebuild the test set, download every image listed in
[`bc_test/SOURCES.md`](bc_test/SOURCES.md) and save it as `bc_test/images/<file>.<ext>`; the file name (without extension) must match the label file in `bc_test/labels/`.
After that the repository can be used as is.

## How to run

1. Python 3.10+ with `pip install ultralytics` (a CUDA build of PyTorch is recommended; I used a desktop with GTX 1660 Ti).
2. Download the Roboflow dataset (YOLOv8 format) and put the test images in `bc_test/images/` as described above.
3. Open `ComputerVisionProject.ipynb` **from the repository root**, and set `DATA` in the first code cell to the Roboflow `config.yaml`.
4. Run the cells in order. Training outputs go to `runs/` (git-ignored); summaries are written to `results/`.

## Experiments

| Part | What changed vs. baseline |
|---|---|
| Baseline | YOLOv8n, epochs=10, imgsz=640, batch=16, fraction=0.3, `optimizer=auto` (Ultralytics picked AdamW, lr=0.001667) |
| Epochs | 15 / 20 / 30 |
| Image size | 416 / 512 / 704 |
| Learning rate (`lr0`) | 0.0005 / 0.003 / 0.006 (AdamW set explicitly) |
| Combined model | epochs=30, imgsz=512, AdamW lr0=0.0005 |

Per-run numbers are in `results/tuning_*.csv` and `results/test_eval_90.csv` (all models on the final 90-image test set).

## Main results

| Model | Valid P / R / mAP50 / mAP50-95 | Test (90 images) P / R / F1 / mAP50 / mAP50-95 |
|---|---|---|
| Baseline | 0.756 / 0.704 / 0.777 / 0.469 | 0.323 / 0.407 / 0.360 / 0.233 / 0.096 |
| Combined | 0.805 / 0.740 / 0.824 / 0.517 | 0.348 / 0.362 / 0.355 / 0.280 / 0.125 |

The large gap between validation and our own test set is a domain gap (different image sources, small or faint flames,
fog and steam that look like smoke), not overfitting: training loss was still falling when training stopped.
See the report for the error analysis with correct and incorrect examples.

## Screenshots
Screenshots of the training and evaluation steps are in [`screenshots/`](screenshots/).

## Credits
- Ultralytics YOLOv8: https://github.com/ultralytics/ultralytics
- Training data: Roboflow Universe, *including1_2* (CC BY 4.0)
- Test images: see `bc_test/SOURCES.md`

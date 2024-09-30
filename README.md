# COCO to YOLO Converter

Converts COCO annotations to YOLO format.

## Features

- Converts COCO annotations to YOLO format
- Downloads and filters images/labels from COCO URLs if missing locally
- Organizes images/labels into required structure

## Setup

```bash
$ pip install -r requirements.txt
```


## Usage

```shell
./coco_to_yolo.py --train-ann <path_to_train_annotations>
                  --val-ann <path_to_val_annotations>
                  --dataset_dir <path_to_output_directory>
                 [--test-ann <path_to_test_annotations>]
                 [--train-img-dir <train_images_directory>]
                 [--val-img-dir <val_images_directory>]
                 [--test-img-dir <test_images_directory>]
                 [--train-label-dir <train_labels_directory>]
                 [--val-label-dir <val_labels_directory>]
                 [--test-label-dir <test_labels_directory>]
                 [--train-txt <train_txt_file_name>]
                 [--val-txt <val_txt_file_name>]
                 [--test-txt <test_txt_file_name>]
                 [--cats <space_separated_categories>]
                 [--cat-file <path_to_category_file>]
```

- `--train-ann`: path to the COCO training annotation JSON file.
- `--val-ann`: path to the COCO validation annotation JSON file.
- `--cats`: space-separated list of categories to include (e.g., person dog cat).
- `--cat-file`: file containing newline-separated categories to include.

### Output

The default script will create the following structure in the specified `dataset_dir`:

```
dataset_dir/
├── images/
│   ├── train/
│   ├── val/
│   └── test/
├── labels/
│   ├── train/
│   ├── val/
│   └── test/
├── train.txt
├── val.txt
└── test.txt
```

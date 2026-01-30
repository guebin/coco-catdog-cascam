# COCO Cat/Dog Dataset for CasCAM

Cat and dog images from COCO with synthetic text artifacts for interpretability research.

## Structure

```
coco-catdog-cascam/
├── original/           # 512×512 clean images (8,640 files)
├── with_artifact/      # 512×512 images with "Cat"/"Dog" text overlays
├── artifact_boxes/     # Binary masks (1=artifact, 0=background)
└── annotations/
    └── trimaps/        # Binary masks (1=foreground, 0=background)
```

## File Naming

Label extraction via filename capitalization:
- **Cat**: `Coco_cat_00000.jpg` (capital 'C')
- **Dog**: `coco_dog_00000.jpg` (lowercase 'c')

## Usage

```bash
# Clone CasCAM
git clone https://github.com/guebin/cascam.git
cd cascam

# Clone this dataset
git clone https://github.com/guebin/coco-catdog-cascam.git data/coco-catdog-cascam

# Run CasCAM
python run.py --data_path ./data/coco-catdog-cascam/with_artifact/
```

## Statistics

| Item | Value |
|------|-------|
| Total images | 8,640 |
| Resolution | 512×512 |
| Artifact area | ~2-5% of image |

## Attribution

- **Source**: [COCO Dataset](https://cocodataset.org/)
- **Modifications**: Resized to 512×512, synthetic text artifacts added

Research use only. See COCO terms of use for commercial deployment.

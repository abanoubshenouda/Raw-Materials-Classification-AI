# Raw Materials Classification
**Bonus Feature**  
**Texture Robustness under Varying Lighting, Shadow & Glare Conditions**  
→ Model recognizes materials correctly even under different illumination, shadow, or glare conditions, simulating real factory settings.

## Dataset ( GitHub Requirements)
- **Main Dataset**: [Kaggle – Raw Material Images for Classification](https://www.kaggle.com/datasets/haaroonafroz/material-dataset-new?utm_source)
- **Additional Custom Images**: Collected by team under extreme lighting, deep shadows, and strong glare (for bonus robustness)  
## Models Implemented (3 architectures as required)

| Model            | Source       | Role                     |
|------------------|--------------|--------------------------|
| ResNet18         | torchvision  | Baseline                 |
| EfficientNet-B1  | timm         | Best accuracy            |
| MobileNetV3      | torchvision  | Lightweight & fast       |
## Bonus Features 
- Heavy augmentations using **Albumentations** (RandomBrightnessContrast, RandomShadow, GaussNoise, MotionBlur, etc.)
- **Grad-CAM** visualization in Streamlit GUI
- Top-3 predictions with confidence scores
- Robust performance under factory-like lighting conditions
## Setup Instructions
```bash
pip install -r requirements.txt
streamlit run gui/GuiApp.py
**raw-materials-classification/**
├── data/
│   ├── custom_lighting_images/     # our custom images 
│   └── README.md                   # dataset description
├── models/         # trained.pth files
├── gui/            # GuiApp.py
├── src/            # DataLoader.py, Train.py, Model_defs.py
├── docs/           # report + confusion matrix + graphs
├── notebooks/      # EDA & experiments
├── requirements.txt
└── README.md

##Team Members & Roles (6 members )
Name               GitHub Username        Main Responsibility
Doha Mohamed       Doha-Mohamed2005       "GUI Development, Grad-CAM, Repo Owner"
Zeinab Mahmoud     0xZeinab               "GUI Assistance & Grad-CAM Integration"
Ahmed Ashraf       ahmedashrafmedo        "Training, Testing, Evaluation"
Abanoub Shenouda   Abanoub Shenouda       "Training, Testing, Evaluation"
Farid Elsharkawi   FaridElsharkawi        "Data Collection & Heavy Augmentations"
Omar Ragab         Omarragab66            "Data Collection & Preprocessing"

Results(will be updated after final training)
ResNet18:       xx%
EfficientNet-B1: xx% ← Best
MobileNetV3:     xx%
Confusion matrix & accuracy graphs → docs/ folder
# Raw Materials Classification
**Goal**: Classify raw materials (wood, metal, plastic, glass, etc.) based on texture  
**Bonus Challenge Implemented**: Texture Robustness under Varying Lighting, Shadow & Glare Conditions
## Dataset
Kaggle + custom images collected under different lighting conditions
## Models
- ResNet18
- EfficientNet-B1 (timm)
- MobileNetV3
## Bonus Features
- Heavy augmentations using Albumentations (RandomBrightnessContrast, GaussNoise, Shadow, etc.)
- Grad-CAM visualization in Streamlit GUI
- Top-3 predictions with confidence scores
## Setup
```bash
pip install -r requirements.txt
streamlit run gui/GuiApp.py
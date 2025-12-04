# Osteoporosis_DataSet

Group Project for AI4ALL Gorup 11A - Osteoporosis Diagnosis 

## What Is This Project?

An AI system that analyzes knee X-rays to detect osteoporosis (bone density loss) and help identify patients at risk. Uses deep learning to automatically classify X-rays into three categories: Normal, Osteopenia (early bone loss), and Osteoporosis (severe bone loss).

## Why It Matters

- **Early Detection**: Identifies bone density issues before fractures occur
- **Accessibility**: Automated screening reduces need for expensive DEXA scans
- **Speed**: Analyzes X-rays in seconds vs. manual review

## How It Works

1. **Upload** a knee X-ray image
2. **AI analyzes** using 2 trained convoluted neural networks
3. **Get results** with diagnosis and confidence score

Our larger system aims to combine predictions from three different AI models (ensemble learning) for more accurate and reliable results.

## Key Features

✅ **85% accuracy** on test dataset  
✅ **3-model ensemble** for robust predictions 
(not fully integrated for dashboard deployment, however 2 ResNet models were utilized for app)
✅ **Web dashboard** with easy-to-use interface  
✅ **Real-time analysis** with visual confidence metrics

## Technologies Used

- **AI Models**: ResNet18, ResNet50, EfficientNet-B3
- **Framework**: PyTorch (deep learning)
- **Interface**: Streamlit (web application)
- **Dataset**: 1,900+ knee X-ray images from Kaggle

## Quick Start
```bash
# Install dependencies
pip install streamlit torch torchvision plotly pandas

# Run the dashboard
streamlit run osteoporosis_dashboard_final.py

# Upload an X-ray and get instant results!
```

## Results Summary

| Model | Accuracy | Specialty |
|-------|----------|-----------|
| Sydney's ResNet18 | 83% | Fully fine-tuned using NVIDIA L4 GPU |
| Michael's ResNet50 | 78% | Partially fine-tuned |
| Ensemble (Combined) | 85% | Best overall performance |

## Ethical Considerations

⚠️ **Important**: This is a research tool, not FDA-approved medical software. All predictions should be reviewed by qualified healthcare professionals; there should always be a human reviewer to validate predictions

**Bias Mitigation:**
- Used weighted sampling to balance class representation
- Data augmentation to increase diversity
- Ensemble approach to reduce individual model bias

**Known Limitations:**
- Dataset from single source (may not generalize to all X-ray equipment)
- Should be used as a screening tool, not definitive diagnosis

## Team

- **Sydney** - Model development (ResNet18)
- **Michael** - Model development (ResNet50)
- **Dia** - Model development (EfficientNet-B3)
- **Sampada** - Data sourcing, research, and UI/UX

## Acknowledgments

**Dataset**: Osteoporosis X-Ray Dataset from Kaggle  
https://www.kaggle.com/datasets/mohamedgobara/multi-class-knee-osteoporosis-x-ray-dataset

**References**:
- Dias et al. (2024). "Osteoporosis Screening: Leveraging EfficientNet with Panoramic Radiography Imaging." *Biomedical Signal Processing and Control*. https://doi.org/10.1016/j.bspc.2024.107031
- Sözen, Tümay, Lale Özışık, and Nursel Çalık Başaran. "An overview and management of osteoporosis." European journal of rheumatology 4, no. 1 (2016): 46.

AI4ALL Career Accelerator Group 11A, Fall 2025 Cohort

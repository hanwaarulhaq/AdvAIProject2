# Plant Disease Classification Project

This repository contains implementations of various deep learning models for plant disease classification using datasets like PlantVillage and PlantDoc.

## Models Implemented

- **Custom Faster R-CNN**: Model for tomato disease detection
- **Vision Transformer**: Implementation with PlantVillage dataset (v1 and v2)
- **R-CNN**: Original and custom implementations for plant classification
- **PlantDoc Faster-RCNN**: Implementation from scratch

## Vision Transformer v2 (PlantVillage Dataset)

### Model Architecture
- **Patch Size**: 16x16
- **Embedding Dimension**: 512
- **Depth**: 8 transformer blocks
- **Number of Heads**: 8
- **MLP Ratio**: 4.0
- **Dropout**: 0.15
- **Total Parameters**: 85,876,766
- **Number of Classes**: 38

### Training Configuration
- **Image Size**: 256x256
- **Batch Size**: 64
- **Epochs**: 25 (with early stopping, patience=7, min_epochs=12)
- **Learning Rate**: 0.0003 (with 5-epoch warmup and cosine decay)
- **Weight Decay**: 0.05
- **Data Augmentation**: Random crop, flip, rotation, color jitter, erasing
- **Loss Function**: Cross-Entropy with label smoothing (0.1)

### Results
- **Best Validation Accuracy**: 98.32% (at epoch 22)
- **Test Accuracy**: 97.95%
- **Test Precision**: 97.98%
- **Test Recall**: 97.95%
- **Test F1-Score**: 97.95%
- **Training Time**: 120.9 minutes

### Top 5 Best Performing Classes (F1-Score)
- Corn_(maize)___Common_rust_: 100.0%
- Corn_(maize)___healthy: 100.0%
- Grape___Leaf_blight_(Isariopsis_Leaf_Spot): 100.0%
- Cherry_(including_sour)___healthy: 100.0%
- Tomato___healthy: 100.0%

### Bottom 5 Worst Performing Classes (F1-Score)
- Apple___Cedar_apple_rust: 87.80%
- Corn_(maize)___Cercospora_leaf_spot Gray_leaf_spot: 88.89%
- Potato___healthy: 88.89%
- Corn_(maize)___Northern_Leaf_Blight: 93.33%
- Tomato___Early_blight: 94.52%

### Generated Outputs
- `best_model.pth`: Best model checkpoint
- `confusion_matrix_test.png`: Test set confusion matrix
- `confusion_matrix_val.png`: Validation set confusion matrix
- `training_curves.png`: Training and validation loss/accuracy curves
- `per_class_metrics.png`: Per-class performance metrics
- `sample_predictions.png`: Sample prediction visualizations
- `classification_report.txt`: Detailed classification report
- `classification_report.csv`: Classification report in CSV format
- `metrics_summary.csv`: Summary of key metrics

## Notebooks

- `CustomRCNN.ipynb`
- `PlantDocFasterRCNN.ipynb`
- `PlantDocRCNN2.ipynb`
- `plantvillage-visiontransformer-v2.ipynb`
- `plantvillage-visiontransformer.ipynb`

## Documentation

- `Plant Disease Classification using Vision Transformer.docx`
- `Git Commit History.docx`

## Demo

- `Demo.mp4`: Demonstration video of the models in action

## Git Commit History

- `53c6593ff51329f268344a65e40c348fd8c7786f` feat: add demo video
- `fd823b858fa91c8b34d46c49ea18da4f393564b4` feat: add vision transformer v2 notebook and documentation
- `a4205aadb1a11f36d0af2c68b0a7ef83e0410b40` Vision Transformer with PlantVillage dataset
- `21b0f38bac32fb2d55481e39c8c77b422237d2d0` Rename PlantDocRCNN.ipynb to PlantDocFasterRCNN.ipynb
- `4e156cbf03132161c1b54af46805d56f52fbdd0b` Delete PlantDocRCNN2
- `64e41f970922ef13b68f3cb6518a7839ff1fe124` Add R-CNN implementation for plant classification
- `52d0c2df54ddc5b08d16526e7e682faa7903bfb` Add original R-CNN implementation from scratch
- `5cb8f9752f2a7408c6a46896e3da0b9a5e87e6a5` Add PlantDoc Faster-RCNN implementation from scratch
- `68ce7cdf903d393594dcebd9b68f527cae0c6` Add custom Faster R-CNN model for tomato disease detection
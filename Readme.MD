# Malaria Diagnosis with CNNs - Group 13

Binary classification of blood-cell microscopy images as **Parasitized** or **Uninfected** using convolutional neural networks.

**Dataset:** NIH Malaria Cell Images (27,558 images, balanced)
**Framework:** TensorFlow / Keras
**Course:** ALU — Deep Learning Formative 2, June 2026

---

## Team and Models

| Member | Model | Type |
|---|---|---|
| Hasbiyallah Umutoniwabo | Baseline CNN | Custom (simple 2-block reference model) |
| Jean | Improved CNN | Custom (deeper + data augmentation) |
| Hamse Jama | VGG16 | Pre-trained transfer learning |
| Alliane Umutoniwase | MobileNetV2 | Pre-trained transfer learning |
| Bakhit | ResNet | Pre-trained transfer learning |

---

## Results Summary

| Model | Best Accuracy | F1 | AUC |
|---|---|---|---|
| Baseline CNN | 93.88% | 0.9398 | 0.9812 |
| Improved CNN | 96.95% | 0.9695 | 0.9944 |
| VGG16 | 93.60% | 0.9400 | 0.9833 |
| MobileNetV2 | 95.60% | 0.9570 | 0.9910 |
| ResNet | Pending | Pending | Pending |

Each member ran 7 experiments varying hyperparameters, architecture choices, and training strategies. The best experiment per model is shown above.

---

## Repository Structure

```
Malaria_Baseline_CNN_Hasbiyallah.ipynb   - Baseline CNN (7 experiments)
Malaria_Improved_CNN_Jean.ipynb          - Improved CNN (7 experiments)
Malaria_VGG16_Hamse.ipynb               - VGG16 transfer learning (7 experiments)
Malaria_MobileNetV2_Alliane.ipynb        - MobileNetV2 transfer learning (7 experiments)
Malaria_ResNet_Bakhit.ipynb             - ResNet transfer learning (7 experiments)
README.md                                - This file
```

---

## How to Run

1. Open any notebook in Google Colab
2. Set the runtime to GPU: Runtime → Change runtime type → T4 GPU
3. Run all cells from top to bottom
4. The dataset downloads automatically from the NIH source — no manual setup needed

---

## What Each Notebook Contains

- Problem introduction and architecture explanation
- Dataset loading and preprocessing
- 7 documented experiments with one hyperparameter changed at a time
- Results table with accuracy, precision, recall, F1, and AUC for every experiment
- Learning curves, confusion matrix, and ROC curve for every experiment
- Error analysis including overfitting and false negative diagnosis
- Best model saved as a .keras file

---

## Key Findings

- The Improved CNN, trained from scratch, outperformed all pretrained models. Good regularization and augmentation mattered more than ImageNet pretraining on this dataset.
- Fine-tuning pretrained models was far more effective than using frozen features. MobileNetV2 jumped from 93.6% frozen to 95.6% after fine-tuning the top 40 layers.
- Recall is the most important metric for this task. A missed infection is more dangerous than a false alarm. MobileNetV2 achieved the highest recall among pretrained models at 96.80%.
- The Baseline CNN serves as the reference lower bound and showed mild overfitting, addressed through dropout regularization.

---

## References

- Rajaraman et al. (2018). Pre-trained CNNs as feature extractors for malaria detection. PeerJ.
- Howard et al. (2017). MobileNets. arXiv:1704.04861.
- He et al. (2016). Deep residual learning for image recognition. CVPR.
- Simonyan and Zisserman (2015). VGG16. ICLR.
- WHO (2022). World Malaria Report. Geneva.

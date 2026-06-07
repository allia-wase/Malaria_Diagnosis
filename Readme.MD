# Malaria Diagnosis with CNNs — Group 17

Five CNN models classifying blood-cell images as Parasitized or Uninfected
(NIH malaria dataset). One baseline, one improved, three transfer-learning models.

## 1. What's in this repo
- One notebook per member (your model + 7 experiments)
- A shared results folder where every experiment is saved
- The consolidated report

## 2. Add the shared Drive folder
Our shared results folder: https://drive.google.com/drive/...  (paste real link)

Open the link -> click **Add shortcut to Drive** (or right-click -> Add shortcut
to Drive) -> choose **My Drive** -> **Add**. It will then show up in your own Drive.

## 3. Open YOUR notebook
In the shared folder, right-click your file -> **Open with -> Google Colaboratory**.

- **Hasbiyallah Umutoniwabo** -> `Malaria_Baseline_CNN_Hasbiyallah.ipynb`
- **Jean Muhire** -> `Malaria_Improved_CNN_Jean.ipynb`
- **Hamse Jama** -> `Malaria_VGG16_Hamse.ipynb`
- **Bakhit Mahamat** -> `Malaria_ResNet50_Bakhit.ipynb`
- **Alliane Umutoniwase** -> `Malaria_MobileNetV2_Alliane.ipynb`  (MobileNetV2 + final compilation)

## 4. Set GPU + run
- **Runtime -> Change runtime type -> T4 GPU -> Save**
- **Runtime -> Run all**
- Approve the Google Drive mount when asked.

## 5. Results & report
- Each model produces its metrics (Accuracy, Precision, Recall, F1, AUC) and its
  three plots (learning curves, confusion matrix, ROC), saved to the shared folder.
- Alliane compiles all five into the consolidated comparison and final report.

> **Do NOT edit the top section** (config, data pipeline, training functions) --
that's what keeps all five models compared fairly. Work only in your own model
section.

> **If you get disconnected:** reopen, Run all again, re-approve the mount.

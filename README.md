# CMPE258 - Deep Learning Assignment: MedNIST Classification + Knowledge Distillation

## 🧠 Project Overview

This assignment implements a complete deep learning pipeline using the MedNIST dataset, including:
1. A custom CNN model trained with various training options.
2. Evaluation of performance using accuracy and inference time metrics.
3. Visual comparisons using matplotlib.
4. Model export and loading for inference.
5. Integration with HuggingFace ViT for knowledge distillation (Excellent rating).

---

## 📁 Dataset
- **Source**: MedNIST (https://github.com/Project-MONAI/tutorials/blob/main/2d_classification/)
- **Preprocessing**: Resized to 64x64, grayscale converted, normalized.

---

## 🧰 Models
### Custom CNN
- 2 Conv layers + ReLU + MaxPool
- 1 Fully Connected layer
- Trained using Adam optimizer + StepLR scheduler

### HuggingFace ViT (Distillation)
- Student: `WinKawaks/vit-tiny-patch16-224`
- Teacher: Custom CNN (converted via grayscale injection for compatibility)

---

## 🧪 Experiments
- **Training configs tried**: augmentations, optimizer/scheduler tweaks
- **Evaluation**: Accuracy and latency using inference timing
- **Visualization**: Plots for accuracy and timing, plus prediction samples

---

## 🧠 Knowledge Distillation (Excellent Grade)
- Used HuggingFace `Trainer` with custom `DistillationTrainer`
- Injected grayscale features to compare teacher-student logits
- Compared results post-training

---

## 📊 Results
- ✅ Accuracy on test set reported
- ✅ Inference time measured
- ✅ Random 10-image predictions shown with matplotlib

---

## 🚀 Running the Code
```bash
# Make sure MedNIST is in ./data/MedNIST
python assignment.py
```

To run distillation:
```bash
python distillation.py
```

---

## 📎 Submission
- 📘 Report: See `CMPE258_HW_Report.docx`
- 📄 Notebook: See `hw_assignment.pdf`
- 🗂️ Code: See `assignment.py`, `distillation.py`

---

## 👨‍💻 Author
- Puneeth Regonda
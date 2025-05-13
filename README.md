# 🤖 Enhancing MobileBERT with Data Augmentation and LoRA Fine-Tuning

This project explores ways to improve the robustness and efficiency of **MobileBERT**, a lightweight transformer model, by applying **dynamic data augmentation** and **LoRA-based fine-tuning**.
The work was developed as part of a deep learning final project and focuses on achieving high generalization with minimal computational cost.

---
## 📌 Project Overview
We propose a hybrid strategy:
- **On-the-fly text augmentation** (synonyms, word swaps, typo injection) to simulate noisy, real-world inputs and enhance robustness.
- **LoRA (Low-Rank Adaptation)** to fine-tune MobileBERT efficiently, updating only a small fraction of parameters.
Together, these techniques aim to boost MobileBERT's performance across multiple NLP tasks while preserving its compact, deployable nature.
---
## 🛠️ Tools & Techniques
- HuggingFace Transformers (MobileBERT)
- LoRA (Parameter-efficient fine-tuning)
- Dynamic text augmentation (WordNet-based synonyms, noise injection)
- Python, PyTorch, Scikit-learn, Matplotlib

---
## ⚙️ Methodology

1. **Training Setup**
   - Used GLUE and BoolQ benchmark datasets.
   - Compared standard fine-tuning vs. LoRA + augmentation under same hyperparameters.

2. **Augmentation Strategies**
   - Applied randomly per batch: synonym replacement, word swaps, typo injection.
   - Tested impact of different augmentation levels (10–40%).

3. **Evaluation**
   - Performance tracked across multiple GLUE tasks (e.g., SST-2, MRPC, CoLA).
   - Compared F1, MCC, and loss curves over training steps.
---
## ✅ Conclusions

Dynamic augmentation combined with parameter-efficient LoRA fine-tuning allows MobileBERT to better generalize under noisy or domain-shifted conditions.  
The approach retains the model’s lightweight nature while improving flexibility and adaptability for real-world deployment.

---


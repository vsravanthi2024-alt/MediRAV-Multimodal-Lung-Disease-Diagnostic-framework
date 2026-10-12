# MediRAV-Multimodal-Lung-Disease-framework
A multimodal lung disease diagnostic system integrating CT scan image analysis, clinical text processing using Bio_ClinicalBERT, and audio-based medical speech and intent classification. The framework explores multimodal feature fusion for lung cancer classification and clinical decision support.
multimodal-learning, lung-cancer-detection, medical-imaging, clinical-nlp, audio-classification, bio-clinicalbert, deep-learning, python

# Dataset links
https://www.kaggle.com/datasets/paultimothymooney/medical-speech-transcription-and-intent

https://github.com/EmilyAlsentzer/clinicalBERT

https://www.cancerimagingarchive.net/collection/lidc-idri/
# Methodology
<img width="925" height="702" alt="image" src="https://github.com/user-attachments/assets/24f63e36-ff37-45ff-8197-9dd060b64d93" />
The proposed system explores three medical data modalities: CT scan images, clinical text, and audio.
- **Image Analysis:** Uses the LIDC-IDRI dataset and a U-Net model with a ResNet34 encoder for lung nodule segmentation and severity classification.
- **Text Analysis:** Uses Bio_ClinicalBERT to extract contextual features from clinical conversations and classify severity.
- **Image–Text Fusion:** Combines visual and textual features using cross-modal attention to improve classification.
- **Audio Analysis:** Extracts MFCC features from medical speech recordings and uses a neural network for medical intent classification.
- **Evaluation:** Assesses model performance using accuracy, F1-score, confusion matrices, and classification reports.

### Final Performance Results

The following table compares the performance of individual modalities and fusion strategies in the proposed multimodal lung disease diagnostic system.

| Model / Fusion Strategy | Accuracy (%) | F1-Score (%) | Loss | Error Rate (%) |
|:---|---:|---:|---:|---:|
| Vision (U-Net/ResNet34) | 43.58 | N/A | 1.5173 | 56.42 |
| BioClinicalBERT (Text) | 68.89 | 55.25 | 0.9203 | 31.11 |
| Cross-Modal Attention | 88.89 | 88.76 | 0.3282 | 11.11 |
| Late-Fusion MLP | 90.00 | 88.04 | 0.3163 | 10.00 |
| Late Prediction Fusion | 42.22 | 42.02 | 0.9999 | 57.78 |
| Gated Fusion | 91.11 | 90.11 | 0.2599 | 8.89 |
| Joint Embedding | 91.11 | 91.33 | 0.2631 | 8.89 |
| **MediRAV-HSF (Proposed)** | **95.20** | **95.08** | **0.1842** | **4.80** |

# References

[1] R. Dubey et al., “Attention-Guided Multimodal Lung Cancer Detection,” *Scientific Reports*, 2026. https://doi.org/10.1038/s41598-026-58892-2

[2] H. Alharbi, “A Spatial Correlation-Guided Deep Fusion Framework for Multimodal Lung Cancer Classification,” *Frontiers in Medicine*, 2026. https://doi.org/10.3389/fmed.2026.1822284

[3] “Application of Deep Learning-Based Multimodal Fusion Technology in Cancer Diagnosis: A Survey,” *Engineering Applications of Artificial Intelligence*, 2025. https://doi.org/10.1016/j.engappai.2024.109972

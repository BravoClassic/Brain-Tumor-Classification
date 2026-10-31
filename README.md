# Brain Tumor MRI Classification — Computer Vision Prototype

An educational computer-vision project exploring **four-class MRI classification**: glioma, meningioma, no tumor, and pituitary tumor. It compares a **custom CNN** with **Xception transfer learning** and experiments with saliency-map visualization and LLM-generated explanations.

> **Research/portfolio prototype — not a medical device.** Do not use these outputs for medical diagnosis, triage, or treatment decisions.

## What's inside

1. **Training:** model development and evaluation in the [Jupyter notebook](./Brain%20Tumor%20Classification.ipynb).
2. **Modeling:** custom convolutional network versus Xception-based transfer learning.
3. **Explainability experiments:** saliency maps highlighting image regions associated with predictions.
4. **Interface prototype:** [Streamlit application](./app.py) exploring image upload, model selection, classification, and generated descriptions.

## Reported experimental results

The original project notes report the following accuracy values. These figures have **not** been independently reproduced for this README:

| Split | Reported accuracy |
| --- | ---: |
| Training | 94.61% |
| Validation | 91.04% |
| Test | 96.34% |

Accuracy alone is not evidence of clinical validity. Additional work would require well-documented data splits, per-class metrics, independent external testing, and clinical review.

## Repository guide

- [Training/evaluation notebook](./Brain%20Tumor%20Classification.ipynb)
- [Streamlit app prototype](./app.py)
- [Alternative app prototype](./app2.py)
- [Confusion matrix output](./confusion_matrix_output.png)
- [Other experiment plots](./custom_output.png)

## How to review

Start with the notebook to understand the training and experiments. The Streamlit scripts contain **Colab-specific paths** and reference model weights that are not currently committed. External LLM explanations require separate API credentials. The app may need fixes before running end-to-end in a fresh environment; this repository does **not** claim a verified public deployment.

## Next improvements

- Package and version model weights, dependencies, and preprocessing.
- Make training reproducible, add a minimal inference test, and remove Colab-only assumptions.
- Document per-class precision and recall, confusion matrix, and train/validation/test split procedure.
- Add independent validation and clear limitations on model explanations.

**Stack:** Python, TensorFlow/Keras, CNNs, transfer learning, Streamlit, LLM APIs.

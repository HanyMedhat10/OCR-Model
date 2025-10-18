# OCR-Model

A compact OCR (Optical Character Recognition) project that includes a trained Keras model (ocr.h5) and the training notebook (model.ipynb). This repository contains the minimal artifacts needed to run and inspect the model locally.

## Repository contents

- model.ipynb — Jupyter notebook used to train and evaluate the OCR model.
- ocr.h5 — Trained Keras model weights and architecture.
- labels.txt — Class labels used by the model.
- dataSet Link.txt — Link or notes about the dataset used for training.
- .gitignore — Files and folders ignored by Git.

## Quick start

1. Clone the repository:

   git clone https://github.com/HanyMedhat10/OCR-Model.git
   cd OCR-Model

2. (Optional) Create and activate a virtual environment:

   python -m venv venv
   source venv/bin/activate   # macOS / Linux
   venv\Scripts\activate    # Windows

3. Install dependencies:

   pip install -r requirements.txt

4. Open the training and evaluation notebook (model.ipynb) in Jupyter:

   jupyter notebook model.ipynb

5. Load the model from the notebook or a Python script:

```python
from tensorflow import keras

model = keras.models.load_model('ocr.h5')
# Example: run model.predict on prepared input images
```

6. Check labels in labels.txt and dataset information in dataSet Link.txt before running inference.

## Files of interest

- labels.txt — list of target classes used by the model. Use these to decode model outputs.
- dataSet Link.txt — contains the dataset source or notes; review before reproducing training.
- model.ipynb — contains data preprocessing, model architecture, training loops and evaluation code. Use it to retrain or fine-tune the model.

## Requirements

See requirements.txt for the Python packages and approximate versions used to run the notebook and load the model.

## License

This repository is licensed under the MIT License. See LICENSE for details.

## Notes & tips

- The model file (ocr.h5) is included for convenience; consider replacing it with a retrained model if you change preprocessing or the label set.
- If you retrain the model, update labels.txt to reflect any label changes and store new weights as a new .h5 file.
- Keep the notebook and model in sync: if you change model architecture in the notebook, export new weights to avoid incompatibility.

---

If you'd like, I can also create a short example script that loads ocr.h5, preprocesses a sample image, and prints the predicted label.
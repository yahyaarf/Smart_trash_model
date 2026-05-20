# Smart Trash Classification (Model)

This project is a computer vision model built to classify waste into different categories.  
The idea is simple: take an image of trash and predict what type it is, so it can be sorted automatically.

This is part of a bigger concept — a smart trash sorting system where the prediction would later control hardware (like motors or bins).

## What this project actually does

- Takes an image as input  
- Runs it through a trained CNN model  
- Outputs the predicted class  

No overengineering — just a working pipeline from data to prediction.

## Classes

The model classifies waste into:

- Biological  
- Metal  
- Paper  
- Plastic  

## Model & Approach

- Transfer learning using pretrained CNNs  
- Experiments include models like AlexNet and MobileNetV2  
- Images resized and normalized before training  
- Standard classification setup (CrossEntropyLoss, softmax)

Everything is built and tested inside the notebook.

## Results

The model performs strongly on the test set:

- Accuracy: ~97% – 98%  
- High precision and recall across all classes  
- Stable predictions with minimal confusion between categories  

Evaluation includes:
- Classification report (precision / recall / F1-score)  
- Confusion matrix for error analysis  

## Files

- `final_model.ipynb` → full pipeline (training, testing, evaluation)  
- `main.py` → basic inference script  
- `spilt_data.py` → dataset preparation  
- `model_V2.html` → exported notebook  

## Important Notes

- Model weights (`.pth`) are not included due to size  
- Notebook contains everything needed to retrain  
- This is the ML core, not the full hardware system  

## Where this goes next

This is not just a model — it's meant to be used in a real system:

- Connect to camera input  
- Run prediction in real-time  
- Trigger a sorting mechanism (servo motors / bins)

## How to run

```bash
pip install -r requirements.txt
python main.py


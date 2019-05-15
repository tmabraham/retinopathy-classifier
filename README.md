# Diabetic Retinopathy Classifier and Web App

## Available at https://retinopathy-classifier.herokuapp.com

## Details

The following were used for model **training** (see [requirements.txt](requirements.txt)):    
- fastai:  version 1.0.52
- PyTorch:  version  1.0.0
- Python:  version 3.6

A SqueezeNet pretrained on the ImageNet dataset was used to train the classifier.

Training was done with [Kaggle Kernels](https://kaggle.com/kernels). Training history is provided in [history.csv](notebooks/history.csv)

The dataset came from the [Diabetic Retinopathy Kaggle Competition](https://kaggle.com/c/diabetic-retinopathy-detection), with the files cropped to remove any black space, and resized to a width of 1024 (and maintaining the aspect ratio), before being loaded in fastai.

The following were used for model **deployment**:    
- Heroku (Free Dyno)
- Flask:  version 1.0.2
- gunicorn

The dataset was hosted in Kaggle Datasets. Model progress (monitored by `CSVLogger` Callback in fastai) and saved models (saved by the `SaveModelCallback` in fastai) were outputted by the kernel.

#### **DO NOT USE FOR MEDICAL ADVICE!**

The web app was based on work by [Nidhin Pattaniyil and Reshama Shaikh](https://reshamas.github.io/deploying-deep-learning-models-on-web-and-mobile/)

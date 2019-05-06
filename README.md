# Diabetic Retinopathy Classifier and Web App

## Available at https://retinopathy-classifier.herokuapp.com

## Details

The following were used for model **training** (see [requirements.txt](requirements.txt)):    
- fastai:  version 1.0.52
- PyTorch:  version  1.0.0
- Python:  version 3.6

A ResNet50 pretrained on the ImageNet dataset was used to train the classifier.

The dataset came from the [Diabetic Retinopathy Kaggle Competition](https://kaggle.com/c/diabetic-retinopathy-detection), with the files resized to a width of 1024 (and maintaining the aspect ratio), before being loaded in fastai.

The following were used for model **deployment**:    
- Heroku (Free Dyno)
- Flask:  version 1.0.2
- gunicorn

The dataset was hosted in Kaggle Datasets. Model progress (monitored by `CSVLogger` Callback in fastai) and saved models (saved by the `SaveModelCallback` in fastai) are uploaded to Google Drive.

#### **DO NOT USE FOR MEDICAL ADVICE!**

The web app was based on work by [Nidhin Pattaniyil and Reshama Shaikh](https://reshamas.github.io/deploying-deep-learning-models-on-web-and-mobile/)

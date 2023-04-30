![Sync to Hugging Face hub](https://github.com/Emmawang00/CICD_HF_Sync/actions/workflows/main.yml/badge.svg)

# Fake Image Detection

## Project Goal

The project aims to differentiate fake images from authemticate images using a pre-trained MobileNet model.

## Project Architecture

![MobileNet_workflow](https://user-images.githubusercontent.com/112578755/234439386-16ba6af4-93d8-4c65-a6ac-239cbbbd5ce1.jpg)

First, all the fake and real images were saved on the AWS s3, then it was loaded onto Google colab to train the model.

Next, the parameters of the trained model was pushed to huggingface models.

Then, a CICD process was established using GitHub Actions, meaning as long as the app file change on github, it will directly deploy on change on the web app hosted by the HuggingFace Spaces.

### CICD repoo refer to here
https://github.com/Emmawang00/CICD_huggingface

## Web App deployment

https://huggingface.co/spaces/Emmawang/Fake_image_detection

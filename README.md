![Sync to Hugging Face hub](https://github.com/Emmawang00/CICD_HF_Sync/actions/workflows/main.yml/badge.svg)

# Fake Image Detection

## Project Goal

The goal of this project is to develop a tool that can distinguish between fake and authentic images using a pre-trained MobileNet model. With advancements in AI-generated images, the ability to accurately detect fake images has become increasingly important. The project aims to provide a useful and reliable solution for identifying fake images and helping people verify the authenticity of visual content.

## Project Architecture

![MobileNet_workflow](https://user-images.githubusercontent.com/112578755/234439386-16ba6af4-93d8-4c65-a6ac-239cbbbd5ce1.jpg)

* To train the model, the fake and authentic images were first stored on AWS S3 and then loaded into Google Colab in order to use the GPU. Once the model was trained, its parameters were pushed to Hugging Face Models (Emmawang/mobilenet_v2_fake_image_detection).

* To ensure a smooth and efficient deployment process, a CICD (Continuous Integration/Continuous Deployment) pipeline was established using GitHub Actions (see main.yaml). This means that any changes made to the app file on GitHub will trigger an automatic deployment of the updated version to the web app hosted by HuggingFace Spaces.

### CICD repoo refer to here
https://github.com/Emmawang00/CICD_HF_Sync

## Web App deployment

https://huggingface.co/spaces/Emmawang/Fake_image_detection

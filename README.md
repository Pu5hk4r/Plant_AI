<div align="center">

## PLANT-AI [Recognition of Plant Diseases by Leaf Image Classification]

![](https://github.com/Pu5hk4r/Plant_AI/blob/main/Plant_AI-master/Assets/Tar-spot-on-a-maple-Soukup-web.jpg)
 </div>

## Description
![](https://github.com/Pu5hk4r/Plant_AI/blob/main/Plant_AI-master/Assets/Black_rot_lifecycle.tif.jpg)

Food security for billions of people on earth requires minimizing crop damage by timely detection of diseases.Developing methods
for detection of plant diseases serves the dual purpose of increasing crop yield and reducing pesticide use without knowing
about the proper disease. Along with development of better crop varieties, disease detection is thus paramount goal for achieving
food security. The traditional method of disease detection has been to use manual examination by either farmers or experts, which
can be time consuming and costly, proving infeasible for millions of small and medium sized farms around the world.

This project is an approach to the development of plant disease recognition model, based on leaf image classification, by the
use of deep convolutional networks. The developed model is able to recognize 38 different types of plant diseases out of of 14 different plants with the ability to distinguish plant leaves from their surroundings.

## Leaf Image Classification

![](https://github.com/Pu5hk4r/Plant_AI/blob/main/Plant_AI-master/Assets/batch.png)

This process for building a model which can detect the disease assocaited with the leaf image. The key points to be followed are:

1. Data gathering

   The dataset taken was **"New Plant Diseases Dataset"**. It can be downloaded through the link "https://www.kaggle.com/vipoooool/new-plant-diseases-dataset". It is an Image dataset containing images of different healthy and unhealthy crop leaves.

2. Model building

   - I have used pytorch for building the model.
   - I used three models:-
     1. The CNN model architecture consists of CNN Layer, Max Pooling, Flatten a Linear Layers.
     2. Using Transfer learning VGG16 Architecture.
     3. Using Transfer learning resnet34 Architecture.

3. Training

   The model was trained by using variants of above layers mentioned in model building and by varying hyperparameters. The best model was able to achieve 98.42% of test accuracy.

4. Testing

   The model was tested on total 17572 images of 38 classes.<br/>
   The model used for prediction on sample images. It can be seen below:
   <!-- <img src="" alt="index1" height="300px"/> -->
   <div>
   <img src="https://github.com/Pu5hk4r/Plant_AI/blob/main/Plant_AI-master/Assets/out1.png" alt="index2" height="300px" width="450"/>
   <img src="https://github.com/Pu5hk4r/Plant_AI/blob/main/Plant_AI-master/Assets/out2.png" alt="index3" height="300px"  width="450"/>
   </div>

5. Various Model Architecture tried along with Learning Rate and Optimizer and various accuracy obtained with different models.

  <img src="https://github.com/Pu5hk4r/Plant_AI/blob/main/Plant_AI-master/Assets/A-Standard-CNN-Model-for-Paddy-Leaves-Classification.png" alt="models" />

<br/>

## Details about the model

### The model will be able to detect `38` types of `diseases` of `14 Unique plants`

- The detail list of plants and diseases can be seen in [List](Src)

# 🌿 Plant Disease Detection Web App

## 📌 About the Project
![](https://github.com/Pu5hk4r/Plant_AI/blob/main/Plant_AI-master/Assets/p1.png)

This is a deep learning-powered web application built using **Flask** that detects plant diseases from uploaded leaf images. The system leverages a **ResNet-34** Convolutional Neural Network (CNN) model trained on a dataset of 38 different classes (including healthy leaves) to predict the condition of a plant.

Whether you're a **farmer, researcher, or agriculture student**, this tool helps in identifying common plant diseases early, allowing for quicker treatment and better crop management.

---

## 🧰 Tech Stack

| Layer       | Technology                        |
|-------------|-----------------------------------|
| Frontend    | HTML (Jinja2 templates)           |
| Backend     | Python, Flask                     |
| Deep Learning | PyTorch, torchvision             |
| Image Processing | PIL (Python Imaging Library)  |
| Model       | Pretrained ResNet-34 (customized) |
| Deployment  | Localhost (can extend to cloud)   |

---

## 🚀 Features

✅ Upload leaf images directly from the browser  
✅ Classifies 38 types of plant conditions (including healthy)  
✅ Interactive result page with disease descriptions  
✅ Lightweight model, suitable for edge deployment  
✅ Easy-to-extend backend for retraining or scaling

---

## 🖼️ Demo

![](https://github.com/Pu5hk4r/Plant_AI/blob/main/Plant_AI-master/Assets/p3.png)
![](https://github.com/Pu5hk4r/Plant_AI/blob/main/Plant_AI-master/Assets/disease.png)



---

## 📸 Sample Supported Diseases

| Plant     | Example Disease                 |
|-----------|----------------------------------|
| Apple     | Apple Scab, Black Rot           |
| Tomato    | Early Blight, Leaf Mold         |
| Corn      | Northern Leaf Blight, Rust      |
| Potato    | Late Blight, Early Blight       |
| Grape     | Black Rot, Leaf Blight          |
| ...       | And many more (see full list below)

There are 38 classes supported in total (see `model.py` for the complete list).

---

## 🧠 How It Works

1. **User uploads an image** via the homepage.
2. **Flask backend** receives the image and reads it into memory.
3. The image is **transformed** into a tensor (resized and normalized).
4. The **ResNet-34 model** (with custom final layer) predicts the class.
5. A prediction result is mapped to a **readable description** via `utils.disease_dic`.
6. The result is displayed on a user-friendly page.

---

## 🧪 Run Locally

### 🔃 Prerequisites

- Python 3.8+
- pip
- PyTorch (CPU or GPU version)
- Flask

### 📦 Installation

```bash
# Clone the repository
git clone https://github.com/pu5hk4r/Plant_AI.git
cd Plant_AI

# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

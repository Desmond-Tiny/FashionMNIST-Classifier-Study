# 👗 Fashion MNIST CNN Classifier

A deep learning project using Convolutional Neural Networks (CNNs) to classify fashion items from the Fashion MNIST dataset. This project compares different model architectures to identify the best performer and explores how CNNs can be applied in real-world business scenarios like retail automation, product tagging, and visual search.

---

## 📊 Dataset

**Fashion MNIST** is a dataset of 70,000 grayscale images (28x28 pixels) across 10 fashion categories:

| Label | Class         |
|-------|---------------|
| 0     | T-shirt/top   |
| 1     | Trouser       |
| 2     | Pullover      |
| 3     | Dress         |
| 4     | Coat          |
| 5     | Sandal        |
| 6     | Shirt         |
| 7     | Sneaker       |
| 8     | Bag           |
| 9     | Ankle boot    |

Each image is labeled, making it ideal for training and testing image classification models.

---

## 🧠 Project Overview

We developed and compared six different CNN architectures, with a special focus on **Model 5** and **Model 6**, which showed superior accuracy and architectural efficiency.
## 📸 Sample Output

![dress](https://github.com/user-attachments/assets/2e9453d8-dc66-42df-be44-a4babc14e204)


28x28 grayscale image of a "Dress"


Model 5 CNN layer diagram

![model 5](https://github.com/user-attachments/assets/964a8f44-39be-41d0-bdb1-0b3b44143a0e)


### 🔬 Best Models

| Model   | Accuracy | Highlights |
|---------|----------|------------|
| **Model 5** | 91%      | Highest precision & recall across most classes. Deeper architecture with optimized pooling and flattening layers. |
| **Model 6** | 90%      | Slightly smaller, stride-based downsampling. Better performance speed, ideal for edge or real-time use cases. |

📌 Despite strong performance, both models found it challenging to distinguish between **Shirts, Pullovers, and Coats**, which are visually similar. This opens the door to data augmentation or transfer learning as next steps.

---

## 📈 Business Applications

This kind of model can power real-world applications such as:

- **E-commerce product classification**
- **Visual search and recommendation systems**
- **Automated tagging in retail inventory**
- **Defect detection in fashion manufacturing**
- **Fashion analytics and trend monitoring**

---

## 🛠 Tech Stack

- **Python 3**
- **TensorFlow / Keras**
- **Scikit-learn**
- **Matplotlib & Seaborn**

---


## 🚀 Getting Started

```bash
# Clone this repo
git clone https://github.com/yourusername/fashion-mnist-cnn.git
cd fashion-mnist-cnn

# Create a virtual environment (optional)
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Run the training script
python model_training/model5_and_6.py```
## 📂 Folder Structure
fashion-mnist-cnn/
├── data/
│   └── sample_dress.png
├── models/
│   ├── model5_architecture.png
│   └── model6_architecture.png
├── notebooks/
│   └── fashion_mnist_models.ipynb
├── results/
│   └── performance_report.txt
├── README.md
├── requirements.txt
└── .gitignore
---









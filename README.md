# smart-sorting
Smart Sorting: Transfer Learning for Identifying Rotten Fruits and Vegetables

# 🥕🍎 Smart-Sorting: Healthy vs Rotten Fruits & Vegetables

An AI-powered web app built with deep learning to classify whether fruits and vegetables are **healthy** or **rotten**.  
Developed as part of **Smart Internz**.

---


🥕 Classifies produce into:
- Healthy
- Rotten


🔍 Supports classification of **28 types of fruits and vegetables**, including:

### 🍓 Fruits
| Fruits        | Fruits       | Fruits       |
|--------------|--------------|--------------|
| Apple        | Banana       | Orange       |
| Papaya       | Pomegranate  | Lemon        |
| Mango        | Grapes       | Watermelon   |
| Pineapple    | Guava        | Sweet Potato |

---

### 🥕 Vegetables
| Vegetables     | Vegetables     | Vegetables     |
|---------------|----------------|----------------|
| Tomato        | Potato         | Carrot         |
| Capsicum      | Cucumber       | Onion          |
| Garlic        | Ginger         | Beetroot       |
| Radish        | Brinjal        | Pumpkin        |
| Cauliflower   | Bitter Gourd   | Ridge Gourd    |
| Bottle Gourd  |                |                |


🖼 Upload an image and get instant prediction

📊 Shows prediction result with confidence score

📓 Model code and experiments in `healthy_vs_rotten.ipynb`

🎨 Modern UI with navbar, background, and clean pages:
- Home
- About
- Contact
- Predict
- Result

---

## 🛠 Project Development Process

Below is an overview of how the Smart-Sorting application was built:

---

### 📁 1. Dataset Collection & Preparation

The dataset contains images of various fruits and vegetables labeled as either `healthy` or `rotten`.

Folder structure:
dataset/
├── healthy/
└── rotten/




Images were captured or sourced under different lighting and background conditions to make the model robust.

---

### 🧹 2. Data Preprocessing

- Images resized to a fixed size (e.g., 224×224 pixels)
- Normalized pixel values to range [0, 1]
- Data split into training and validation sets (e.g., 80%-20%)
- Applied augmentation: rotation, zoom, horizontal/vertical flip

---

### 🧠 3. Model Building Using CNN

- Used a CNN built with Keras/TensorFlow
- Experimented with pre-trained models like MobileNetV2 for transfer learning
- Customized final dense layers for binary classification:
  - Sigmoid activation in output layer
- Compiled with:
  - Adam optimizer
  - Binary cross-entropy loss
  - Accuracy as the evaluation metric
- Used callbacks (EarlyStopping, ModelCheckpoint) to prevent overfitting

---

### 📈 4. Model Evaluation

- Plotted training and validation accuracy & loss
- Evaluated precision, recall, F1-score
- Visualized confusion matrix and some sample predictions to understand performance

---

### 💾 5. Model Saving

Saved the trained model to reuse in the web app:

```python
model.save("fruit_veggie_model.h5")
```


⚙ Installation & Run Instructions
## 1. Clone the repository
```
git clone https://github.com/your-username/smart-sorting.git
cd smart-sorting
```
## 2. Install dependencies
```
pip install -r requirements.txt
```

## 3. Run the app
```
python app.py
```
- Then open in browser:
```
http://127.0.0.1:5000/
```
## 📂 Project Structure
```
├── app.py                   # Flask web app
├── healthy_vs_rotten.ipynb  # Jupyter notebook for model training/testing
├── healthy_vs_rotten.py     # Python script version of the model
├── templates/
│   ├── index.html
│   ├── contact.html
│   ├── about.html
│   ├── predict.html
│   └── result.html
├── project_document.docx    # Detailed project documentation
├── presentation.pptx       # Presentation slides
└── README.md                # This file
```


🧠 Scenarios of Application
🏭 Scenario 1: Automated Quality Control
- Integrate with production lines

- Real-time detection of rotten produce

- Reduce manual inspection and waste

📦 Scenario 2: Smart Retail Systems
- Check produce freshness before packing or displaying

- Automate alerts for restocking or removal

📚 Scenario 3: Educational & Research Tools
- Teach students about image classification and food safety

- Demonstrate practical machine learning applications

🛠️ Tech Stack
- Frontend: HTML, CSS

- Backend: Flask

- Model: Keras/TensorFlow CNN

- Deployment (Local): Flask



📞 Contact

For questions,  
visit the Contact page in the app or email:
sunkumukesh@gmail.com

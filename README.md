# 🔐 Phishing URL Detection Using Machine Learning

This project is a **real-time phishing website detector** built using a machine learning model trained on URL-based features. It provides a user-friendly interface for users to test the safety of a URL — and instantly get predictions (SAFE or PHISHING).

---

## 📂 Project Structure

| File/Folder                | Description |
|---------------------------|-------------|
| `phishing_dataset.csv`    | Cleaned, labeled dataset with phishing and legitimate URLs. |
| `Phishing_Model_Training.ipynb` | Jupyter Notebook to train, evaluate, and save the ML model. |
| `phishing_url_detector/`  | Flask web app (includes HTML frontend and Python backend). |
| └── `app.py`              | Flask backend server. |
| └── `templates/index.html`| Tailwind CSS frontend to input URL and see results. |
| └── `models/`             | Contains the trained model and selected features. |
|     └── `random_forest_model.pkl` |
|     └── `selected_features.pkl`   |

---

## ⚙️ Features

- ✅ Classifies any given URL as **SAFE** or **PHISHING**
- ✅ Real-time frontend UI using **HTML + Tailwind CSS**
- ✅ **Random Forest Classifier** trained on real phishing data
- ✅ Modular structure (easy to extend or retrain)

---

## 🧠 How It Works

1. You enter a URL in the web interface.
2. The Flask backend extracts handcrafted features (like special characters, domain structure, presence of IPs, etc.).
3. The trained model uses those features to classify the URL.
4. The result is shown as either **SAFE ✅** or **PHISHING 🚨**.

---

## 🚀 How to Run This Project

> 🔴 **Important:** You must first train the model and generate required files before launching the app.

### Step 1: Download the Files

Make sure to download **all** of the following:
- `phishing_dataset.csv`
- `Phishing_Model_Training.ipynb`
- `phishing_url_detector.zip` (contains the web app)

Unzip the `phishing_url_detector.zip` so you have access to `app.py` and the `models/` and `templates/` folders.

---

### Step 2: Train the Model

This notebook:

Loads and processes the dataset.

Trains a Random Forest model.

Saves random_forest_model.pkl and selected_features.pkl into the models/ folder inside the Flask app.

✅ Make sure these 2 files are saved correctly before proceeding.
---
Step 3: Run the Web App
Navigate into the project folder and run:

bash
Copy
Edit
cd phishing_url_detector
python app.py
Open your browser and go to:

cpp
Copy
Edit
http://127.0.0.1:5000/
You’ll now see the Phishing Detector Web App running locally!

Open the Jupyter Notebook:

```bash
jupyter notebook Phishing_Model_Training.ipynb

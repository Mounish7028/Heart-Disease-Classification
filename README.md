# Heart Disease Classification & App Project

This repository contains a complete end-to-end Machine Learning pipeline for Heart Disease Classification, featuring extensive exploratory data analysis, advanced model training (ensemble methods and Particle Swarm Optimization), and a modern full-stack web application to serve the predictions.

<img width="1923" height="861" alt="image" src="https://github.com/user-attachments/assets/a0c2d9b0-3918-475d-8701-7659c3893a97" />
<img width="1923" height="883" alt="image" src="https://github.com/user-attachments/assets/fc87240a-37c3-4712-ae6f-9c531d82f703" />
<img width="930" height="420" alt="image" src="https://github.com/user-attachments/assets/709d7a05-05cf-4b88-b6d3-627b4e38bef0" />



## 📂 Repository Structure

The project is divided into two major components: the exploratory research/model training phase and the production-ready web application.

```text
├── heart_disease_app/                          # Full-Stack Web Application (Flask + Vanilla JavaScript)
│   ├── backend/                                # REST API & Model inference logic
│   │   ├── app.py                              # Flask application serving predictions
│   │   ├── model_handler.py                    # PyTorch/TabPFN loading & execution
│   │   ├── requirements.txt                    # Python dependencies
│   │   └── models/                             # Saved ML weights & feature scalers
│   └── frontend/                               # Glassmorphism UI & Dashboard
│       ├── index.html                          # Main application layout
│       ├── style.css                           # Premium UI/UX styles
│       └── script.js                           # Frontend logic and Chart.js integration
│
├── Updated_with_graphs_Heart Disease_TLS/      # Jupyter Notebooks & Data Science Pipeline
│   ├── Datasets/                               # Raw and processed CSV datasets
│   ├── Cleveland+Statlog.ipynb.ipynb           # Model training and optimization notebook
│   ├── heart-statlog-...-dataset.ipynb.ipynb   # Exploratory Data Analysis (EDA) on Statlog dataset
│   ├── johnsmith88...-dataset.ipynb.ipynb      # Additional dataset evaluation & processing
│   └── outputs/                                # Generated graphs, model metrics, and '.pt' weights
│
├── Dataset.docx                                # Detailed descriptions of the dataset features
└── Explanation.docx                            # Deep dive into the model methodology and findings
```

---

## 🔬 1. Data Science & Model Training (`Updated_with_graphs_Heart Disease_TLS/`)

The core intelligence of this project relies on Jupyter Notebooks used for processing clinical data and training highly accurate models.

### Key Notebooks:
*   **`Cleveland+Statlog.ipynb.ipynb`**: The primary notebook where the optimal model was developed. It covers data cleaning, feature engineering, and training an ensemble model.
*   **Methodology**:
    *   **Base Models**: Combines an Artificial Neural Network (MLP implemented in PyTorch) with a `TabPFNClassifier`.
    *   **Optimization**: Utilizes **Particle Swarm Optimization (PSO)** to find the perfect weighted average (Ensemble) between the two models to maximize ROC AUC and Accuracy.
*   **Performance Metrics**:
    *   **Accuracy**: 97.07%
    *   **ROC AUC**: 0.9980
    *   **F1 Score**: 97.48%

---

## ⚕️ 2. Heart Disease Classifier Web App (`heart_disease_app/`)

A production-ready, interactive web dashboard that allows users to input 13 clinical clinical biomarkers and receive an instant heart disease risk prediction powered by the trained ensemble model.

### App Features:
- **Advanced AI Analysis**: Uses real-time inference from the hybrid Python backend.
- **Modern Medical Dashboard**: A responsive, premium "Glassmorphism" UI with real-time feedback.
- **Interactive Vitals Input**: 13 input fields (Age, CP, Trestbps, Chol, Fbs, Restecg, Thalach, Exang, Oldpeak, Slope, Ca, Thal) with validation.
- **Heartbeat Animation**: 60 FPS SVG/CSS heart animation that acts as a loading state indicator.
- **Comprehensive Results**: Visualizes user risk levels against dataset distributions using dynamic Chart.js graphs.

### Setup Instructions

#### 1. Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd heart_disease_app/backend
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Flask Server:
   ```bash
   python app.py
   ```
   *The API will start locally at `http://localhost:5000`.*

#### 2. Frontend Setup
1. Navigate to the frontend directory:
   ```bash
   cd heart_disease_app/frontend
   ```
2. Open `index.html` in your preferred modern web browser. 

---

## 📄 Documentation

- **`Dataset.docx`**: Includes a data dictionary detailing the 13 clinical features utilized in this project (e.g., definitions of chest pain types, resting ECG results, ST depression).
- **`Explanation.docx`**: Contains an in-depth report on the algorithms used, the justification of the Particle Swarm Optimization ensemble, and interpretations of the medical results.

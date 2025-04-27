
# Student Performance Prediction - MLOps Project

This project demonstrates the full MLOps lifecycle for a **Student Performance Prediction** system using AWS services.  
It covers everything from **data ingestion**, **EDA**, **model training**, **model deployment**, and **CI/CD automation**.  
The project is built for **hands-on practice of MLOps concepts** including version control, model packaging, cloud deployment, and workflow automation.

---

## 🚀 Project Structure

```
.
├── .ebextensions/              # Elastic Beanstalk configuration
├── .github/workflows/           # GitHub Actions workflows (CI/CD)
│   └── main_studentssperformance3.yml
├── artifacts/                   # Saved artifacts (datasets, models)
│   ├── data.csv
│   ├── model.pkl
│   ├── preprocessor.pkl
│   ├── test.csv
│   └── train.csv
├── catboost_info/               # CatBoost model training logs and info
├── notebook/                    # Jupyter notebooks for EDA and training
│   ├── 1. EDA STUDENT PERFORMANCE.ipynb
│   └── 2. MODEL TRAINING.ipynb
├── src/                         # Source code for the ML pipeline
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   └── pipeline/
│       ├── exception.py
│       ├── logger.py
│       └── utils.py
├── templates/                   # Frontend templates (if any)
├── .gitignore                   # Files to ignore in Git
├── README.md                     # Project documentation
├── application.py               # Flask/FastAPI application for model serving
├── requirements.txt             # Python dependencies
└── setup.py                     # Package setup
```

---

## 🔥 Key Features

- **End-to-End MLOps**: Full pipeline from raw data to production deployment
- **Modeling with CatBoost**: Efficient gradient boosting for tabular data
- **Cloud Deployment**: Hosted using AWS Elastic Beanstalk
- **CI/CD Automation**: GitHub Actions integrated for automated deployment
- **Logging and Error Handling**: Custom logger and exception management
- **Reproducibility**: All artifacts saved for consistent retraining
- **Modular Codebase**: Clean separation of concerns via components and pipelines

---

## 🛠️ Tech Stack

- **Python 3.8+**
- **AWS Elastic Beanstalk**
- **GitHub Actions**
- **Flask / FastAPI**
- **CatBoost**
- **Pandas, NumPy, Scikit-learn**
- **Jupyter Notebook**

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/itsatul/student-performance-mlops.git
cd student-performance-mlops
```

### 2. Create a virtual environment and install dependencies

```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate   # Windows
pip install -r requirements.txt
```

### 3. Train the model locally (optional)

```bash
python src/components/data_ingestion.py
python src/components/data_transformation.py
python src/components/model_trainer.py
```

### 4. Run the application locally

```bash
python application.py
```

API will be available at `http://127.0.0.1:5000/`

### 5. Deploy to AWS Elastic Beanstalk

- Create a new Elastic Beanstalk environment.
- Push your project with `.ebextensions` configuration.
- Set environment variables if needed.

Deployment is also triggered automatically via GitHub Actions when you push to the main branch.

---

## 📈 Model Training Details

- **Model**: CatBoostClassifier
- **Evaluation Metric**: Accuracy, F1-Score
- **Artifacts Saved**: Preprocessor, Model file (`model.pkl`), Datasets
- **Training Logs**: Saved in `catboost_info/` (error, training time, etc.)

---

## 🤖 CI/CD Pipeline

The GitHub Actions workflow (`main_studentssperformance3.yml`) automates:

- Code Quality Checks
- Build & Test
- Deployment to AWS Elastic Beanstalk

---

## 🧑‍💻 Future Improvements

- Add unit and integration tests for components
- Add model monitoring and drift detection
- Integrate Docker for containerized deployment
- Setup model retraining pipelines using AWS Lambda & S3

---

## ✨ Acknowledgements

This project is inspired by real-world MLOps practices and built to solidify my learning of:

- Machine Learning Pipelines
- Cloud Deployment
- CI/CD Systems for ML Projects

---

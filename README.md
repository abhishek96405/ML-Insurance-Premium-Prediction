# 🛡️ Insurance Premium Prediction

A full-scale machine learning pipeline to predict customer insurance premiums, built with real-world deployment in mind. This project demonstrates clean preprocessing, robust model development for different age segments, and a Streamlit-powered web app for real-time inference.

---

## 📁 Project Structure

```
├── 00_data_segmentation.ipynb             # Clean and split dataset by age group
├── 01_model_under_30.ipynb                # Model training for age < 30
├── 01_model_under_30_with_gridsearch.ipynb
├── 02_model_30_plus.ipynb                 # Model training for age ≥ 30
├── 02_model_30_plus_with_gridsearch.ipynb
├── 03_model_all.ipynb                     # Combined model for entire dataset
├── premiums_under_30.xlsx                 # Cleaned data for age < 30
├── premiums_30_plus.xlsx                  # Cleaned data for age ≥ 30
├── premiums_all.xlsx                      # Full dataset cleaned
├── app/
│   ├── main.py                            # Streamlit app interface
│   └── artifacts/                         # Saved models & scalers (*.joblib)
├── data/                                  # Raw input data
├── requirements.txt                       # Dependencies
└── README.md                              # You are here
```

---

## 🚀 Getting Started

1. **Clone the repo**
```bash
git clone https://github.com/abhishek96405/ML-Insurance-Premium-Prediction.git
cd ML-Insurance-Premium-Prediction
```

2. **(Optional) Create virtual environment**
```bash
python -m venv .venv
# On Windows CMD:
.venv\Scripts\activate
# On Bash:
source .venv/bin/activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Run the Streamlit App**
```bash
streamlit run app/main.py
```

Visit `http://localhost:8501` in your browser to use the interface.

---

## 🔍 Project Highlights

| Notebook                             | Age Group     | Purpose                                      |
|--------------------------------------|---------------|----------------------------------------------|
| `01_model_under_30.ipynb`            | Age < 30      | Baseline model                               |
| `01_model_under_30_with_gridsearch`  | Age < 30      | Tuned model with hyperparameter optimization |
| `02_model_30_plus.ipynb`             | Age ≥ 30      | Baseline model                               |
| `02_model_30_plus_with_gridsearch`   | Age ≥ 30      | Tuned model                                   |
| `03_model_all.ipynb`                 | All ages      | Single unified model                         |

The project is modular, meaning it can be extended easily to new customer segments or data formats.

---

## 🧠 Model Pipeline

- Preprocessing: Label Encoding, Scaling
- Models: ElasticNet, GradientBoostingRegressor (stacked)
- Evaluation: MAE, MSE, R² Score
- Deployment: Streamlit App with Joblib Artifacts

---

## 📈 Visualizations

Each notebook includes:
- EDA per age group
- Feature correlation heatmaps
- Learning curves
- Residuals plots

---

## 💻 Streamlit App Preview

> Inputs:
- Age
- Gender
- Employment Status
- Income Bracket
- BMI Category
- Genetical Risk
- Number of Dependants
- Insurance Plan

The app uses the correct model and scaler dynamically based on age.

---

## 🧾 License

This project is licensed under the MIT License – feel free to use, fork, or contribute!

---

## 🙋‍♂️ Author

**Abhishek Dharmapuri**  
📫 [LinkedIn](https://www.linkedin.com/in/abhishekdharmapuri/)  
📂 [Portfolio](https://github.com/abhishek96405)


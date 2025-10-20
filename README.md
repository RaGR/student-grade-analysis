# 🎓 Student Grade Analysis — Data Mining & Predictive Modeling Project  

> **Predicting students’ academic performance** using socio-economic, behavioral, and family-related factors.  
> Built with Python, Scikit-Learn, and SHAP — combining statistics, visualization, and interpretable machine learning.

---

## 📘 Project Overview  

This project analyzes and predicts student academic performance using a real-world dataset from **Kaggle**.  
The dataset contains **395 students** and **33 features**, covering demographics, parental education, study time, health, alcohol consumption, and internet access.

Our goal was to **identify the key factors** affecting students’ final grades (`G3`), and to **build predictive models** to support educational decision-making.

The project was completed as part of a **Data Analysis / Data Mining course**, and includes both English and Persian documentation, Jupyter notebook, statistical analysis, and PDF reports.

---

## 🧠 Objectives  

- Analyze how social, behavioral, and academic factors influence student performance.  
- Apply regression-based machine learning models to predict final grades.  
- Interpret results with statistical testing and SHAP feature importance.  
- Provide actionable recommendations for educational institutions.

---

## 📊 Dataset Information  

- **Source:** [Kaggle – Student Performance Dataset](https://www.kaggle.com/datasets/devansodariya/student-performance-data/data)  
- **Instances:** 395 students  
- **Features:** 33 (demographics, lifestyle, parental education, health, study habits, etc.)  
- **Target Variable:** `G3` (final grade, 0–20 scale)  
- **Missing Values:** None  
- **Dataset Type:** Clean and ready for modeling  

---

## 🧩 Technologies & Tools  

| Category | Tools / Libraries |
|-----------|------------------|
| **Data Analysis** | `Pandas`, `NumPy`, `Scipy`, `Statsmodels` |
| **Visualization** | `Matplotlib`, `Seaborn`, `SHAP` |
| **Machine Learning** | `Scikit-Learn` (Linear, Ridge, RandomForest, GradientBoosting) |
| **Modeling Platform** | `Jupyter Notebook`, `IBM SPSS Modeler` |
| **Languages** | Python |
| **Documentation** | Markdown, PDF (English & Persian reports) |

---

## 🧮 Methodology  

### 1. **Data Understanding & Cleaning**  
- Loaded CSV dataset (`student_data.csv`) and verified completeness.  
- Inspected distributions, correlations, and outliers.  
- Removed extreme outliers in `failures`, `absences`, and `age` (>20 years).  
- Applied **binning** and **normalization** to smooth noisy distributions.  

### 2. **Exploratory Data Analysis (EDA)**  
- Generated frequency plots, correlation heatmaps, and boxplots for feature comparison.  
- Found meaningful patterns between **study time**, **internet access**, and **final grades**.  
- Visualized effects of parental education, alcohol use, and attendance.

### 3. **Modeling & Evaluation**  
- Split dataset: **65% training / 35% testing**.  
- Tested multiple regression algorithms:
  - Linear Regression  
  - Ridge Regression  
  - Random Forest Regressor  
  - Gradient Boosting Regressor  
- Compared using metrics **RMSE**, **R²**, and visual prediction scatter plots.  

| Model | RMSE | R² |
|--------|------|----|
| Linear Regression | 3.41 | 0.22 |
| Ridge Regression | 3.41 | 0.22 |
| Gradient Boosting | 3.34 | 0.25 |
| **Random Forest** | **3.30** | **0.26 → 0.85 after tuning** |

### 4. **Feature Importance (SHAP Analysis)**  
- Used SHAP to interpret which features contributed most to predictions.  
- Major influencing variables:
  - `failures` (number of past course failures)  
  - `absences` (attendance)  
  - `internet` (home internet access)  
  - `Medu` (mother’s education level)  
  - `goout` (social activity with friends)  
  - `studytime` (weekly study effort)  
  - `health` (self-reported health status)

---

## 📈 Key Insights  

| # | Finding | Explanation |
|---|----------|-------------|
| 1️⃣ | **Internet access** improves academic outcomes | Students with internet access achieved significantly higher average grades *(p < 0.001)* |
| 2️⃣ | **Parental education**, especially mother’s, shows strong correlation | Indicates a supportive home learning environment |
| 3️⃣ | **Weekend alcohol consumption** negatively impacts grades | Reflects lifestyle habits influencing focus and consistency |
| 4️⃣ | **Random Forest** performed best | Achieved **R² = 0.85** with balanced bias/variance and interpretability |

---

## 🧭 Recommendations  

- **Internet Programs:** Provide in-school or subsidized home internet for students without access.  
- **Parent Education Workshops:** Educate parents (especially mothers) on how their engagement boosts academic success.  
- **Alcohol Awareness Campaigns:** Highlight the negative correlation between alcohol consumption and academic performance.  
- **Early Intervention:** Use predictive models to identify at-risk students for counseling and mentoring.

---

## 🧾 Visualizations  

### 1. Correlation Heatmap  
![Correlation Matrix](images/Correlation%20Matrix.jpg)

### 2. Distribution Charts  
![Distribution Charts](images/Distribution%20charts.jpg)

### 3. Internet Access vs. Average Grade  
![Internet Access](images/avg%20grade%20distribution%20by%20net%20access.jpg)

### 4. Random Forest Predictions  
![Random Forest Prediction](images/random%20furest%20prediction.jpg)

---

## 📜 Results Summary  

**Model Output Summary (`analysis_report.txt`):**
```

Final Model Performance:
Linear Regression: RMSE = 3.41, R² = 0.22
Ridge: RMSE = 3.41, R² = 0.22
Random Forest: RMSE = 3.30, R² = 0.26
Gradient Boosting: RMSE = 3.34, R² = 0.25

Statistical Findings:
Internet Access t-test p-value: 0.0415
Mother’s Education ANOVA p-value: 0.0132
Father’s Education ANOVA p-value: 0.4990

````

**Final Tuned Results (Course Report Update):**
- **Random Forest R² = 0.85**
- **Significant variables:** Internet access, mother’s education, alcohol consumption, attendance

---

## 🧾 Reports & Documents  

| File | Description |
|------|--------------|
| [`student_analysis.ipynb`](student_analysis.ipynb) | Full Python analysis notebook |
| [`student_data.csv`](student_data.csv) | Clean dataset from Kaggle |
| [`analysis_report.txt`](analysis_report.txt) | Model performance metrics |
| [`project-report.pdf`](project-report.pdf) | Final academic report (Persian + English summary) |
| [`داده کاوی - وضعیت تحصیلی.docx`](داده%20کاوی%20-%20وضعیت%20تحصیلی.docx) | Full Persian course submission |
| `/images/` | Visualizations for EDA & model interpretation |

---

## 💬 Conclusions  

- **Internet availability** and **maternal education** are the strongest determinants of success.  
- Behavioral factors like **alcohol use** and **absences** significantly reduce performance.  
- ML models such as **Random Forest** can help identify students who need early academic support.  
- Combining **statistical methods** and **AI models** offers actionable insight for schools and policymakers.

---

## ⚙️ How to Run  

```bash
# Clone the repo
git clone https://github.com/RaGR/student-grade-analysis.git
cd student-grade-analysis

# Open Jupyter Notebook
jupyter notebook student_analysis.ipynb
# or with VScode extentions
````

---

## 🧾 Citation

If you use this project for research or educational purposes, please cite:

**Samadi, Ramtin.** *Student Grade Analysis – Predictive Modeling of Academic Performance (2025).*
GitHub Repository: [https://github.com/RaGR/student-grade-analysis](https://github.com/RaGR/student-grade-analysis)

---

## 🧩 License

This project is licensed under the **MIT License** — you’re free to use, modify, and distribute with attribution.

---

## 🌐 Author

**👤 Ramtin Samadi**
Software Engineer | Data Analyst | AI Automation Developer
📧 [ramtin7.samadi@gmail.com](mailto:ramtin7.samadi@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/ramtin-samadi-ragr7/) • [GitHub](https://github.com/RaGR)

---

### ⭐ If you found this project useful, consider giving it a star!

It helps others discover the work and motivates further open-source research.

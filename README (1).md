# Student Performance Predictor

A beginner-friendly Machine Learning project that predicts whether a student will **PASS** or **FAIL** based on:

- **Score/Marks** (`score`)
- **Attendance** (`att`)
- **Study hours per day** (`hrs`)

The project generates a **synthetic dataset**, trains a **Logistic Regression** classifier, prints model accuracy, saves the trained model as `model.joblib`, and optionally allows interactive predictions from the terminal.

---

## Tech Stack

- **Python**
- **NumPy**
- **Pandas**
- **scikit-learn**
- **joblib**

---

## Project Structure

```text
Student-Performance-Predictor/
├── README.md
└── Student Performance Predictor/
    ├── student_predictor.py
    ├── requirements.txt
    ├── output.txt
    ├── output_report.txt
    └── Student Project Report.pdf
```

---

## How It Works

1. **Data Generation (Synthetic)**
   - Random values are created for `score`, `att`, and `hrs`.
   - A rule-based formula (with some randomness) determines the result label (`res`):
     - `res = 1` → PASS  
     - `res = 0` → FAIL

2. **Training**
   - Features: `[score, att, hrs]`
   - Model: `LogisticRegression(solver="liblinear")`
   - Train/Test split: 80/20

3. **Evaluation**
   - Prints accuracy on the test set.

4. **Model Saving**
   - Saves trained model to: `model.joblib`

5. **Prediction**
   - Interactive terminal loop where you enter values and get **PASS/FAIL** output.

---

## Installation & Setup

### 1) Clone the Repository
```bash
git clone https://github.com/KARTIKEYSINGH009/Student-Performance-Predictor.git
cd Student-Performance-Predictor
```

### 2) (Recommended) Create a Virtual Environment
```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate
```

### 3) Install Dependencies
Your requirements file is inside the project folder:

```bash
pip install -r "Student Performance Predictor/requirements.txt"
```

---

## Run the Project

### Option A: Train + Interactive Prediction
```bash
python "Student Performance Predictor/student_predictor.py"
```

Example flow:
- It will train the model
- Print accuracy
- Save `model.joblib`
- Ask for user input (`score`, `att`, `hrs`) and output **PASS/FAIL**

### Option B: Train Only (No Interactive Input)
```bash
python "Student Performance Predictor/student_predictor.py" --no-input
```

---

## Output

After running, you will see:
- A preview of generated data (`df.head()`)
- Model accuracy
- A confirmation that `model.joblib` is saved

Example:
```text
Student Predictor
accuracy: 0.86xx
saved model.joblib
```

---

## Notes / Limitations

- The dataset is **synthetic**, so accuracy is based on generated rules, not real-world student data.
- This is a learning project meant to demonstrate:
  - dataset creation
  - model training
  - evaluation
  - saving a model
  - taking input from the command line

---

## Future Improvements

- Add visualizations (matplotlib / seaborn)
- Use a real dataset (CSV) instead of random data
- Add more features (sleep hours, assignments, stress level, etc.)
- Build a UI (Streamlit / Flask)
- Improve evaluation using confusion matrix and balanced data

---

## Author

**Kartikey Singh**  
VIT Bhopal University
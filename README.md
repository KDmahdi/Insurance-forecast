# Medical Insurance Cost Prediction 🩺💰

---

## 📝 Overview

Welcome to the Medical Insurance Cost Prediction project! This project utilizes a **Multiple Linear Regression** model to predict medical insurance costs based on a number of personal attributes. The main goal is to help insurance companies make more accurate pricing decisions and allow individuals to understand the key factors that drive their insurance expenses.

This notebook walks through the entire process, from data cleaning and preprocessing to model training and evaluation.

---

## 📄 Dataset

The project uses the `medical_insurance.csv` dataset, which contains the following columns:

- **`age`**: Age of the primary beneficiary.
- **`gender`**: Gender of the insurance contractor (male/female).
- **`bmi`**: Body Mass Index, providing an understanding of body weight relative to height.
- **`children`**: Number of children/dependents covered by the health insurance.
- **`discount_eligibility`**: Indicates whether the person is eligible for a discount (yes/no).
- **`region`**: The beneficiary's residential area in the US (e.g., southwest, southeast).
- **`expenses`** (Target 🎯): Individual medical costs billed by health insurance.
- **`premium`** (Target 🎯): The amount paid for the insurance policy.

---

## ⚙️ Project Workflow

The project follows these key steps:

1.  **Data Loading**: The dataset is loaded into a `pandas` DataFrame.
2.  **Data Preprocessing & Cleaning**:
    - **Categorical Encoding**: Text-based columns were converted into a numerical format that the model can understand.
        - `gender` and `discount_eligibility` were mapped to binary values (0/1).
        - `region` was transformed using **One-Hot Encoding**.
3.  **Model Training**:
    - The dataset was split into **80% for training** and **20% for testing**.
    - A `LinearRegression` model from `scikit-learn` was trained to predict two target variables (`expenses` and `premium`) at the same time.
4.  **Model Evaluation**: The model's performance was assessed on the test data to ensure its accuracy and reliability.

---

## 📊 Results & Evaluation

The model's performance was evaluated using standard regression metrics. Here are the results on the test set:

- **R² Score**: **0.65**
  - This indicates that our model can explain approximately **65%** of the variance in the insurance costs, which is a solid start!
- **Mean Absolute Error (MAE)**: `2185.31`
- **Mean Squared Error (MSE)**: `18068739.14`

These results show that features like age, BMI, and discount eligibility have a significant impact on insurance costs.

---

## 🚀 How to Run This Project

To run this project on your local machine, follow these simple steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```
    *(Don't forget to replace `your-username/your-repository-name` with your actual GitHub info!)*

2.  **Install the necessary libraries:**
    ```bash
    pip install pandas numpy scikit-learn jupyterlab
    ```

3.  **Run the Jupyter Notebook:**
    ```bash
    jupyter lab bime.ipynb
    ```

And you're all set! Feel free to explore the notebook, tweak the model, and see how you can improve the results. Happy coding! ✨

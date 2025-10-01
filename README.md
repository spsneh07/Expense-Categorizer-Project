# Expense-Categorizer-Project
# Smart Expense Categorizer 🧾

## Objective
This project is a machine learning model that automatically categorizes financial transactions based on their text descriptions. For example, it classifies a text like 'Zomato order' into the 'Food' category. This was completed as Task 2 of the 2nd Year Tasks.

---

## Tech Stack
* **Language:** Python
* **Libraries:**
    * Pandas (for data manipulation)
    * Scikit-learn (for model building and evaluation)
    * Jupyter Notebook (for development)

---

## Implementation Details

The project follows a standard machine learning workflow:

1.  **Data Collection:** A custom dataset of over 100 transaction examples was created and saved in `transactions.csv`.
2.  **Data Preparation:** The text was cleaned by converting it to lowercase and removing all non-alphabetic characters.
3.  **Feature Extraction:** The cleaned text was converted into numerical features using `TfidfVectorizer`, which also removed common English stop words.
4.  **Modeling:** A `LinearSVC` (Linear Support Vector Classifier) model was chosen for classification.
5.  **Evaluation:** The model's performance was robustly evaluated using 5-fold cross-validation to get a stable and reliable accuracy score.

---

## Results
The final model achieved a cross-validation accuracy of **~27%**. While the overall score is modest, the model performs very well on key categories with sufficient data, correctly identifying transactions for Food, Travel, and Bills.

**Example Predictions:**
* 'Coffee at Starbucks' ==> Predicted Category: **Food**
* 'IRCTC Ticket Booking' ==> Predicted Category: **Travel**
* 'Monthly rent transfer' ==> Predicted Category: **Bills & Utilities**

---

## How to Run
1.  Clone the repository.
2.  Make sure you have Python and the required libraries (`pandas`, `scikit-learn`) installed.
3.  Place the `transactions.csv` file in the same directory.
4.  Run the `expense_categorizer.ipynb` notebook.

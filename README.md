# Sentimental Analysis of Restaurant Reviews

## Project Description
This project performs sentiment analysis on restaurant reviews to classify them as either positive (1) or negative (0). The goal is to build a model that can accurately predict the sentiment of a new review. The dataset used contains 1000 reviews.

---

## Structure
- `notebooks/`: Notebooks with EDA and model
- `data/`: Dataset files

---

## Methodology
The project follows these key steps:
1.  **Data Loading:** The dataset `Restaurant_Reviews.tsv` is loaded into a pandas DataFrame.
2.  **Data Cleaning & Preprocessing:**
    * Special characters are removed, and all text is converted to lowercase.
    * Text is tokenized (split into words).
    * Common English stopwords (like "the", "a", "is") are removed using NLTK.
    * Words are stemmed to their root form (e.g., "loved" becomes "love") using PorterStemmer.
3.  **Feature Extraction:** The cleaned text is converted into numerical features using the Bag of Words model (CountVectorizer), limited to the 1500 most frequent words.
4.  **Model Training:** A **Multinomial Naive Bayes** classifier is trained on 80% of the data.
5.  **Model Evaluation & Tuning:**
    * The model is tested on the remaining 20% of the data.
    * Hyperparameter tuning was performed for the `alpha` value to find the best-performing model.

---

## Results
The final model achieved the following performance on the test set:
* **Accuracy:** 78.5%
* **Precision:** 76.42% (with default alpha)
* **Recall:** 78.64% (with default alpha)

The best accuracy of **78.5%** was achieved with an `alpha` value of **0.2**.

The confusion matrix for the predictions was:
* **True Positives:** 81
* **True Negatives:** 72
* **False Positives:** 25
* **False Negatives:** 22

---

## How to Run This Project
1.  **Clone the repository:**
    ```bash
    git clone [URL_of_your_repository]
    ```
2.  **Install dependencies:**
    Make sure you have Python installed. Then, install the required libraries using the `requirements.txt` file.
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run the notebook:**
    Open the `Sentimental Analysis of Restaurant Review .ipynb` file in Jupyter Notebook or Google Colab and run the cells sequentially.

---

## Author
* **Rishabh kumar**

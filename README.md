# Fake-news-classifier
Fake news detection has become increasingly important in the modern world. By analyzing the textual content of news articles, we can determine whether an article is real or fake based on patterns found in the text.

### Key Steps

1. Data Preprocessing: 
    - Handling missing values.
    - Merging the `author` and `title` columns for better feature representation.
    - Stemming of words to reduce them to their root form.
    - Converting the textual data into numerical vectors using TF-IDF.

2. Modeling:
    - Logistic Regression model is used to classify news as real or fake.
    - The model is trained and tested using an 80-20 train-test split.

3. Evaluation:
    - The model achieves an accuracy of **97.9%** on the testing dataset.

## Dataset

The dataset contains the following columns:
- `author`: Author of the news article.
- `title`: Title of the news article.
- `content`: Combined text of author and title after preprocessing.
- `label`: Binary label indicating whether the news is real (0) or fake (1).

### Data Preprocessing

1. **Filling Missing Values**: Missing values in the dataset are filled with empty strings to ensure clean input data.
   
2. **Stemming**: 
    - Used the Porter Stemmer to convert words into their root forms (e.g., "running" to "run").
    - Removed stop words to improve the model's focus on meaningful content.

3. **TF-IDF Vectorization**:
    - Textual data is converted into numerical data using Term Frequency-Inverse Document Frequency (TF-IDF) vectorization to capture important words and reduce the dimensionality of the dataset.

## Model

- **Logistic Regression**: A linear model used for binary classification.
- **Accuracy on Training Data**: ~99%.
- **Accuracy on Testing Data**: **97.9%**.

## Dependencies

To run this project, you will need the following Python libraries:

- pandas
- scikit-learn
- nltk
- re
- matplotlib
- seaborn

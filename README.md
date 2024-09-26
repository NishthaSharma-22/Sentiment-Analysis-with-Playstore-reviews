# Sentiment-Analysis-with-Playstore-reviews
Performed sentiment analysis for XYZ company on playstore reviews to categorize customer reviews as 'POSITIVE' or 'NEGATIVE'

## INTRODUCTION:

**AIM**: To perform sentiment analysis on Google Play Store app reviews, classifying them as either "Positive" or "Negative" <br>
**DATASET USED**: Sample dataset was sourced from kaggle.<br>
**TOOLS AND LIBRARIES**: This project is made with Python and uses:<br>
- NLTK for text preprocessing<br>
- sci-kit learn for machine learning for ML models (Logistic regression, naive bayes)<br>
- Pandas for data manipulation<br>
- Seaborn and Matplotlib  for data visualization (making confusion matrices)<br>

## DATA UNDERSTANDING:
Dataset had 2 useful columns with user reviews and another one with score for those  reviews on a scale of 1 to 5, where:<br>
- 1 = Very Negative<br>
- 2 = Negative<br>
- 3 = Neutral <br>
- 4 = Positive<br>
- 5 =  Very Positive<br>

## DATA PREPROCESSING:
**Text Cleaning**: Used NLTK for:<br>
- Tokenization<br>
- Stop word removal<br>
- Lemmatization<br>

**Label Assignment**:<br>
Scores of 1 and 2 are labeled as negative<br>
Scores of 4 and 5 are labeled as positive<br>
Neutral Scores (3) are removed from the dataset<br>

## FEATURE EXTRACTION:
**TF-IDF** (Text-frequency inverse document frequency): <br>
Used TfidfVectorizer to convert the cleaned text into numerical features suitable for machine learning models.<br>
Limited the feature size to 6000 terms for efficient computation while preventing overfit.<br>

## MODEL IMPLEMENTATION:
### **Logistic Regression**: 
- Initially implemented logistic regression<br>
- **Accuracy** achieved: **87%** <br>
- **Pros**: Simple and easy to interpret, excellent for binary classification<br>
- **Cons**: Assumes linear relation between features, and best useful when datasets are small- medium sized.<br>

### **Naive Bayes**:
- Decided to implement naive bayes to compare accuracy<br>
- Achieved accuracy of **85%** <br>
- **Pros**: Simple and effective for text processing<br>
- **Cons**: Assumes no interrelation between words, hence ‘naive’ <br>

## CONCLUSION:
Logistic Regression was the best-performing model with an accuracy of 87%. Naive Bayes came close but was slightly lower in performance.

## Future Work:
Use advanced models and explore word embeddings.

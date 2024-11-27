# Comprehensive Report on Instagram Mental Health Analysis using Sentiment Analysis 
---

## **1. Data Preprocessing**

To prepare the data for analysis and modelling, various preprocessing steps were applied:

- **Cleaning Text**:
  - Removed special characters, brackets, and other irrelevant symbols.
  - Converted all text to lowercase to ensure uniformity.
- **Stopword Removal**:
  - Common words (e.g., "the", "and") that don't contribute much meaning were removed.
- **Lemmatization**:
  - Converted words to their root forms (e.g., "running" → "run") to reduce feature dimensionality.
- **Tokenization**:
  - Text was split into words and subwords for more granular analysis.
- **Normalization**:
  - Ensured consistent text formats for further processing.

---

## **2. Feature Engineering**

To enhance the predictive power of the data, several features were extracted:
- **TF-IDF**: Captures the importance of words relative to the entire dataset.
  - Example: Words like "happy", "sad", "angry" might score higher due to their association with specific sentiments.
- **N-grams**: Generated bigrams and trigrams to understand word pairings and sequences.
- **Sentiment Metrics**:
  - **Polarity**: Measures sentiment intensity (-1 to +1).
  - **Subjectivity**: Ranges from 0 (objective) to 1 (subjective).

### Top Words by Sentiment
- **Positive Sentiment**: Words like "love", "great", "happy".
- **Negative Sentiment**: Words like "hate", "bad", "sad".

---

## **3. Model Training and Hyperparameter Tuning**

### Models Trained
- **Random Forest**: Robust for handling unstructured data.
- **Support Vector Machine (SVM)**: Effective for high-dimensional text data.
- **Gradient Boosting**: Captures complex interactions among features.
- **Logistic Regression**: Baseline model with interpretable coefficients.

### Hyperparameter Tuning
- **Grid Search**: Optimized parameters like `n_estimators` (Random Forest), `C` (SVM), and `learning_rate` (Gradient Boosting).
- **Example Improvement**:
  - **Gradient Boosting Pre-Tuning F1 Score**: 0.85
  - **Post-Tuning F1 Score**: 0.89

### Best Model
- **Gradient Boosting** achieved the highest F1 score after hyperparameter tuning.
- **Metrics**:
  - **Accuracy**: 88.4%
  - **F1 Score**: 0.89

---

## **4. Model Evaluation**

### Confusion Matrix Analysis
The confusion matrix shows the model's classification performance:
- **Positive Sentiment**: High precision and recall.
- **Neutral Sentiment**: Some misclassifications with Negative Sentiments.
- **Negative Sentiment**: Balanced performance.

| Actual \ Predicted | Positive | Neutral | Negative |
|---------------------|----------|---------|----------|
| **Positive**        | 91%      | 5%      | 4%       |
| **Neutral**         | 8%       | 78%     | 14%      |
| **Negative**        | 5%       | 11%     | 84%      |

### Class-wise Performance Metrics
| Class       | Precision | Recall | F1 Score |
|-------------|-----------|--------|----------|
| Positive    | 0.88      | 0.91   | 0.89     |
| Neutral     | 0.80      | 0.78   | 0.79     |
| Negative    | 0.84      | 0.83   | 0.83     |

---

## **5. Visualizations**

### Feature Importance (Random Forest Example)
- **Top Words by Importance**:
  1. "happy"
  2. "sad"
  3. "angry"

### Sentiment Distribution
- **Polarity**:
  - 40% of posts fell in the neutral polarity range.
  - Positive polarity was more frequent than negative.
- **Subjectivity**:
  - Most posts were moderately subjective.

### Word Clouds
- **Positive Sentiment**: Frequent words include "love", "happy", "great".
- **Negative Sentiment**: Frequent words include "hate", "bad", "sad".

---



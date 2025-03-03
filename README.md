# Alphabet Soup Neural Network Model Report

## Overview of the Analysis
Alphabet Soup, a nonprofit foundation, seeks to optimize its funding selection process by identifying applicants with the highest likelihood of success. To accomplish this, I developed a binary classification model using deep learning to predict whether an applicant will effectively utilize the funds provided. By leveraging historical data, we trained and evaluated a neural network to determine its effectiveness in predicting funding success.

---
## Results
### Data Preprocessing
- **Target Variable:** `IS_SUCCESSFUL` (binary outcome: 1 = successful, 0 = unsuccessful)
- **Feature Variables:**
  - `APPLICATION_TYPE` – Type of application submitted
  - `AFFILIATION` – Sector of industry affiliation
  - `CLASSIFICATION` – Government classification
  - `USE_CASE` – Purpose for funding
  - `ORGANIZATION` – Type of organization
  - `STATUS` – Organization’s active status
  - `INCOME_AMT` – Income classification
  - `SPECIAL_CONSIDERATIONS` – Special consideration status
  - `ASK_AMT` – Requested funding amount
- **Removed Variables:**
  - `EIN` – Unique identifier, does not contribute to prediction
  - `NAME` – Organization name, not relevant for classification

---
### Compiling, Training, and Evaluating the Model
- **Neural Network Architecture:**
  - **Input Layer:** Features from the preprocessed dataset
  - **Hidden Layers:**
    - **First layer:** 80 neurons, ReLU activation
    - **Second layer:** 30 neurons, ReLU activation
  - **Output Layer:** 1 neuron, Sigmoid activation (for binary classification)

- **Performance Evaluation:**
  - Initial Model Accuracy: Approximately 71-74%
  - Target Accuracy: 75%+
  
- **Optimization Attempts:**
  1. **Added a third hidden layer** – Resulted in slightly lower accuracy.
  2. **Removed second hidden layer** – Resulted in slightly lower accuracy.
  3. **Increased the number of neurons in each layer** 
  4. **Tuned the optimizer by reducing the learning rate** 
  5. **Tried batch size variations (16 instead 32)**


---
## Summary and Recommendations
### Overall Model Performance
- The deep learning model performed okay (71-73% accuracy) but did not exceed 75%.
- Despite optimizations, the model struggled to exceed even 73% most of the time

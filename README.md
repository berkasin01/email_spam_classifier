# Email Spam Classifier
Binary email classification using a TF-IDF and Logistic Regression pipeline trained on the SpamAssassin public corpus.

## Dataset
SpamAssassin public corpus (2002). 2,500 ham emails and 500 spam emails. Raw email files parsed using Python's built-in email library to extract plain text bodies.

## Pipeline
Raw email text is passed through a single sklearn Pipeline: TF-IDF vectorization with English stop word removal, followed by Logistic Regression classification. No manual preprocessing required at inference time.

## Results
Accuracy: 94.38%
Ham precision: 0.94, recall: 1.00
Spam precision: 1.00, recall: 0.63

## Known Limitation
Spam recall is 0.63. The dataset is from 2002 and modern spam phrases such as "verify your identity" and "bank details" were not well represented in training data, causing some spam to be misclassified as ham.

## Stack
Python, scikit-learn, pandas, matplotlib, seaborn

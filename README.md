# ML_algorithm

Titanic survival prediction, done to compare two classic ML algorithms - Logistic Regression and SVM - on the same dataset.

## What's in here

Used the classic Titanic dataset. First did some basic cleanup - dropped columns that don't really help prediction (PassengerId, Name, Ticket, Cabin), filled missing Age values with the mean, filled missing Embarked values with the mode, and converted Sex and Embarked into numeric columns since models can't work with text directly.

After that, split the data into train/test and trained two models on it:
- Logistic Regression
- SVM (Support Vector Classifier)

Compared both on accuracy and recall, then tested both models on a few made-up passenger records to see who they'd predict as survived or not.

## Files

- `ML_algorithm.ipynb` - the notebook
- `Titanic-Dataset.csv` - dataset used (from the standard Kaggle Titanic dataset)

## Running it

```
pip install pandas scikit-learn
```

Then open the notebook and run top to bottom. Make sure `Titanic-Dataset.csv` is in the same folder.

## Notes

Recall matters here more than plain accuracy honestly, since predicting survival correctly (not missing actual survivors) is usually the more interesting metric on this dataset. Both models did decently, SVM and LR were pretty close on this run - worth trying a Random Forest next to see if it beats both.

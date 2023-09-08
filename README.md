# Logistic Regression - Titantic Survivors

## Question
Can we predict which Titanic passengers survived?

## Data
887 entries

Features:
* `Survived` - no: 0, yes: 1
* `Pclass` - passenger class (1st, 2nd, 3rd)
* `Name`
* `Sex`
* `Age`
* `Siblings/Spouses Aboard` - number of
* `Parents/Children Aboard` - number of
* `Fare` - amount paid for ticket

## Analysis
Analysis included all variables except `Name`.

Histograms were plotted for each variable to check for outliers.<br>
![image](https://github.com/nwferreri/logistic-regression/assets/112211174/98ea0e1e-9fb2-48dd-a2d5-56b846526a50)<br>
No outliers were removed.

Dummy variable was created for `Sex`.

Correlation matrix was created to check for collinearity.<br>
![image](https://github.com/nwferreri/logistic-regression/assets/112211174/953fb3f1-2112-47dc-bb1b-dcfe99e1b3be)<br>
No collinearity was detected between continuous variables.

A logistic regression was created using Logit and found that `Fare` and `Parents/Children Aboard` were statistically insignificant.

## Evaluation
Predictions were made and a Confusion Matrix was generated.<br>
![image](https://github.com/nwferreri/logistic-regression/assets/112211174/b6f9cd73-b0f8-48df-987e-92d02cb576e5)

Classification report showed:
* Precision: Out of all the passengers that the model predicted survived, 65% actually did.
* Recall: Out of all the passengers that actually did survive, the model  predicted this outcome correctly for 63% of those passengers.
* F1 Score: 64%

## Conclusions

Based on the classification report, the model doesn't do a great job of accurately predicting who survives and needs to be improved.

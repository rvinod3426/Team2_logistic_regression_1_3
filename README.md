# Team2_logistic_regression_1_3

## Team Charter
| Field | Your team’s entry |
|---|---|
| Team number | 2 |
| Members (name — **time zone**) | Rohan Vinod - CDT, Catherine Chen - CDT, Bader Almeshri - AST, Felix Lynch - EST|
| Section owners |Data Wrangler (1-3) - Catherine, Analyst (4+6) - Felix, Modeler (5+7) - Rohan, Evaluator (8-9) - Bader, PM / Storyteller (framing, Sec 10, ReadMe + charter) - Everyone|
| Synchronous meeting times (**each member’s local time**) | 4pm CDT, 5pm EST, 11pm AST |
| Async channel + expected response time | Slack for our async communication. While you don't need to reply instantly, please try to check in and respond within 2 hours between 10am and 8pm your local time. |
| How you’ll avoid notebook merge conflicts | All code should be written in the shared Colab notebook. Avoid downloading the notebook, editing it locally, then re-uploading a separate copy. Make sure to save to Github regularly during your async work sessions as well. |

Team members: Rohan Vinod, Catherine Chen, Felix Lynch, Bader Almeshri

## Approach
The goal of this model is to help banks target calls more efficiently by predicting which clients are actually likely to say yes rather than calling everyone at random. To do this, we built the features by one-hot encoding the categorical variables and keeping numeric ones, split the data into 80/20 for training and testing, scaled features with MinMaxScaler (fit on train only to avoid leakage), and trained a logistic regression model. We evaluated it with accuracy, a confusion matrix, and ROC/AUC to see whether the model adds value beyond just predicting the majority class. Our steps were data preprocessing, model building, and evaluation. 


## Final Recommendation
Accuracy alone is not whole for this problem: our model's 89.4% is barely above the 88% lazy baseline, because the data is heavily imbalanced and accuracy prioritizes getting the easy majority class right. The more meaningful result is the AUC of 0.751, which shows the model can meaningfully rank clients by likelihood to subscribe. We recommend the bank use the model's predicted probabilities to rank and prioritize call lists rather than relying on a hard yes/no. This way, the call center can focus effort on the highest-probability clients first, rather than treating the model's binary prediction as final.

## Contribution Log
- Rohan (Modeler) - 6 commits, completed designated Modeler work + ReadME (Sections 5+7)
- Catherine (Data Wrangler/Storyteller) - 1 commit, completed designated Data Wrangler work + Team charter and Sec 10 (Sections 1-3, 10)
- Bader (Evaluator) - 3 commits, completed designated Evaluator work (Sections 8-9)
- Felix (Analyst) - 0 commits (forgot to commit but saved work on CoLab), completed designated Analyst work (Sections 4+6)

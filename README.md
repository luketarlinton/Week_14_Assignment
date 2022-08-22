# Week_14_Assignment

## Establish a Baseline Performance:
### Conclusions:
#### The baseline trading algorithm performed quite well as depicted within the following image of the actual returns vs the strategy returns;
https://github.com/luketarlinton/Week_14_Assignment/blob/main/SVM_Actual_vs_Strategy_ORIGINAL.png
#### The plot indicates that the strategy returns closly follows the same trend as the actual returns with the strategy retunrs outperforming the actual returns. The classification report shows that the algorithm better predicts the buy signals than it does the sell signals. For the buys it produced a precision of .56 (56% accuracy of buy predictions), a recall of .96 (96% of buy signals were correctly identified) and an F1 score of .71 (71% of buy signal predictions were correct when using both the precision and recall scores). For the sell signals, it produced a precision of .43 (43% accuracy of sell predictions), a recall of .04 (4% of sell signals were correctlt identified) and a F1 score of .07 (7% of sell signal predictions were correct when using both the precision and recall scores).


## Tune the Baseline Trading Algorithm:
### What impact resulted from increasing or decreasing the training window?
#### I tuned the baseline trading algorithm by adjusting the dateoffset from 3 to 9 months. This resulted in a slightly more accurate algorithm with the precision scores of both the buy and sell signals increasing slightly. Buy signal precision rose to .57 and the sell signal precision rose to .45.
https://github.com/luketarlinton/Week_14_Assignment/blob/main/SVM_Actual_vs_Strategy_TUNE1.png
#### Although the above image depicts the actual and startegy returns aren't following the same trend as closley the startegy and actual returns are almost identical by 2021.

### What impact resulted from increasing or decreasing either or both of the SMA windows?
#### I tuned the baseline trading algorithm by adjusting both the short and long SMA windows. I increased the short window from 4 to 10 and decreased the long window from 100 to 60. This lead to both the precision scores of the buy and sell signals staying very similair to the baseline. However it lead to a large drop in the recall of the buy signals to .24 and a large rise in the recall for sell signals to .76.
https://github.com/luketarlinton/Week_14_Assignment/blob/main/SVM_Actual_vs_Strategy_TUNE2.png
#### The above plot indicates that the actual and strategy returns are following almost opposite trends with the actual returns ending up on a largely upward trend whilst the strategy returns was on a downward trend.

### Conclusion:
#### Of the two tuned versions the better performing was the algorithm produced by tuned 1 which was adjusted by increasing the dateoffset from 3 to 9 months. The better perfromance is displayed int he below plot;
https://github.com/luketarlinton/Week_14_Assignment/blob/main/SVM_Actual_vs_Strategy_TUNE1.png

## Evaluate a New Machine Learning Classifier:
### Did this new model perform better or worse than the provided baseline model? 
#### The new logistic regression model for the most part outperformed the baseline model. This is depicted in the below plot however towards 2021 the strategy returns begun to take a large dive while the actual returns continued to increase.
https://github.com/luketarlinton/Week_14_Assignment/blob/main/Logistic_Regression_Actual_vs_Strategy.png
The precision scores were very similair to the baseline model, however the logistic regression better identified the sell signals whilst the baseline model better predicted the buy signals. 

### Did this new model perform better or worse than your tuned trading algorithm?
The new logitic regression model outperformed the second tuned trading algorithm whilst it was close in performance to the first tuned trading algorithm.

### Logistic Regresion Model Plot:
https://github.com/luketarlinton/Week_14_Assignment/blob/main/Logistic_Regression_Actual_vs_Strategy.png

### Original Base Model Plot:
https://github.com/luketarlinton/Week_14_Assignment/blob/main/SVM_Actual_vs_Strategy_ORIGINAL.png

### First Tuned Model Plot:
https://github.com/luketarlinton/Week_14_Assignment/blob/main/SVM_Actual_vs_Strategy_TUNE1.png

### Second Tuned Model Plot:
https://github.com/luketarlinton/Week_14_Assignment/blob/main/SVM_Actual_vs_Strategy_TUNE2.png

#### From the above plots it is clear the second tuned model was the worst performing in regards to actual vs strategy returns. The Logistic Regression, Base and First Tuned Model all have their merits and were close in performance. With the First Tuned and the Logistic Regression being the top performers.



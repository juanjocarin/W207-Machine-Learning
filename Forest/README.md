# W207 Final Project

MIDS - Summer semester 2015

* Juanjo Carin
* Tuhin Mahmud
* Vamsi Sakhamuri

**Final version**: https://github.com/juanjocarin/W207-final-project/blob/master/W207-Carin_Mahmud_Sakhamuri.ipynb

[Predictions for the test set submitted to Kaggle](https://github.com/juanjocarin/W207-final-project/blob/master/Forest/test_labeled.csv)

[Presentation](https://docs.google.com/presentation/d/1Apk9JW_TBPbLmRxe0wNuiAUOZle4eu09Er-VbvTrwCs/edit?usp=sharing)

Kaggle competition hosted at https://www.kaggle.com/c/forest-cover-type-prediction

We used the most typical classifiers that we covered in the course, with the exception of **Neural Networks** (week 7). These are:

- **k Nearest Neighbors** (week 2)
- **Naive Bayes** (week 3)
- **Decision Trees**, as well as **Random Forests**, **Extra Trees**, and **AdaBoost** (week 4)
- **Logistic Regression** (week 5)
- **Stochastic Gradient Descent** (week 6)
- **Support Vector Machines** (week 8)
- **Gaussian Mixture Models** (week 10) used for classification

**AdaBoost combined with Extra Trees** yielded the best results, followed by **Extra Trees** alone, **Random Forests**, **Nearest Neighbors**, **SVMs**, **GMMs**, and **Decision Trees**. **Naive Bayes**, **Logistic Regression**, and **SGD** did not perform very well for this problem (and hence they are included in the Annexes at the end).

The analysis of the existing features led us to engineer new ones, which we used to improve that best model (AdaBoost).

Finally we ensembled the results of the best 4 models (**kNN**, **AdaBoost**, **SVMs**, and **GMMs**), weighting them by their accuracy. (We excluded **Decision Trees**, **Random Forests**, and **Extra Trees** since they belong to the same family of methods than **AdaBoost**: they perform similarly, and also tend to make the same misclassification mistakes, so including the four would have "given them advantage" over the other three methods and overweighted those mistakes.)

Nonetheless, the predictions were not as accurate for the test set as they had been for the dev set we created from the training set, because the available data we had to train our models was quite different from the data we had to predict (the former was not a representative sample of the latter, or vice versa).

But still we scored a 79.513% accuracy in the test after submitting to Kaggle, putting us in the 205th position if the competition was still open.



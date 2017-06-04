# MLP_GridSearchCV
Maybe for big samples,dropout is useful.  we can't completely guarentee with dropout is better than without dropout.
the following experienment can prove that small samples is better without dropout layer.

![loss](https://github.com/DreamPurchaseZnz/Picture/blob/master/loss.png)

Depiched from the picture,we can conclude some piont:
* model with dropout layer don't performance well than model without dropout
* model with variety layers get the same loss. that mean ,only one hidden layer can fix the problem.and more hidden layer is not neccessary.

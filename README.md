# MLP_GridSearchCV
Maybe for big samples,dropout is useful.  we can't completely guarentee with dropout is better than without dropout.
the following experienment can prove that small samples is better without dropout layer.

![loss](https://github.com/DreamPurchaseZnz/Picture/blob/master/loss.png)

Depiched from the picture,we can conclude some piont:
* model with dropout layer don't performance well than model without dropout
* model with variety layers get the same loss. that mean ,only one hidden layer can fix the problem.and more hidden layer is not neccessary.
* model with more hidden layer is likely to get overfit and train time increase greatly.when you try to use dropout to solve overfit,you will
find that the training process is becoming fragile and easily break down.maybe it is because of small samples(40)
* model with one hidden layer  preformance best.

# Convolution1D vs MLP
the result is awesome, convolution1D is better in process of train and prediction,which mean less overfitting and more stable trainning.
the the following picture can confirm it:
![cnn](https://github.com/DreamPurchaseZnz/Picture/blob/master/compare_mlp_cnn.png)

mlp may exists some problem ,such as lack of robustness and overfitting.

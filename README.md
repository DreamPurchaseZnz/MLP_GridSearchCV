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
# convolution 1D principle
![principle](https://github.com/DreamPurchaseZnz/Picture/blob/master/con1d/conv1D.JPG)

# Convolution neural network sturcture
![struct](https://github.com/DreamPurchaseZnz/Picture/blob/master/con1d/structure.JPG)

# Convolution1D vs MLP
the result is awesome, convolution1D is better in process of train and prediction,which mean less overfitting and more stable trainning.
the the following picture can confirm it:
![cnn](https://github.com/DreamPurchaseZnz/Picture/blob/master/compare_mlp_cnn.png)

mlp may exists some problem ,such as lack of robustness and overfitting.when you train more than 400 epochs, the loss may loss control,up and down intensely.

Tips 
* When tensorflow rise this error Dst tensor is not initialized. this mean GPU memory is full. so shut down some thread and clean memory.
# Conv2D vs Con1D 
To complemet convolution, there are two ways:one is using con1d just for convolution1d,the other is con2d with proper parameters.there's no differnce in used memory and GPU load.only GPU core clock is defferent.we can see the following picture:

![1d](https://github.com/DreamPurchaseZnz/Picture/blob/master/con1d/cnn1d_GPU%20comsume.png)
![2d](https://github.com/DreamPurchaseZnz/Picture/blob/master/con1d/cnn_GPU%20comsume.png)

we can see the final test result:
![comparison_12](https://github.com/DreamPurchaseZnz/Picture/blob/master/con1d/conparison_Con1D_Con2D.png)

As described in the picture above,we can draw some conclusion: con2d and con1d both can achieve the function of convolution 1D.but up to data,con1D is more suitable,for the reason of more accuracy ,less overfitting and better implement

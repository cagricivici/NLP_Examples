# Purpose:
This code is a comparison btw generic CNN application and ResNet Application. In order to see how good it is, I put the result which is cvs file into Kaggle Competation then it shows that it is 8th ranked of all applicants in there.

# Keynotes:
- Since having the all benefits from pretrained ResNet18, I prefer to preserve all CNN parameters by freezing until the last one of CNN layer. Because last layer is supposed to learn deeper learning so I let it learn more and more while training since the frontlier of layers is frozen because first observations on data is generic such as edge detection, corner detection, convex hulls. I dont want to loose the parameters that comes from pretrained one by re-training again. The model is to learn in last CONV layer and FC Layer.

- In order to make the FC layer stronger, I prefer to put some layers so that it would be not complex or very basic. In order to enhance btw layers, batchnormalization and dropout is playing important keys. When i see the loss and acc graph, I thought that no need to have more regularizaions for the model because it would be risky in overfitting by having K1,K2 regularizations or any penalties.
  ![image](https://github.com/user-attachments/assets/105110f4-c446-417f-a917-f4d34fbe6ce6)

Kaggle Competation:
https://www.kaggle.com/competitions/cifar-10/overview
![image](https://github.com/user-attachments/assets/0ae1dc7d-63ec-4814-97af-cee2583afb22)


- for *W/O RESNET Application* : https://github.com/cagricivici/cifar10/tree/main/cifar10_wo_resnet

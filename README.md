# Fashion MNIST
#### **Implementing Tiny ResNet and training it on fashion images**

Dataset Source: https://www.kaggle.com/datasets/zalando-research/fashionmnist

The CNN model has the following architecture: 
<pre>
Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_16 (Conv2D)           (None, 28, 28, 16)        160       
_________________________________________________________________
lambda_7 (Lambda)            (None, 28, 28, 16)        0         
_________________________________________________________________
activation_1 (Activation)    (None, 28, 28, 16)        0         
_________________________________________________________________
dropout_4 (Dropout)          (None, 28, 28, 16)        0         
_________________________________________________________________
residual_unit_6 (ResidualUni (None, 14, 14, 32)        14336     
_________________________________________________________________
residual_unit_7 (ResidualUni (None, 14, 14, 32)        18432     
_________________________________________________________________
dropout_5 (Dropout)          (None, 14, 14, 32)        0         
_________________________________________________________________
residual_unit_8 (ResidualUni (None, 7, 7, 64)          57344     
_________________________________________________________________
residual_unit_9 (ResidualUni (None, 7, 7, 64)          73728     
_________________________________________________________________
dropout_6 (Dropout)          (None, 7, 7, 64)          0         
_________________________________________________________________
residual_unit_10 (ResidualUn (None, 4, 4, 128)         229376    
_________________________________________________________________
residual_unit_11 (ResidualUn (None, 4, 4, 128)         294912    
_________________________________________________________________
flatten_1 (Flatten)          (None, 2048)              0         
_________________________________________________________________
dense_2 (Dense)              (None, 250)               512250    
_________________________________________________________________
batch_normalization_1 (Batch (None, 250)               1000      
_________________________________________________________________
dropout_7 (Dropout)          (None, 250)               0         
_________________________________________________________________
dense_3 (Dense)              (None, 10)                2510      
=================================================================
Total params: 1,204,048
Trainable params: 1,203,548
Non-trainable params: 500
_________________________________________________________________
</pre>


After training for 27 epochs, the model obtained ``93.35%`` accuracy on the test set. 

The trained model is available in ``./trained_model/tiny_resnet.h5``.

Learning curves is as follows:




 

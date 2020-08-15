# Transfer Learning with CIFAR-10
This notebook demostrates how transfer leaerning can be used to leverage feautures learned by pre-trained models on similar datasets (ImageNet in this case) to build a model for our dataset (CIFAR-10 in this case). The notebook is divided in following sections - 

## Data Preprocessing
* Step-1 => Load CIFAR-10 dataset and prepare batches as per batch-size 
* Step-2 => Perform sanity check by displaying some images and corresponding labels
* Step-3 => Configure dataset for performance by using the AUTOTUNE feature of Tensorflow for managing a input buffer while training
* Step-4 => Add data augmentation to achieve better generalization (can be skipped is dataset is large)
* Step-5 => Rescale the dataset images according to selected model

## Model Building
* Step-1 => Import the base model (MobileNetV2) in this case without the top classification layer. 
* Step-2 => Add a classification head
* Step-3 => Stack the base model and classification layer
* Step-4 => Compile the model and select base learning rate, loss and optimizer

## Training
* Step-1 => Fit the model 
* Step-2 => Plot the train vs validation loss and accuracy plots

## Finetuning
* Step-1 => If the accuracy levels are not upto the expectations, try unfreezing some layers from the base model and train again.
* Step-2 => Plot the train vs validation loss and accuracy plots to see changes

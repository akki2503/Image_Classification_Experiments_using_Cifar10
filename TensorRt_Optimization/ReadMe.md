# TensorRt Optimization

This IPython file demostrates the enhancement in inference time of an Image after
optimizing the Tensorflow Model using TensorRt engine. 

## Building and Training a Tensorflow Model from Scratch

The first section deals with building and training a 3 block VGG style model from scratch.
However, the model overfits and gives a validation accuracy of around 75% it does the job 
for demostration pursposes which the primary aim here. 

![alt text](https://github.com/akki2503/CIFAR_10_experiments/blob/master/TensorRt_Optimization/train_vs_val_loss.png?raw=true)

## Converting Keras .hdf5 model to frozen graph model

Section 2 deals with converting the model from .hdf5 format to frozen graph model and writing it to .pb format.
It also pertaing to performing inference on a image from the web and displaying infernece time.

Its important to convert the keras model or a tensorflow model to frozen graph as Tensorflow models contain all of the millions of variables including gradients. Think about it, you don’t need the gradients when you deploy your model on a webserver so why carry all this load. Freezing is the process to identify and save all of required things(graph, weights etc) in a single file that you can easily use.  

![alt text](https://github.com/akki2503/CIFAR_10_experiments/blob/master/TensorRt_Optimization/frozen_graph_model_inference.png?raw=true)

## Installing the required libraries and packages for TensorRT Optimization

The experiment is performed on a remote machine using Google Colab. The libraries and packages compatible with the CUDA version installed on it have to be chosen accordingly from the nvidia webiste.

For experimenting in google colab, "nv-tensorrt-repo-ubuntu1804-cuda10.0-trt5.1.5.0-ga-20190427_1-1_amd64.deb".
Install the corresponding tensorrt repo from NVIDIA repository and save it to the ``/content/drive/My\ Drive/python/`` location in your google drive. 

## Building the TensorRt Engine and calculating inference time 

The last section demostrates how to build the TensorRt Engine and perform Inference using the optimized model.

## Results

The inference time of the model increases by almost 3X when optimized using TensorRt making it a viable tool for deployment in real-time applications. 

![alt text](https://github.com/akki2503/CIFAR_10_experiments/blob/master/TensorRt_Optimization/tensorrt_model_inference.png?raw=true)

## License
[MIT](https://choosealicense.com/licenses/mit/)

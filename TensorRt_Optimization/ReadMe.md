# TensorRt Optimization

This IPython file demostrates the enhancement in inference time of an Image after
optimizing the Tensorflow Model using TensorRt engine. 

## Building and Training a Tensorflow Model from Scratch

The first section deals with building and training a 3 block VGG style model from scratch.
However, the model overfits and gives a validation accuracy of around 75% it does the job 
for demostration pursposes which the primary aim here. 

![alt text](https://github.com/akki2503/CIFAR_10_experiments/blob/master/TensorRt_Optimization/train_vs_val_loss.png?raw=true)

## Usage

```python
import foobar

foobar.pluralize('word') # returns 'words'
foobar.pluralize('goose') # returns 'geese'
foobar.singularize('phenomena') # returns 'phenomenon'
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)

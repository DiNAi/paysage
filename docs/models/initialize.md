# Documentation for Initialize (initialize.py)

## functions

### glorot\_normal
```py

def glorot_normal(batch, model, **kwargs)

```



Initialize the parameters of an RBM.<br /><br />Identical to the 'hinton' method above<br />with the variation that we initialize the weights according to<br />the prescription of Glorot and Bengio from<br /><br />"Understanding the difficulty of training deep feedforward neural networks", 2010:<br /><br />Initialize the weights from N(0, \sigma)<br />with \sigma = \sqrt(2 / (num_vis_units + num_hidden_units)).<br /><br />Set hidden_bias = 0<br />Set visible_bias = inverse_mean( \< v_i \> )<br />If visible_scale: set visible_scale = \< v_i^2 \> - \< v_i \>^2<br /><br />Notes:<br />&nbsp;&nbsp;&nbsp;&nbsp;Modifies the model parameters in place.<br /><br />Args:<br />&nbsp;&nbsp;&nbsp;&nbsp;batch: A batch object that provides minibatches of data.<br />&nbsp;&nbsp;&nbsp;&nbsp;model: A model to initialize.<br /><br />Returns:<br />&nbsp;&nbsp;&nbsp;&nbsp;None


### hinton
```py

def hinton(batch, model, **kwargs)

```



Initialize the parameters of an RBM.<br /><br />Based on the method described in:<br /><br />Hinton, Geoffrey.<br />"A practical guide to training restricted Boltzmann machines."<br />Momentum 9.1 (2010): 926.<br /><br />Initialize the weights from N(0, \sigma)<br />Set hidden_bias = 0<br />Set visible_bias = inverse_mean( \< v_i \> )<br />If visible_scale: set visible_scale = \< v_i^2 \> - \< v_i \>^2<br /><br />Notes:<br />&nbsp;&nbsp;&nbsp;&nbsp;Modifies the model parameters in place.<br /><br />Args:<br />&nbsp;&nbsp;&nbsp;&nbsp;batch: A batch object that provides minibatches of data.<br />&nbsp;&nbsp;&nbsp;&nbsp;model: A model to initialize.<br /><br />Returns:<br />&nbsp;&nbsp;&nbsp;&nbsp;None


### pca
```py

def pca(batch, model, **kwargs)

```



Initialize the parameters of an RBM using the principal components<br />to initialize the weights.<br /><br />Notes:<br />&nbsp;&nbsp;&nbsp;&nbsp;Modifies the model parameters in place.<br /><br />Args:<br />&nbsp;&nbsp;&nbsp;&nbsp;batch: A batch object that provides minibatches of data.<br />&nbsp;&nbsp;&nbsp;&nbsp;model: A model to initialize.<br /><br />Returns:<br />&nbsp;&nbsp;&nbsp;&nbsp;None


### stddev
```py

def stddev(batch, model, **kwargs)

```



Initialize the parameters of an RBM. Set the rows of the weight matrix<br />proportional to the standard deviations of the visible units.<br /><br />Notes:<br />&nbsp;&nbsp;&nbsp;&nbsp;Modifies the model parameters in place.<br /><br />Args:<br />&nbsp;&nbsp;&nbsp;&nbsp;batch: A batch object that provides minibatches of data.<br />&nbsp;&nbsp;&nbsp;&nbsp;model: A model to initialize.<br /><br />Returns:<br />&nbsp;&nbsp;&nbsp;&nbsp;None


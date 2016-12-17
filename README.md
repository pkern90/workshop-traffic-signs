# workshop-traffic-signs

## Data
For this workshop we will be using the [German Traffic Sign Recognition Benchmark Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=news). Particularly a preprocessed version from [Udacity](https://www.udacity.com/) which is also used in one of the projects in their [Self-Driving Car Nanodegree Programm](https://www.udacity.com/course/self-driving-car-engineer-nanodegree--nd013). In this version all the images are resized to 32x32 pixels and already split into a train and test set. The data can be downloaded [here](https://drive.google.com/open?id=0B02X9kiSe3GBamlKYndVMi1raGM).

![Sample traffix signs](images/signs.png)

## Setup

We will use python 3.5 with the following packages:

- [jupyter](http://jupyter.org/)
- [NumPy](http://www.numpy.org/)
- [scikit learn](http://scikit-learn.org/stable/)
- [matplotlib](http://matplotlib.org/)
- [seaborn](http://seaborn.pydata.org/)
- [tqdm](https://pypi.python.org/pypi/tqdm)
- [TensorFlow](http://tensorflow.org)
- [Keras](https://keras.io/)

The easiest way to get started is by installing [anaconda](https://www.continuum.io/downloads). Anaconda allows to create virtual environments to keep everything nice an clean. After installing anaconda your command line tool of choice and execute the following statements.

### Environment

The next line will create a new environment with python 3.5 and install numpy, jupyter, matplotlib, scikit-learn and seaborn. Replace "env-name" with the name you want to call your environment.

```
conda create -n env-name python=3.5 numpy jupyter matplotlib scikit-learn seaborn
```

After the environment was created you have to activate it before you can install additional packages or actually use it. How you activate an environment depends on you OS. Remember to replace "env-name" with the name you chose.

**Linux, OS X:**
```
source activate env-name
```

**Windows:**
```
activate env-name
```


### tqdm
tqdm can now be installed with the following command.
```
pip install tqdm
```

### Tensorflow

Next step is to install tensorflow which can be installed with or without gpu support. Since the gpu version is more complicate to setup and requires additional libraries like Cuda we will go with the cpu version for now. Still if you have a powerful gpu you can follow the official setup [guide](https://www.tensorflow.org/get_started/os_setup) to install the gpu version which will be a lot faster. 


**Windows:**
```
pip install --upgrade https://storage.googleapis.com/tensorflow/windows/cpu/tensorflow-0.12.0rc1-cp35-cp35m-win_amd64.whl
```

**Linux:**
```
export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-0.12.0rc1-cp35-cp35m-linux_x86_64.whl
pip install --ignore-installed --upgrade $TF_BINARY_URL
```

**OS X:**
```
export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-0.12.0rc1-py3-none-any.whl
pip install --ignore-installed --upgrade $TF_BINARY_URL
```

### Keras

Finally install keras.
```
pip install keras
```

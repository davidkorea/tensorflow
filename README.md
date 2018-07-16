# tensorflow

# Issue 1 - MAC install tensorflow

1. Install pip3

```$ python3 -m easy_install pip```
```
  Searching for pip                                                                                         
  Best match: pip 10.0.1           
  Adding pip 10.0.1 to easy-install.pth file         
  Installing pip script to /usr/local/bin                                                                   
  Installing pip3 script to /usr/local/bin                                                                  
  Installing pip3.6 script to /usr/local/bin     

  Using /usr/local/lib/python3.6/site-packages                                                              
  Processing dependencies for pip                                                                           
  Finished processing dependencies for pip                                                                  
```
2. Install tensorflow

```$ pip3 install tensorflow```

# Issue 2 - Win7 

1. Re-install to the path without space

```$ conda create -n tensorflow pip install python=3.5```
```
  WARNING: A space was detected in your requested environment path
  'e:\Program Files\Anaconda3\envs\tensorflow'
  Spaces in paths can sometimes be problematic.
  Solving environment: failed
```
2. Warnings that could ignore?
```
  >>> import tensorflow as tf
  >>> sess = tf.Session()

  2018-07-17 00:46:16.481492: I T:\src\github\tensorflow\tensorflow\core\platform\
  cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow bi
  nary was not compiled to use: AVX2

  >>> hello = tf.constant('hello, tensor flow')
  >>> print(sess.run(hello))
  b'hello, tensor flow'
```
  reference:
  [Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX AVX2](https://stackoverflow.com/questions/47068709/your-cpu-supports-instructions-that-this-tensorflow-binary-was-not-compiled-to-u)

# tensorflow

# Issue 4 - Open Tensorborad in Kaggle Kernel

1. open tensorboard locally

```python
writer = tf.summary.FileWriter('./graph1', sess.graph)
writer.close()
sess.close()

!tensorboard --logdir='./graph1'
```


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

# Issue 2 - Win7 install tensorflow

1. Re-install to the path without space

```$ conda create -n tensorflow pip python=3.5```
```
WARNING: A space was detected in your requested environment path
'e:\Program Files\Anaconda3\envs\tensorflow'
Spaces in paths can sometimes be problematic.
Solving environment: failed
```

2. Do as the official guidebook - [Installing with Anaconda](https://www.tensorflow.org/install/install_windows?hl=ko)

```$ C:> conda create -n tensorflow pip python=3.5 ```

```$ C:> activate tensorflow```

```$ (tensorflow)C:> pip install --ignore-installed --upgrade tensorflow ```


3. Warnings that could ignore?
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
  
  
 # Issue 3 - Win10 import error
 
 **Unfixed**
 
 ```
 >>> import tensorflow as tf
Traceback (most recent call last):
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\python\pywrap_tensorflow_internal.py", line 14, in swig_import_helper
    return importlib.import_module(mname)
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\importlib\__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "<frozen importlib._bootstrap>", line 985, in _gcd_import
  File "<frozen importlib._bootstrap>", line 968, in _find_and_load
  File "<frozen importlib._bootstrap>", line 957, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 666, in _load_unlocked
  File "<frozen importlib._bootstrap>", line 577, in module_from_spec
  File "<frozen importlib._bootstrap_external>", line 938, in create_module
  File "<frozen importlib._bootstrap>", line 222, in _call_with_frames_removed
ImportError: DLL load failed: DLL 초기화 루틴을 실행할 수 없습니다.

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\python\pywrap_tensorflow_internal.py", line 17, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\python\pywrap_tensorflow_internal.py", line 16, in swig_import_helper
    return importlib.import_module('_pywrap_tensorflow_internal')
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\importlib\__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
ImportError: No module named '_pywrap_tensorflow_internal'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\__init__.py", line 22, in <module>
    from tensorflow.python import pywrap_tensorflow  # pylint: disable=unused-import
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\python\__init__.py", line 49, in <module>
    from tensorflow.python import pywrap_tensorflow
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\python\pywrap_tensorflow.py", line 74, in <module>
    raise ImportError(msg)
ImportError: Traceback (most recent call last):
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\python\pywrap_tensorflow_internal.py", line 14, in swig_import_helper
    return importlib.import_module(mname)
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\importlib\__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "<frozen importlib._bootstrap>", line 985, in _gcd_import
  File "<frozen importlib._bootstrap>", line 968, in _find_and_load
  File "<frozen importlib._bootstrap>", line 957, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 666, in _load_unlocked
  File "<frozen importlib._bootstrap>", line 577, in module_from_spec
  File "<frozen importlib._bootstrap_external>", line 938, in create_module
  File "<frozen importlib._bootstrap>", line 222, in _call_with_frames_removed
ImportError: DLL load failed: DLL 초기화 루틴을 실행할 수 없습니다.

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\python\pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\python\pywrap_tensorflow_internal.py", line 17, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\site-packages\tensorflow\python\pywrap_tensorflow_internal.py", line 16, in swig_import_helper
    return importlib.import_module('_pywrap_tensorflow_internal')
  File "C:\Users\xerox\Anaconda3\envs\tensorflow\lib\importlib\__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
ImportError: No module named '_pywrap_tensorflow_internal'


Failed to load the native TensorFlow runtime.

See https://www.tensorflow.org/install/install_sources#common_installation_problems

for some common reasons and solutions.  Include the entire stack trace
above this error message when asking for help.
>>>
 ```

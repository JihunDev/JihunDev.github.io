---
layout: post
title: RaspberryPi TensorFlow 설치
tags: RaspberryPi
comments: true
use_math: true
---

# RaspberryPi 3 B+ install Tensorflow

## Version
- Board Raspberry Pi3 B+
- OS 2018-06-27-raspbian-stretch-lite
- Python 3.5.2

## Guide
[TensorFlow on Raspbian](https://www.tensorflow.org/install/install_raspbian)

## install

### Raspbian Update
```shell
$ sudo apt-get update
$ sudo apt-get upgrade -y
```

### pip install
```shell
$ sudo apt-get install python3-pip
$ pip3 -V
```

### Altas install
- 선형 대수 라이브러리 
- numpy 의존성
```shell
$ sudo apt install libatlas-base-dev
```

### Tensorflow install
```shell
$ pip3 intall tensorflow
```


## Trouble Shooting

#### ImportError: No module named PIL
##### Err Message
```shell
pi@raspberrypi:~/dummy_classification $ python3 DDD_20180812_interpreter_v1.py
Traceback (most recent call last):
  File "DDD_20180812_interpreter_v1.py", line 4, in <module>
    from PIL import Image
ImportError: No module named 'PIL'
```
##### Solution
```shell
$ sudo apt-get install libjpeg-dev libfreetype6 libfreetype6-dev zlib1g-dev
$ pip install pillow
```

#### ImportError: libopenjp2.so.7
##### Err Message
```shell
pi@raspberrypi:~/dummy_classification $ python3 DDD_20180812_interpreter_v1.py
Traceback (most recent call last):
  File "DDD_20180812_interpreter_v1.py", line 4, in <module>
    from PIL import Image
  File "/home/pi/.local/lib/python3.5/site-packages/PIL/Image.py", line 64, in <module>
    from . import _imaging as core
ImportError: libopenjp2.so.7: cannot open shared object file: No such file or directory
```
##### Solution
```shell
$ sudo apt-get install libopenjp2-7
```

#### ImportError: libtiff.so.5
##### Err Message
```shell
pi@raspberrypi:~/dummy_classification $ python3 DDD_20180812_interpreter_v1.py
Traceback (most recent call last):
  File "DDD_20180812_interpreter_v1.py", line 4, in <module>
    from PIL import Image
  File "/home/pi/.local/lib/python3.5/site-packages/PIL/Image.py", line 64, in <module>
    from . import _imaging as core
ImportError: libtiff.so.5: cannot open shared object file: No such file or directory
```
##### Solution
```shell
$ sudo apt-get install libtiff5
```

#### ImportError: tensorflow_wrap_interpreter_wrapper.so
##### Err Message
```shell
pi@raspberrypi:~/dummy_classification $ python3 DDD_20180812_interpreter_v1.py
/usr/lib/python3.5/importlib/_bootstrap.py:222: RuntimeWarning: compiletime version 3.4 of module 'tensorflow.python.framework.fast_tensor_util' does not match runtime version 3.5
  return f(*args, **kwds)
/usr/lib/python3.5/importlib/_bootstrap.py:222: RuntimeWarning: builtins.type size changed, may indicate binary incompatibility. Expected 432, got 412
  return f(*args, **kwds)
Traceback (most recent call last):
  File "DDD_20180812_interpreter_v1.py", line 53, in <module>
    prediction = load_and_inteprete(testimages[i], modelfullpath, labelfilefullpath)
  File "DDD_20180812_interpreter_v1.py", line 20, in load_and_inteprete
    interpreter = interpreter_wrapper.Interpreter(model_path=modelpathname)
  File "/home/pi/.local/lib/python3.5/site-packages/tensorflow/contrib/lite/python/interpreter.py", line 50, in __init__
    _interpreter_wrapper.InterpreterWrapper_CreateWrapperCPPFromFile(
  File "/home/pi/.local/lib/python3.5/site-packages/tensorflow/python/util/lazy_loader.py", line 53, in __getattr__
    module = self._load()
  File "/home/pi/.local/lib/python3.5/site-packages/tensorflow/python/util/lazy_loader.py", line 42, in _load
    module = importlib.import_module(self.__name__)
  File "/usr/lib/python3.5/importlib/__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "<frozen importlib._bootstrap>", line 986, in _gcd_import
  File "<frozen importlib._bootstrap>", line 969, in _find_and_load
  File "<frozen importlib._bootstrap>", line 958, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 673, in _load_unlocked
  File "<frozen importlib._bootstrap_external>", line 673, in exec_module
  File "<frozen importlib._bootstrap>", line 222, in _call_with_frames_removed
  File "/home/pi/.local/lib/python3.5/site-packages/tensorflow/contrib/lite/python/interpreter_wrapper/tensorflow_wrap_interpreter_wrapper.py", line 28, in <module>
    _tensorflow_wrap_interpreter_wrapper = swig_import_helper()
  File "/home/pi/.local/lib/python3.5/site-packages/tensorflow/contrib/lite/python/interpreter_wrapper/tensorflow_wrap_interpreter_wrapper.py", line 24, in swig_import_helper
    _mod = imp.load_module('_tensorflow_wrap_interpreter_wrapper', fp, pathname, description)
  File "/usr/lib/python3.5/imp.py", line 242, in load_module
    return load_dynamic(name, filename, file)
  File "/usr/lib/python3.5/imp.py", line 342, in load_dynamic
    return _load(spec)
  File "<frozen importlib._bootstrap>", line 693, in _load
  File "<frozen importlib._bootstrap>", line 666, in _load_unlocked
  File "<frozen importlib._bootstrap>", line 577, in module_from_spec
  File "<frozen importlib._bootstrap_external>", line 914, in create_module
  File "<frozen importlib._bootstrap>", line 222, in _call_with_frames_removed
ImportError: /home/pi/.local/lib/python3.5/site-packages/tensorflow/contrib/lite/python/interpreter_wrapper/_tensorflow_wrap_interpreter_wrapper.so: undefined symbol: _ZN6tflite12tensor_utils39NeonMatrixBatchVectorMultiplyAccumulateEPKfiiS2_iPfi
```
##### Solution
```shell
$ fail
```
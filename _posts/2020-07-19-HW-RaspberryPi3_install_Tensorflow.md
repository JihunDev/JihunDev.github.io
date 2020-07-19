---
layout: post
title: RaspberryPi 3B+에 TensorFlow 설치
tags: TensorFlow RaspberryPi
comments: true
---

RaspberrPi에서 TensorFlow 사용해야하는 상황이 발생하여 정리

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
# Object Detection Practice

- Object Detection API를 통해서 Custom Dataset을 이용한 Object Detection을 해보자!

1. 아래 네가지를 다운로드 받는다.
``` bash
pip install pillow
pip install lxml
pip install jupyter
pip install matplotlib
```
2. models/research/에서 해당 명령어를 타이핑한다.
```
protoc object_detection/protos/*.proto --python_out=.
export PYTHONPATH=$PYTHONPATH:`pwd`:`pwd`/slim
```


### Reference

- https://pythonprogramming.net/introduction-use-tensorflow-object-detection-api-tutorial/

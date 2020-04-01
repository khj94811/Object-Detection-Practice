# Object Detection Practice

- Object Detection API를 통해서 Custom Dataset을 이용한 Object Detection을 해보자!

1. 아래 명령어를 수행하자.
``` bash
pip install pillow
pip install lxml
pip install jupyter
pip install matplotlib
```
2. models/research/에서 해당 명령어 수행
```
protoc object_detection/protos/*.proto --python_out=.
export PYTHONPATH=$PYTHONPATH:`pwd`:`pwd`/slim
```
3. OpenCV를 이용하여 Video를 Frame단위로 끊어준다.

4. LabelImg를 이용하여 각 frame에 bounding box를 만들어주자.

  - LabelImg는 아래 repo에서 clone 받을 수 있다.
    - https://github.com/tzutalin/labelImg
  
  - 직접 Labeling을 하면 시간이 많이 걸릴 수 있기 때문에, 좋은 모델을 이용하여 Bounding Box를 Automatic하게 그려줄 수 있다.
    - 나는 pretrained된 VGG16-SSD Model을 사용했다.
    - 결과는 썩 좋지는 않았다.
    - Model을 fine-tuning해서 써야할 것 같다.


### Reference

- https://pythonprogramming.net/introduction-use-tensorflow-object-detection-api-tutorial/

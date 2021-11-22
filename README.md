# 2021VRDL_HW2

## Environment
```
Ubuntu 16.04.5 LTS (GNU/Linux 4.15.0-39-generic x86_64)
```

## Requirements

To install requirements:
```
pip install -r requirements.txt
pip install -U PyYAML
```

Furthermore, please install Mish-Cuda as following:
```
pip install git+https://github.com/JunnYu/mish-cuda.git
```

## Training

To train the model(s) in the paper, run this command:
```
python train.py --device 0 --batch-size 32 --img 640 640 --data hw2.yaml --cfg cfg/hw2.cfg --weights 'hw2.weights' --name hw2 --epoch 30 
```

## Testing

To evaluate my model on ImageNet, run:
```
python test.py -img 640 --conf 0.001 --batch 8 --device 0 --data coco.yaml --cfg cfg/yolov4-pacsp.cfg --weights weights/weight.pt
```

## Weight for Training Model

You can download the file here:

- [The file of weight](https://drive.google.com/file/d/1EhhSuLb4FHcRADGh7Fi_ute492mAQavk/view?usp=sharing)

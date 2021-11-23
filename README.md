# 2021VRDL_HW2-Object Detector on SVHN Datasets

This project is part of a series of projects for the course Selected Topics in Visual Recognition using Deep Learning. This Repository gathers the code for digit object detector.

## Environment
```
Ubuntu 16.04.5 LTS (GNU/Linux 4.15.0-39-generic x86_64)
Google Colab (For Speech benchmark)
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

To train the model in the paper, run this command:
```
python train.py --device 0 --batch-size 32 --img 640 640 --data hw2.yaml --cfg cfg/hw2.cfg --weights 'hw2.weights' --name hw2 --epoch 30 
```

## Testing & Speed Benchmark

To evaluate my model on YOLOv4 and get the speed benchmark, run:
```
python testing.py --img 640 --conf 0.05 --batch 32 --device 0 --data hw2.yaml --cfg cfg/hw2.cfg --weights weights/weight.pt --iou-thres 0.4  --task test --names data/hw2.names --save-json
```

Please refer to [inference.ipynb](https://github.com/PeiHuaWu/2021VRDL_HW2/blob/main/inference.ipynb). And to get the testing data, you need the authorization code, which is provided in my report.pdf.

## Weight for Training Model

You can download the file here:

- [The file of weight](https://drive.google.com/file/d/1dZdWxhHfwOKiUvjTGz1nA1JIVhhIULB6/view?usp=sharing)

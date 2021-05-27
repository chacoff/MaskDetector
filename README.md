# A mask detector using YOLOV5

The original repository of yolov5 from ultralytics: https://github.com/ultralytics/yolov5

**Conda enviroment**
```
conda activate <env>
conda install pip
pip freeze > requirements.txt
```
**PIP enviroment**
```
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
```

**git**
```
$ git clone https://github.com/chacoff/MaskDetector
```


**Train**
```
$ train.py 
```
or
```
$ python train.py --img 640 --batch 16 --epochs 21 --data dataset/vott-csv-export/mask.yaml --weights yolov5x.pt --nosave --cache
```

**Results**

<image src='https://github.com/chacoff/MaskDetector/blob/main/data/images/covid_test8.jpg' width='420'>

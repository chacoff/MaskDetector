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

**dataset**
you will have to uncompress everything from the dataset folder/, you will have there about 8 compressed files which corresponds to the images and another compressed file corresonding the annotations already in darknet format. I am including as well the annotations in a VoTT CSV format which you could use to convert into darknet format with a toold you can find among my other repositories.


**training**
```
$ train.py 
```
or
```
$ python train.py --img 640 --batch 16 --epochs 21 --data dataset/vott-csv-export/mask.yaml --weights yolov5x.pt --nosave --cache
```

**Results**

<image src='https://github.com/chacoff/MaskDetector/blob/main/data/images/covid_test8.jpg' width='420'>

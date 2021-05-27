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

you will have to uncompress everything from the *dataset/* folder. You will find there about 8 compressed files which correspond to the images and another compressed file corresponding the annotations already in darknet format. 

I am including as well the annotations in a VoTT CSV format which you could use to convert into darknet format with a tool you can find among my other repositories: https://github.com/chacoff/VoTT-CSV-to-Darknet-Format


**training**

*mask.yaml*, you will find it in *dataset/vott-csv-export/*. It is pointing to *validation.txt* and *training.txt*, pay attention on the address to the images, it will be different on your computer, i guess, the easiest is using notepad++ and replacing my address with yours, or, use my convertion from CSV to darknet, but you will need to do some configurations in there anyway.

```
$ train.py 
```
or
```
$ python train.py --img 640 --batch 16 --epochs 21 --data dataset/vott-csv-export/mask.yaml --weights yolov5x.pt --nosave --cache
```

**training results**

<image src='https://github.com/chacoff/MaskDetector/blob/main/data/images/results.png' width='720'>
  
**tests**

<image src='https://github.com/chacoff/MaskDetector/blob/main/data/images/covid_test8.jpg' width='420'>
  

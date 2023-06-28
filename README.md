# Road Segmentation with YOLOP

## Clone current repo

If already cloned it before then simply `git pull` inside the `smpc` repo to update the branches

#### To clone only the road segmentation part
```
git clone https://github.com/reachpranjal/smpc.git -b roadseg --single-branch
```

## Clone YOLOP
```
cd smpc && git checkout roadseg
git clone https://github.com/hustvl/YOLOP.git
```

## Move the inference file inside YOLOP
```
mv inference.py YOLOP/tools/
```

To print `fps` on the image/video frames, uncomment line 142 & 143 in the `inference.py` 

## Run Inference

```
cd YOLOP
```

#### Image
- For image input 
Store the test image inside `YOLOP/inference/images/` 
```
python tools/inference.py --source inference/images/<img_name>.jpg
```
#### Video

- For video input 
Store the test video inside `YOLOP/inference/videos/` 
```
python tools/inference.py --source inference/videos/<vid_name>.mp4
```

#### Camera

- For Camera input

If there are any camera connected to your computer, you can set the source as the camera number(The default is 0).

```
python tools/inference.py --source 0
```
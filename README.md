# rv1126_deploy_yolov5

## export out .onnx model
```
python export.py --weights ./runs/train/exp/weights/best.pt --img 640 --batch 1 --include onnx --opset 12
```

## detect .pt model
```
python detect.py --weights runs/train/exp/weights/best.pt --img 640 --conf 0.25 --source runs/train/exp/test_img --data data/my.yaml
```

## detect .onnx model
```
python detect.py --weights runs/train/exp/weights/best.onnx --img 640 --conf 0.25 --source runs/train/exp/test_img --data data/my.yaml --dnn
```

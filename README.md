## Environment

For installation of the project dependencies, please run:
```
pip install -r requirements.txt
``` 

## Dataset
### Human3.6M
#### Preprocessing
1. We follow the previous state-of-the-art method [MotionBERT](https://github.com/Walter0807/MotionBERT/blob/main/docs/pose3d.md) for dataset setup. Download the [MotionBERT](https://github.com/Walter0807/MotionBERT/blob/main/docs/pose3d.md)'s preprocessed H3.6M data [here](https://1drv.ms/u/s!AvAdh0LSjEOlgU7BuUZcyafu8kzc?e=vobkjZ) and unzip it to 'data/motion3d'.
2. Slice the motion clips by running the following python code in `data/preprocess` directory:

**For our model with T = 243**:
```text
python h36m.py  --n-frames 243
```

## Training
After dataset preparation, you can train the model as follows:
### Human3.6M
You can train Human3.6M with the following command:
```
python train.py --config <PATH-TO-CONFIG>
```
where config files are located at `configs/h36m`. 
```
python train.py --config configs/h36m/TCPFormer_h36m_243.yaml 
```

## Acknowledgement

Our code is extended from the following repository. We thank the authors for releasing the codes. 

- [TCPFormer](https://github.com/AsukaCamellia/TCPFormer/tree/main)
- [S4](https://github.com/state-spaces/s4)

## Licence
This project is licensed under the terms of the MIT license.




# HR-Depth: High Resolution Self-Supervised Monocular Depth Estimation
This repository contains an executable demonstration of ONNX and TensorFlow implementation for depth estimation using the model proposed in:
> HR-Depth: High Resolution Self-Supervised Monocular Depth Estimation
> Xiaoyang Lyu, Liang Liu, Mengmeng Wang, Xin Kong, Lina Liu, Yong Liu*, Xinxin Chen and Yi Yuan

[official implementation repository](https://github.com/shawLyu/HR-Depth)
## 1. Requirements Installation
Inside the directory containing the cloned repo, install the necessary packages in [requirements.txt](https://github.com/AbdullahMu/158_HR-Depth/blob/new_branch/requirements.txt)

```bash
pip install -r requirements.txt
```
## 2. Downloading Trained Models
All of the trained models can be downloaded by running the following three lines of code in terminal: 
```bash
for f in *.sh; do
  bash "$f" 
done
```
Alternatively, only the shell script of the eponymous model of interest can be executed.


![High Resolution Self-Supervised Monocular Depth Estimation Demo Output](Screenshot_2022-05-15_12-59-53.png)

## 3.A.  HR-Depth with ONNX Runtime in Python
To prepare the downloaded ONNX models, execute the following command:
```bash
python onnx_merge.py
```
the following output should be printed to console upon successful execution
```bash
graph1 outputs: ['317a', '852a', '870a', '897a', '836a']
graph2 inputs: ['0b', 'input.1b', 'input.13b', 'input.25b', 'input.37b']
Constructing the io_match list from your input and output
```
To run a demo of the HR-Depth with ONNX, execute the following command:
```bash
python demo/demo_hr_depth_onnx.py
```

## 3.B.  HR-Depth with TensorFlow Lite in Python
To run a demo of the HR-Depth with TensorFlow, execute the following command:
```bash
python demo_hr_depth_tflite.py
```

> Written with [StackEdit](https://stackedit.io/).

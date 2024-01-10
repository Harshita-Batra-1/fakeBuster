# FakeBuster: A DeepFakes Detection Tool for Video Conferencing Scenarios

This repository contains the source code for the paper- [FakeBuster: A DeepFakes Detection Tool for Video Conferencing Scenarios](https://dl.acm.org/doi/10.1145/3397482.3450726)

This paper proposes FakeBuster, a novel DeepFake detector for (a) detecting impostors during video conferencing, and (b) manipulated faces on social media. FakeBuster is a standalone deep learning- based solution, which enables a user to detect if another person’s video is manipulated or spoofed during a video conference-based meeting. This tool is independent of video conferencing solutions and has been tested with Zoom and Skype applications. It employs a 3D convolutional neural network for predicting video fakeness. The network is trained on a combination of datasets such as Deeperforensics, DFDC, VoxCeleb, and deepfake videos created using locally captured images (specific to video conferencing scenarios). Diversity in the training data makes FakeBuster robust to multiple environments and facial manipulations, thereby making it generalizable and ecologically valid.


# Installation
```
pip install pyqt joblib pyqtgraph matplotlib
pip install opencv-python mss
pip install --no-cache-dir torch==1.5.0+cu101 torchvision==0.6.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html
pip install torch==1.5.0+cpu torchvision==0.6.0+cpu -f https://download.pytorch.org/whl/torch_stable.html
python main.py
```
# Run
This tool requires model weights for face detector and deepfake detector which can be downloaded from the [drive link](https://drive.google.com/drive/folders/1Vej_l-g6wvwaaAcigxuf4l8-IHxNWk75?usp=sharing)  \
Configure parameters in `config.py`
1. Update the path parameters `checkpointpath` and `weights_path`.
2. Configure model device placement- `fake_det_device` and `fake_det_device`

Run command:-
```
python main.py
```

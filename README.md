# Project Page for NIPS 2018 Submission

Paper ID: 4

Paper Title: **Tracking by Animation: Unsupervised Learning of Multi-Object Attentive Trackers**

The latest version of our paper is available [**HERE**](https://github.com/anonymous-projects/tracking-by-animation).




## 1. Requirements
- Python 3.6
- PyTorch 0.3.1



## 2. Usage

```
cd path/to/tba        # first enter the project root directory
```


### 2.1 Generate data


```
python scripts/gen_mnist.py         # for MNIST-MOT

python scripts/gen_sprite.py        # for Sprites-MOT

python scripts/gen_duke.py          # for DukeMTMC
```


### 2.2 Train the model

```
python run.py --task mnist        # choose a task from mnist/sprite/duke
```


### 2.3 Show training curves

```
python scripts/show_curve.py --task mnist        # choose a task from mnist/sprite/duke
```



### 2.4 Evaluate the tracking performance





## 3. Results


### 3.1 MNIST-MOT


### 3.2 Sprites-MOT


### 3.3 DukeMTMC


### 3.4 Visualizing and understanding the RAT


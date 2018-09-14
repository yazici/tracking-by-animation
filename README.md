# Project Page for AAAI 2019 Submission 
# Paper ID: 792


## 1. Requirements
- python 3.6
- pytorch 0.3.1
- [py-motmetrics](https://github.com/cheind/py-motmetrics) (to evaluate tracking performances)



## 2. Usage


### 2.1 Generate training data

```
cd path/to/tba                  # enter the project root directory
python scripts/gen_mnist.py     # for mnist
python scripts/gen_sprite.py    # for sprite
python scripts/gen_duke.py      # for duke
```


### 2.2 Train the model


```
python run.py --task mnist     # for mnist
python run.py --task sprite    # for sprite
python run.py --task duke      # for duke
```


### 2.3 Show training curves


```
python scripts/show_curve.py --task mnist     # for mnist
python scripts/show_curve.py --task sprite    # for sprite
python scripts/show_curve.py --task duke      # for duke
```


### 2.4 Evaluate tracking performances

#### a) Generate test data
```
python scripts/gen_mnist.py --metric 1         # for mnist
python scripts/gen_sprite.py --metric 1        # for sprite
python scripts/gen_duke.py --metric 1 --c 1    # for duke, please run over all cameras by setting c = 1, 2, ..., 8
```

#### b) Generate tracking results
```
python run.py --init sp_latest.pt --metric 1 --task mnist                     # for mnist
python run.py --init sp_latest.pt --metric 1 --task sprite                    # for sprite
python run.py --init sp_latest.pt --metric 1 --task duke --subtask camera1    # for duke, please run all subtasks from camera1 to camera8
```

#### c) Convert the results into `.txt`
```
python scripts/get_metric_txt.py --task mnist                     # for mnist
python scripts/get_metric_txt.py --task sprite                    # for sprite
python scripts/get_metric_txt.py --task duke --subtask camera1    # for duke, please run all subtasks from camera1 to camera8
```

#### d) Evaluate tracking performances
```
python -m motmetrics.apps.eval_motchallenge data/mnist/pt result/mnist/tba/default/metric --solver lap      # form mnist
python -m motmetrics.apps.eval_motchallenge data/sprite/pt result/sprite/tba/default/metric --solver lap    # form sprite
```

To evaluate duke, please upload the file `duke.txt` (under `result/duke/tba/default/metric/`) to https://motchallenge.net.




## 3. Results (video results will be available soon)


### 3.1 MNIST-MOT


### 3.2 Sprites-MOT


### 3.3 DukeMTMC


### 3.4 Visualizing the RAT


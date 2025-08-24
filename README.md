

## Installation

Install system requirements:
```
sudo apt-get install python3-dev python3-pip python3-tk libglib2.0-0
```

Install python dependencies:
```
pip3 install -r requirements.txt
```

## Run Evaluation on WFLW dataset
1. Download and process WFLW dataset
    * Download WFLW dataset and annotation from [Here](https://wywu.github.io/projects/LAB/WFLW.html).
    * Unzip WFLW dataset and annotations and move files into ```./dataset``` directory. Your directory should look like this:
        ```
        AdaptiveWingLoss
        └───dataset
           │
           └───WFLW_annotations
           │   └───list_98pt_rect_attr_train_test
           │   │
           │   └───list_98pt_test
           │
           └───WFLW_images
               └───0--Parade
               │
               └───...
        ```
    * Inside ```./dataset``` directory, run:
        ```
        python convert_WFLW.py
        ```
        A new directory ```./dataset/WFLW_test``` should be generated with 2500 processed testing images and corresponding landmarks.

2. Download pretrained model from [Google Drive](https://drive.google.com/file/d/1HZaSjLoorQ4QCEx7PRTxOmg0bBPYSqhH/view?usp=sharing) and put it in ```./ckpt``` directory.

3. Within ```./Scripts``` directory, run following command:
    ```
    sh eval_wflw.sh
    ```
    


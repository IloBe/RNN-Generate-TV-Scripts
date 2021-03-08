# RNN: Generate TV Scripts
## Introduction
Welcome to this **RNN project** of the Udacity Deep Learning course. We generate an original TV script by using a recurrent neural network which has been trained on existing Seinfeld TV scripts. In other words, we are using a dataset of scripts about this US sitcom for model learning. 

Have in mind, that for creating a fake script the project iterates over a large amount of data, and it takes a number of hours to train, even on GPU. Therefore, to manage the GPU workspace time given for this project, we build and test the RNN model (including data pre-processing, defining model architecture, etc.) in CPU mode by creating and activating its own new environment, then GPU mode to accelerate training is activated.

## RNN Architecture
For our NLP task we are using a RNN architecture including as hidden layer components **Long Short-Term Memory (LSTM)** cells with their gates. The following FloydHub [blog](https://blog.floydhub.com/long-short-term-memory-from-zero-to-hero-with-pytorch/) delivers a very good introduction to this RNN variant network. With help of LSTM gates contextual information from earlier states are still available. They react as a kind of filter to store relevant information if the model is trained appropriately.

At the end of blog the author mentioned as well, that LSTM architectures have been state-of-the-art for NLP tasks for a long time, but now <i>Attention</i>-based models or <i>Transformers</i> are delivering better results.

## Project
1. To get the basic files clone the following repository and put the files to your local repository:<br>
`git clone https://github.com/udacity/deep-learning-v2-pytorch.git`

This way you can stay up to date with any changes we make by pulling the changes to your local repository with git pull.

Additionally, a workspace utility [file](https://s3.amazonaws.com/video.udacity-data.com/topher/2018/May/5b0dea96_workspace-utils/workspace-utils.py) is added, to make sure that the remote GPU connection during model training is stable. This file is not part of the Udacity repository, it has to be added manually from the mentioned link.

2. **If you are running the project on your local machine (and not using e.g. AWS services)** create and activate a new environment. First, move to directory `path/to/RNN_TV-Scripts-project`. Have in mind that it will take days to train this model on 'normal' CPU hardware.
  - __Windows__
  ```
	conda create --name RNN_TV-Scripts-project python=3
	activate RNN_TV-Scripts-project
	pip install -r requirements/requirements.txt
  ```
  
3. **If you are running the project on your local machine (and not using e.g. AWS services)**, create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `RNN_TV-Scripts-project` environment. 
```
python -m ipykernel install --user --name RNN_TV-Scripts-project --display-name "RNN_TV-Scripts-project"
```

4. Open the notebook.
```
jupyter notebook dlnd_tv_script_generation.ipynb
```

5. **If you are running the project on your local machine (and not using AWS)**, before running code, change the kernel to match the project environment by using the drop-down menu (**Kernel > Change kernel > RNN_TV-Scripts-project**).

## License
This project coding is released under the MIT license.

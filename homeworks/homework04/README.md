In this homework your goal is to build the QA system for Russian language using the [SberQuAD dataset](https://arxiv.org/pdf/1912.09723.pdf). The preprocessing code and baseline solution (BiDAF) are the slightly adapted version of the [Stanford CS224n Starter code](https://github.com/chrischute/squad).

The starting point of this assighnment is the `SberQuAD_preprocessing_and_problem_statement.ipynb` notebook.
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/neychev/made_nlp_course/blob/master/homeworks/homework04/SberQuAD_preprocessing_and_problem_statement.ipynb)


You may choose either this assignment or the `homework05` on the Image Captioning. Or do both ;) 

Next comes the original instructions from the https://github.com/chrischute/squad repository.



### Setup

1. Make sure you have [Miniconda](https://docs.conda.io/en/latest/miniconda.html) installed
    1. Conda is a package manager that sandboxes your project’s dependencies in a virtual environment
    2. Miniconda contains Conda and its dependencies with no extra packages by default (as opposed to Anaconda, which installs some extra packages)

2. cd into src, run `conda env create -f environment.yml`
    1. This creates a Conda environment called `squad`

3. Run `source activate squad`
    1. This activates the `squad` environment
    2. Do this each time you want to write/test your code
  
4. Run `python setup.py`
    1. This downloads SQuAD 2.0 training and dev sets, as well as the GloVe 300-dimensional word vectors (840B)
    2. This also pre-processes the dataset for efficient data loading
    3. For a MacBook Pro on the Stanford network, `setup.py` takes around 30 minutes total  

5. Browse the code in `train.py`
    1. The `train.py` script is the entry point for training a model. It reads command-line arguments, loads the SQuAD dataset, and trains a model.
    2. You may find it helpful to browse the arguments provided by the starter code. Either look directly at the `parser.add_argument` lines in the source code, or run `python train.py -h`.
# Learning from Positive and Unlabeled Data with Arbitrary Positive Shift

[![docs](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/AnonNeurIPS20/arbitrary_pu/blob/master/LICENSE)

**Status**: Under submission at NeurIPS 2020 (#460)  
**Authors**: Anonymous

This repository contains the source code associated with NeurIPS submission #460 entitled "Learning from Positive and Unlabeled Data with Arbitrary Positive Shift"

## Running the Program

To run the program, enter the `src` directory and call:

`python driver.py ConfigFile`

where `ConfigFile` is one of the `yaml` configuration files in folder `src/configs`. If CUDA is installed on your system, the program enables CUDA execution automatically.

### First Time Running the Program

The first time the program is run, it will download any necessary dataset and create any transfer learning representations automatically.  Please note that this process can be time consuming --- in particular for 20 Newsgroups where creating the ELMo-based embeddings can take several hours.

These downloaded files are stored in a folder `.data` that is in the same directory as `driver.py`.

### Results

Results are printed to the console. The tool also creates a folder named `res` in the same directory as `driver.py` where it exports results in CSV (comma separated value) format.

### Requirements

Our implementation was tested in Python 3.6.5.  Minimum testing was performed with 3.7.1 but `requirements.txt` may need to change depending on your local Python configuration.  It uses the [PyTorch](https://pytorch.org/) neural network framework, version 1.3.1 and 1.4.  For the full requirements, see `requirements.txt` in the `src` directory.

We recommend running our program in a [virtual environment](https://docs.python.org/3/tutorial/venv.html).  Once your virtual environment is created and *active*, run the following in the `src` directory:

```
pip install --user --upgrade pip
pip install -r requirements.txt
```

### License

[MIT](https://github.com/AnonNeurIPS20/arbitrary_pu/blob/master/LICENSE).

### Acknowledgements

This repository includes an implementation of PUc that was provided by the tool's author Tomoya Sakai.

# Environment set up

### Miniconda ###

Within this course we will be using Python 3 along with a few open-source libraries (packages). First follow the instructions for **Installing Miniconda** from the [MLP course Environment set up 
notes](https://github.com/sinziana91/mlpractical/blob/mlp2017-8/master/notes/environment-set-up.md). If you already have Miniconda installed you can move to the next section.

### Conda environment ###

Create the Conda environment for the DME labs with:

```bash
conda create -n dme python=3
```

Type `y` when presented with the package plan. Every time you start working on the lab exercises you have to activate your environment with:

```bash
source activate dme
```

omitting "source" for a Windows installation. To deactivate the environment do: `source deactivate dme` (or ` deactivate dme` for Windows).

We will now install the required packages:

```bash
conda install jupyter numpy scipy matplotlib pandas statsmodels scikit-learn seaborn
conda install -c conda-forge scikit-optimize
pip install git+git://github.com/sinziana91/pca-magic.git@master
```


### Course material ###

Once you have finished installed everything, you should download the course material. You have two options:
  1. We recommend that you directly download a .zip file from https://github.com/sinziana91/DME/ which will contain everything you need and save it in the folder you have just created. You can do this from the terminal by typing:
  
    wget https://github.com/sinziana91/DME/archive/master.zip
    unzip master.zip
    
  2. If **and only if** you are familiar and confident with using Git/GitHub, you can initialise a git directory, add the above repo as remote and pull everything into your local directory. Please use this option only if you really know what you are doing. Unfortunately, we won't be able to provide you with Git/Github support if you run into issues with syncing and using version control in general.

Open a terminal (or Command Prompt in Windows), navigate to the folder where you have downloaded the course material and type:

  ```bash
  jupyter notebook
  ```

Then click on `01_Lab_1_Visualisation.ipynb` to open it.

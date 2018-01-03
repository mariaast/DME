# Environment set-up


## Setting up for DICE

Within this course we will be using Python along with a few open-source libraries (packages). These packages cannot be installed directly, so we will have to create a virtual environment. We are using virtual environments to make the installation of packages and retention of correct versions as simple as possible. You can read [here](https://virtualenv.pypa.io/en/stable/) if you want to learn about virtual environments, but this is **not** necessary.

Now open a terminal and follow these instructions. We are expecting you to enter these commands in **one-by-one**. Waiting for each command to complete will help catch any unexpected warnings and errors. Please read heed any warnings and errors you may encounter. We are on standby in the labs to help if required.

1. Change directory to home and create a virtual environment:
  ```bash
  cd
  virtualenv --distribute virtualenvs/dme_env # Creates a virtual environment
  ```

2. Navigate to and activate the virtual environment (you will need to activate the virtual environment every time you open a new terminal - this adds the correct python version with all installed packages to your system's `$PATH` environment variable):
  ```bash
  cd virtualenvs/dme_env
  source ./bin/activate  # Activates the environment, your shell prompt should now change to reflect you are in the `dme_env` environment
  ```

3. Install all the python packages we need (once the correct virtual environment is activated, pip install will install packages to the virtual environment - if you're ever unsure which python you are using, type `which python` in the terminal) **WATCH FOR WARNINGS AND ERRORS HERE**. We have split these commands up to encourage you to enter them one-by-one:
  ```bash
  pip install -U setuptools  # The -U flag upgrades the current version
  pip install -U pip
  pip install yolk
  pip install jupyter
  pip install numpy
  pip install scipy
  pip install matplotlib
  pip install pandas
  pip install statsmodels
  pip install scikit-learn
  pip install scikit-optimize
  pip install seaborn
  ```
4. You should now have all the required modules installed. Our next step is to make a new directory where we will keep all the lab notebooks, datasets and assignments. Within your terminal:
  ```bash
  
  cd # Navigate back to your home directory
  
  mkdir dme_2016 # Make a new directory and enter it
  
  cd dme_2016
  ```
5. Now you have two options:
  1. We recommend that you directly download a .zip file from https://github.com/agamemnonc/dme which will contain everything you need and save it in the folder you have just created. You can do this from the terminal by typing:
    ```bash
    
    wget https://github.com/agamemnonc/dme/archive/master.zip
    
    unzip master.zip
    ```
  2. If **and only if** you are familiar and confident with using Git/GitHub, you can initialise a git directory, add the above repo as remote and pull everything into your local directory. Please use this option only if you really know what you are doing. Unfortunately, we won't be able to provide you with Git/Github support if you run into issues with syncing and using version control in general.

6. Once you have downloaded the material, you are now ready to start working in the Jupyter environment. First you need to activate the `dme_env` environment and start a Jupyter Notebook session from within the folder where the material is stored. **Note that you will have to follow this procedure for all labs.**
  1. Navigate home and ensure the `dme_env` virtualenv is activated:
    ```bash
    
    cd
    
    source virtualenvs/dme_env/bin/activate # Activates the environment
    ```
  2. Enter the directory you downloaded the course material:
    ```bash
    
    cd dme_2016/iaml-master
    ```
  3. Start a jupyter notebook:
    ```bash
    
    jupyter notebook
    ```
  4. This should automatically open your browser. Click on `01_Lab_1_Visualisation.ipynb` to open it

## Setting up for personal machine (Windows / OS X / Ubuntu)

1. If you are using a personal machine, you can choose whether to do as above or use the Anaconda distribution (Python version 2.7, choose the appropriate installer according to your operating system). Anaconda is a standard set of packages used in scientific computing which the Anaconda team curate to keep them consistent.

2. Once the installation is complete, we need to install the `seaborn` and `skopt` packages which are not included in the distribution. It's also recommended that you set up a conda environment for this project. This way, if you update anything in your anaconda base install, this environment will remain unchanged. To create a conda (virtual) environment called `dme_env`, open a Terminal (or Command Prompt window if you are running Windows) and type:

  ```bash
  conda create -n dme_env python=2.7 numpy scipy matplotlib pandas jupyter scikit-learn=0.18.1 seaborn=0.7.0
  ```

3. Activate the conda environment (don't forget to repeat this step every time you begin work from a new terminal):

  ```bash
  source activate dme_env
  ```
4. To recover disk space we can clear the package tarballs Conda just downloaded:

  ```bash
  conda clean -t
  ```

5. We also need to install `skopt` (make sure you have already activated the `dme_env` as outlined above):

  ```bash
  pip install scikit-optimize
  ```

6. Once you have finished installed everything, you should download the course material. You have two options:
  1. We recommend that you directly download a .zip file from https://github.com/agamemnonc/dme which will contain everything you need and save it in the folder you have just created. You can do this from the terminal by typing:
    ```bash
    wget https://github.com/agamemnonc/dme/archive/master.zip
    unzip master.zip
    ```
  2. If **and only if** you are familiar and confident with using Git/GitHub, you can initialise a git directory, add the above repo as remote and pull everything into your local directory. Please use this option only if you really know what you are doing. Unfortunately, we won't be able to provide you with Git/Github support if you run into issues with syncing and using version control in general.

7. Open a terminal (or Command Prompt in Windows), navigate to the folder where you have downloaded the course material and type:

  ```bash
  jupyter notebook
  ```

8. Then click on `01_Lab_1_Visualisation.ipynb` to open it.

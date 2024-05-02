# Installation instructions

# WiFi access for Cefas staff
If your laptop is configured to use the eduroam academic network this will be available across campus. Alternatively [register to Sky's free WiFi The Cloud](https://account.thecloud.eu/spportal/).

# Laptop Installation
For this course you will need to have Python installed on your laptop, including some extra packages. Follow the instructions below to set up your Python environment. Make sure you do this do this **before** the course, including running the test as below. There will be a troubleshooting session on the first day at 8:30 as advertised in the invite email.

As an alternative you can use cloud hosting by [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ueapy/pythoncourse2023-materials/main?urlpath=lab) to run all the lessons with the data here contained (it is not possible to load your own data), but any changes made won't be saved.

Feel free to contact [Jenny at Cefas](mailto:jennifer.graham@cefas.co.uk) or [Eliza at UEA](mailto:e.karlowska@uea.ac.uk) if you have any problems with the installation (but better do an internet search first!)
Note: The course is designed in Python 3.9 but even if you have a different version installed, 3.9 will be installed when creating a conda environment in step 3 below.

## 1. Install Python distribution

### Cefas Users
You will neet to request in advance a temporary administrator password to make the installation. 

As a government organisation we do not have free access to Anaconda, so please use the free alternative mambaforge. For those in academia, we also recommend this as a more lightweight (and often faster) python installation option!  

1.1.a [Download Mambaforge for your OS](https://github.com/conda-forge/miniforge#mambaforge) 

1.2.a After downloading, follow the instructions as suggested [here](https://github.com/conda-forge/miniforge#install)

### Students or UEA Staff
1.1.b. [Download Anaconda with Python 3 for your OS](https://www.anaconda.com/download/). 

1.2.b. Install it following [these instructions](https://docs.anaconda.com/anaconda/install/). Be sure to select install "just me" when prompted.

### UEA HPC (Ada)
Following the course, there are a number of modules available for use of python on Ada, using either mamba or anaconda. 

However, for the purpose of this course, we recommend viewing the notebooks on your own machine. 

## 2. Download course materials
From the Friday before the course (2nd of June) the material for the workshop can be downloaded as a [zip file](https://github.com/ueapy/pythoncourse2023-materials/archive/main.zip) or can be cloned from our [GitHub repository](https://github.com/ueapy/pythoncourse2023-materials). 


### Option 1: Download ZIP file (easier)
Download the materials as a [zip file](https://github.com/ueapy/pythoncourse2023-materials/archive/main.zip) and unpack it in a suitable directory, for example, in `Downloads` folder. Jump to [3. Create the environment](installation.md#3.-Create-the-environment).

### Option 2: Using Git (allows restoring originals after modifications)
#### 2.1. Install Git
If you don't have git version control system installed, you can install it following these instructions:
##### Linux
Use your package manager. For example, using aptitude you would run the following terminal command: `sudo apt-get install git`
##### Mac
* The XCode command line tools need to be installed.
* Install XCode if it isn’t already. XCode is available in the Mac App Store for free.
* Launch XCode and accept the license agreement.
* Quit XCode.
* Open a new terminal and run the command xcode-select --install
* Select install on the pop-up menu.
##### Windows
Download and install [Git for Windows](https://git-scm.com/downloads).

#### 2.2. Clone the repository
2.2.1. Open the command line (Git bash, terminal or cmd.exe)

2.2.2. (Linux or Mac, optional) Change to a suitable directory (e.g. `cd /home/yourname/Documents`)

2.2.3. Clone the repo by typing

```
git clone https://github.com/ueapy/pythoncourse2023-materials.git
```
This should create a local copy of the course materials in the current directory.

Windows-users, double check that it has been cloned in the directory you wanted.


## 3. Create the environment
3.1. Make sure Anaconda or Mambaforge is installed and the course materials are downloaded

3.2. Open the command line or python prompt (i.e., search "Terminal" on Mac Spotlight Seach; search "Anaconda prompt" or "mamba" on Windows start menu)

3.3. Navigate to folder containing the cloned / downloaded course materials. Use the `cd` command, for example:

```
cd C:\Users\myname\Downloads\pythoncourse2023-materials\
```

3.4. Create the environment using `conda` package manager:

```bash
conda env create -f environment.yml
```
or if you installed mamba
```bash
mamba env create -f environment.yml
```

This will take some time depending on your Internet speed (<15 minutes).


If you get stuck try typing return or, failing this, creating the environment again.

## 4. Activate the environment
### Linux / Mac
If your default shell is NOT bash, first type `bash`. Activate the relevant environment by typing:
```bash
conda activate course2023
```
### Windows
Still in the command line (Anaconda/mamba prompt), type:
```
conda activate course2023
```

## 5. Test the installation (essential!)
From the terminal type:
```
python -c "import seaborn"
```
If you don't get any errors then your installation was sucessful.

## 6. Launch Jupyter
Once the environment is activated, type 
```
jupyter notebook
```
in the command line. This should open Jupyter Notebook in your browser. We will also demonstrate using Jupyterlab, which is ery similar but offer a more flexible interface. For this type

```
jupyter lab
```

## Still having trouble?
If you are unable to install Anaconda Python on your PC, contact the [course organisers](index.md#registration-and-enquiries).
Another option: launch the course in the cloud! [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ueapy/pythoncourse2023-materials/main?urlpath=lab) This requires no installation but progress and modifications won't be saved.

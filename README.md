# Pandas intro workshop

A _learning by doing_ workshop for learning the basics of the Pandas library.

## Prerequisites

The main prerequisite that is needed is Jupyter with NumPy and Pandas installed (Or some other way of using a Jupyter notebook) There are many services that provide notebooks available for free. 
If you do not want to install or run it on your local computer you can follow the entire workshop using one of the following free Jupyter services:

 - [Azure Notebooks](https://notebooks.azure.com/)
 - [Google Colab](https://colab.research.google.com/notebooks/)
 - [Kaggle Notebooks](https://www.kaggle.com/kernels)

You can install Jupyter in multiple ways. For this workshop I recommend one of two ways. By using a docker container, or by using the `Anaconda` distribution.

**NOTE:** If you are using one of the notebook solutions in the cloud, you have to upload the notebook, img folder and data folder to the cloud provider. (Or check it out from git on the cloud providers notebook) This workshop is designed around using docker and a local computer mainly.

### Using Docker
Install docker on your local computer if this is not already installed. You can download docker from here: [Download Docker](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe)

Then pull the latest Jupyter image and start it on your computer. If you use the command line then you can do this by typing the following command: 

Windows:
```
docker run --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v "%cd%":/home/jovyan/work jupyter/datascience-notebook
```

OSX / Linux:

```
docker run --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v "$PWD":/home/jovyan/work jupyter/datascience-notebook
```

A container using the latest `jupyter/datascience-notebook` will then be started and can be stopped by pressing `Ctrl-C` in the console. (Or closing the console) In the console a link is printed that you can use to access the notebook. This link looks like so: `http://127.0.0.1:8888/?token=6519a549112e9191d6485a5360980635442c8ec9e03f4924` where token is different. 

You now have a running Jupyter Notebook instance running as a Docker container and you can work on notebooks using your favorite browser. The notebooks mounts up your current working directory as the folder `work` in Jupyter.


### Using Anaconda.

Anaconda is a Python distribution that contains a lot of packages that often is not present in PiP. You can download an installer and install it locally by [downloading the installer here](https://www.anaconda.com/distribution/#download-section).


## Book

Much of the content in this workshop is based upon a book that is available for free: The [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/) written by Jake VanderPlas is one of the best books for learning Jupyter, NumPy and Pandas. This book is free and available for reading at the previous link. There also exists also a print copy that you can buy from Amazon here: [Python Data Science Handbook](https://www.amazon.com/_/dp/1491912057)

It will not be used directly in the workshop. But if you like to learn by yourself outside of the workshop, then this is a very good book to read.

![Book](https://jakevdp.github.io/PythonDataScienceHandbook/figures/PDSH-cover.png)

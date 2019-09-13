# Setting Up the Environment:
For Python workshops, we will use Python 3.7 on an online Integrated Development Environment (IDE), such as Project Jupyter and/or Google COLAB.
<br/>
## Project Jupyter:
It is an open source web application that allows for creating, sharing documents. Documents can contain different codes, stylistic texts, visualizations.
<br/>
We recommend to use Jupyter applications after installing Anaconda Distribution.
<br/>
- **Steps for Successful Setup:**
1. Download Python 3.7 through Anaconda: https://www.anaconda.com/distribution/
2. Check your OS system type. For Lab PCs, Windows 10, 64-bit OS. This is different for Unix-like OS.
3. Follow installation instructions.
4. Make sure to install Python 3.7 within user space, not as an administrator, this might require extra privileges.
4. To launch in Windows OS, go to search bar, and choose Anaconda Navigator, and choose Jupyter. **OR** you can use Anaconda Prompt Shell, and type `Jupyter Notebook` in root directory or wherever you want to work. For Unix-like OS, type `Jupyter Notebook` in terminal.


## Google Colaboratory:
This is a free jupyter notebook  environment, with no setup at all and runs on a virtual host machine.
<br/>
You can do all Project Jupyter functionalities  for your browser, only requires having a gmail account.
<br/>
- Steps for Successful launch:
1. Sign into your Google account
2. Go to Google COLAB: https://colab.research.google.com/notebooks/welcome.ipynb
3. Choose a new Python 3 file, and save it into your Google Drive.
4. Such step will create a COLAB folder inside your Google Drive.
<br/>

If you want to use an Ipython file saved on your Google Drive; follow these steps:
1. Upload .ipynb file to Google Drive in related folder.
2. Launch the file through COLAB.
3. Before executing  commands, Mount the Drive to working COLAB session, run the following commands for Successful mount:
<br/>

`from google.colab import drive` <br/>
`drive.mount('/content/gdrive')`

<br/>
It will ask you to authenticate your account. By doing so you can import files into your working session.

## Installing Python Packages from a Jupyter Notebook
what is the  difference between `pip` v. `conda`?
  - pip installs python packages in any environment.
  - conda installs any package in conda environments.
Not to be confused, if installed Python using Anaconda, then use `conda` to install Python packages. If `conda` tells you package does not exist, use `pip`.
<br/>

- Running Shell Commands:

The notation `!` can run shell commands from the notebook, still it might be problematic  with complicated packages, since the Shell Environment and Python Executable are disconnected.
<br/>

- For Installation in the current Jupyter Kernel, use: <br/>

`import sys` <br/>

`!conda install --yes --prefix {sys.prefix} <package_name>`
<br/> OR <br/>

`import sys`
<br/>
`!{sys.executable} -m pip install <package_name>`

- For more details:
https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/

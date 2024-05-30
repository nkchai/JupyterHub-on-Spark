# Jupyter Notebook with Spark tutorial

### Login
Follow below steps to access JupyterHub:
1. Connect the school VPN visit https://vpn.iit.edu and download the university VPN (cisco) software (watch out your will have to authenticate via your second factor).
2. Connect to the host `vpn.iit.edu` in the vpn client.
3. You need to be on the VPN to access any resources related to the cluster.

Go to the link `http://192.168.172.72:8000/` and sign in  with your username and password.

!['login page'](./images/login-image.png)

### Creating a Notebook
Once you are logged in, you will see a page like this:

!['jupyter-lab'](./images/jupyter-lab.png)

This is called **Launcher**.The left pane is the File Browser, it is the area where you will see all you files and folders present in your account. You can make use of ***New Folder***, ***Upload Files*** buttons situated right below ***Run Menu***.

Click on python icon under the Notebook section to create a new notebook. This will create a new notebook in the ***current directory***. If you want to create a new notebook in specific directory, navigate to that folder and then click on python icon under notbook section.

### Running programs

Once you have created a notebook, you can run your python programs. You can run a cell by clicking on the play button on the top menu of the notebook as shown below.

!['hello-world'](./images/hello-world.png)

You can access launcher again by clicking on **"+"**.


### Terminal

In the launcher click on ***Terminal*** in the ***other*** section.

![Terminal](./images/terminal.png)

This is like any other linux terminal, you can do everything that your normal profile terminal allows you to do.

The main use of this section in this case is to ***clone and manage GitHub Repo's***. Clone your repository via ssh using `git clone`.

For more information on cloning your repo [click here](https://github.com/illinoistech-itm/jhajek/tree/master/itmd-521/git-tutorial).

### Installing Python libraries

The jupyter notebook generated is like any other jupyter notebook, you can install any extenal libraries with `pip`. Example:

```
pip install pandas
```
**Note:** Only spark jobs will be sent to the spark cluster, any code other than spark will be run on local compute.

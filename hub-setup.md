## Installation

### Check prerequisites

- A Linux/Unix based system
- [Python](https://www.python.org/downloads/) 3.8 or greater
- [nodejs/npm](https://www.npmjs.com/)

  - If you are using **`conda`**, the nodejs and npm dependencies will be installed for
    you by conda.

  - If you are using **`pip`**, install a recent version (at least 12.0) of
    [nodejs/npm](https://docs.npmjs.com/getting-started/installing-node).

- If using the default PAM Authenticator, a [pluggable authentication module (PAM)](https://en.wikipedia.org/wiki/Pluggable_authentication_module).
- TLS certificate and key for HTTPS communication
- Domain name

### Install packages
Use `sudo` to install the packages globally.
#### Using `pip`

JupyterHub can be installed with `pip`, and the proxy with `npm`:

```bash
npm install -g configurable-http-proxy
python3 -m pip install jupyterhub
```

If you plan to run notebook servers locally, you will need to install
[JupyterLab or Jupyter notebook](https://jupyter.readthedocs.io/en/latest/install.html):

    python3 -m pip install --upgrade jupyterlab
    python3 -m pip install --upgrade notebook

### Run the Hub server

Use `sudo` to run the below commands.

To start the Hub server, run the command:

    jupyterhub

Visit `http://localhost:8000` in your browser, and sign in with your system username and password.

To access the hub at a paticular url use `--ip` flag.

```
jupyterhub --ip 192.168.172.26
```

_Note_: To allow multiple users to sign in to the server, you will need to
run the `jupyterhub` command as a _privileged user_, such as root.
The [wiki](https://github.com/jupyterhub/jupyterhub/wiki/Using-sudo-to-run-JupyterHub-without-root-privileges)
describes how to run the server as a _less privileged user_, which requires
more configuration of the system.

## Configuration

The [Getting Started](https://jupyterhub.readthedocs.io/en/latest/tutorial/index.html#getting-started) section of the
documentation explains the common steps in setting up JupyterHub.

The [**JupyterHub tutorial**](https://github.com/jupyterhub/jupyterhub-tutorial)
provides an in-depth video and sample configurations of JupyterHub.

### Create a configuration file

To generate a default config file with settings and descriptions:

    jupyterhub --generate-config


# jupyter

OpenFisca Jupyter notebook Docker container definition and examples


## Usage
This Dockerfile contains the code of OpenFisca-core, OpenFisca-france and all the dependencies. 

Based on the docker jupyter/singleuser, it's used by jupyterhub for work with openfisca in a python2 environnement.


## Description

For download the docker, make the next command : 

```
docker pull openfisca/jupyter

```

After, that you have to :

- Install jupyterhub (https://github.com/jupyter/jupyterhub)

- Install Dockerspawner (https://github.com/jupyter/dockerspawner)

- Install Oauthenticator (https://github.com/jupyter/dockerspawner/tree/master/examples/oauth)
- create the nginx configuration File.

You need to specify variable environment, you can do this with a simply file, called env.

For Finish, create a service file in /etc/systemd/system

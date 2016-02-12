# jupyter

OpenFisca Jupyter notebook Docker container definition and examples

Enables [JupyterHub](https://github.com/jupyter/jupyterhub) to spawn user servers in docker containers
which have [`OpenFisca-Core`](https://github.com/openfisca/openfisca-core) and
[`OpenFisca-France`](https://github.com/openfisca/openfisca-core) pre-installed,
in a `python2` environement.

This container is published on [Docker Hub](https://hub.docker.com/r/openfisca/jupyter/) and
is based on the container [`jupyter/singleuser`](https://hub.docker.com/r/jupyter/singleuser/).

## Usage

To download the container: 

```
docker pull openfisca/jupyter
```

Then you have to:

- install [JupyterHub](https://github.com/jupyter/jupyterhub)
- install [DockerSpawner](https://github.com/jupyter/dockerspawner)
- install [OAuthenticator](https://github.com/jupyter/dockerspawner/tree/master/examples/oauth)
- create the [`nginx` configuration file](config/jupyter.nginx.conf) for your domain by replacing all the `example.com` occurences

You need to define environment variables in [`env`](config/env).

If you are using `systemd`, you can copy the [`systemd` service file](config/jupyterhub.service)
in `/etc/systemd/system` and replace the template values between `<` and `>` by the actual values.

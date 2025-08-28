![Current tag](https://img.shields.io/github/tag/thermistor/docker.svg)

# kamal

An ansible role that preps a server for deploying with [kamal](https://kamal-deploy.org/).

It does the following:
- installs `docker` package
- adds ubuntu user to `docker` group
- manages ssh keys for the ubuntu user

## Usage

    roles:
      - role: thermistor.kamal
        kamal_shortname: sample_app

## Vars

Vars that must be set:

    kamal_shortname: sample_app
    kamal_deployer_keys: []

Vars with defaults (shown) that you can override:

    kamal_env: staging
    kamal_user: ubuntu
    kamal_pkg_dependencies:
      - docker.io
      - curl

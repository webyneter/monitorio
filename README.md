# monitorio

Ansible role deploying a customized version of [vegasbrianc/prometheus](https://github.com/vegasbrianc/prometheus)'s prometheus stack.

## Remote host prerequisites

* Docker (tested with 18.06)
* Docker Compose (tested with 1.22)

## Required role parameters

* `root_dir_path`: path to the root directory for reversario files to reside in on a remote host e.g. `~/apps/`;
* `commit_sha`: SHA1 of the commit to deploy;
* `letsencrypt_email`: email to be used by letsencrypt;
* `grafana_domain`: grafana domain;
* `prometheus_domain`: prometheus domain.

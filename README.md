# monitorio

Ansible role deploying a customized version of [vegasbrianc/prometheus](https://github.com/vegasbrianc/prometheus)'s prometheus stack.

## Remote host prerequisites

* Docker (tested with 18.06)
* Docker Compose (tested with 1.22)

## Required role parameters

* `root_dir_path`: path to the root directory for reversario files to reside in on a remote host e.g. `~/apps/`

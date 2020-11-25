[![CI](https://github.com/marvel-nccr/ansible-role-python/workflows/CI/badge.svg)](https://github.com/marvel-nccr/ansible-role-python/actions)
[![Ansible Role](https://img.shields.io/ansible/role/52015.svg)](https://galaxy.ansible.com/marvel-nccr/python)
[![Release](https://img.shields.io/github/tag/marvel-nccr/ansible-role-python.svg)](https://github.com/marvel-nccr/ansible-role-python/releases)

# Ansible Role: marvel-nccr.python

An Ansible role that installs a specific base python+pip version (`major.minor` only).

The executables will be available at `/usr/bin/python3.7` and `/usr/local/bin/pip3.7`, for the `base_python_version` specified.

The role is tested against: Ubuntu 16.04/18.04/20.04, Fedora 31 and CentOS 8 for python versions `3.6`, `3.7` and `3.8`.

## Installation

`ansible-galaxy install marvel-nccr.python`

## Role Variables

See `defaults/main.yml`

## Example Playbook

```yaml
- hosts: servers
  roles:
  - role: marvel-nccr.python
```

## Development and testing

This role uses [Molecule](https://molecule.readthedocs.io/en/latest/#) and [Docker](https://www.docker.com/) for tests.

After installing [Docker](https://www.docker.com/):

Clone the repository into a package named `marvel-nccr.python` (the folder must be named the same as the Ansible Galaxy name)

```bash
git clone https://github.com/marvel-nccr/ansible-role-python marvel-nccr.python
cd marvel-nccr.python
```

Then run:

```bash
pip install -r requirements.txt  # Installs molecule
molecule test  # runs tests
```

or use tox (see `tox.ini`):

```bash
pip install tox
tox
```

## Code style

Code style is formatted and linted with [pre-commit](https://pre-commit.com/).

```bash
pip install pre-commit
pre-commit run -all
```

## Deployment

Deployment to Ansible Galaxy is automated *via* GitHub Actions.
Simply tag a release `vX.Y.Z` to initiate the CI and release workflow.
Note, the release will only complete if the CI tests pass.

## License

MIT

## Contact

Please direct inquiries regarding Quantum Mobile and associated ansible roles to the [AiiDA mailinglist](http://www.aiida.net/mailing-list/).

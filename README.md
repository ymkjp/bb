bb-base
===

## Requirements
- Vagrant v1.8.x
- Python v2.7.x

```
# Example on OS X with Homebrew
xcode-select --install
brew update && brew install \
  Caskroom/cask/vagrant \
  python
```

## Setup

```
pip install --requirement requirements.txt
ansible-galaxy install --role-file= install_roles.yml
```

## Run VM

```
vagrant up
```

## Provision

```
vagrant provision dev_01
```

[![Latest Stable Version](https://poser.pugx.org/rvanginneken/gitbox/v/stable)](https://packagist.org/packages/rvanginneken/gitbox)
# git-box
A GIT extension which uses the [petervanderdoes/gitflow-avh](https://github.com/petervanderdoes/gitflow-avh) extension to create branches following the box's versioning:

`MAJOR.RELEASE.HOTFIX`

git-box will only bump version if there is no active release/hotfix (local or remote) and the last tag was using our versioning.
Assuming everything else was set up as expected, you end it up with a branch that has been synced to remote.

## Installation
After [installing gitflow-avh](https://github.com/petervanderdoes/gitflow-avh/wiki/Installation), git-box can be installed with composer:  
`$ composer global require rvanginneken/gitbox`

## Usage
Assuming our latest tag was `7.3.1`, the following changes would apply:

* Using `$ git box major` would bump the version to `8.0.0`.
* Using `$ git box release` would bump the version to `7.4.0`.
* Using `$ git box hotfix` would bump the version to `7.3.2`.

---

Created by [Roy Van Ginneken](https://github.com/rvanginneken) & [Martijn Cuppens](https://github.com/MartijnCuppens).

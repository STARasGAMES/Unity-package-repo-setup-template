# Unity package template
This template provides solution on how to create and maintain your package, while allowing it to be distributed through GitHub.
It has CI actions, which creates/updates branch called `upm` after each commit to `main`.
This is very usefull because you can have whole project(with all settings) in repo, but also allow to install only `upm` branch through Package Manager.

Look at [upm](https://github.com/STARasGAMES/Unity-package-repo-setup-template/tree/upm) branch to see how it looks.

## Steps to setup your package repo

* Create new repo using this project as template
* Rename folder "Packages/PACKAGE_NAME" to represent your package name
* Change PACKAGE_NAME in ".github/workflows/ci.yml" to your packages's folder name
* Copy your package name, because you will need to paste it several time
  1. In Unity go to your package folder and select package.json file. Change all appropriate fields.
  2. In Unity go to your package folder and change names for .asmdef files
  3. Change `README.md` and `Packages/PACKAE_NAME/README.md` installation sections accordingly 
  4. Remove from `README.md` unnecessary text 

## Installation
Install via git url by adding this entry in your **manifest.json**

`"$package-name$": "https://github.com/$GitHubUsername$/$RepositoryName$.git#upm"`
# Devpacks repo

This is a repo dedicated to holding plugins for vim v8+ as git submodules.

Should be used with [this repo](https://github.com/uncomplete/devenv) but can be used by itself.

To use:

```
$> git clone --recursive https://github.com/uncomplete/devpacks.git ~/.vim/pack
```

To add a plug-in:

```
$> git submodule init
$> git submodule add <https-git-url> <dir>/<start-or-opt>/<plug-in-name>
$> git add .gitmodules <dir>/<start-or-opt>/<plug-in-name>
$> git commit -m "Added <plug-in-name>
$> git push
```

Update packages:

```
$> git submodule update --remote --merge
$> git commit -m "Updated all"
```

Removing a plug-in:

```
$> git submodule deinit <dir>/<start-or-opt>/<plug-in-name>
$> git rm <dir>/<start-or-opt>/<plug-in-name>
$> rm -Rf .git/modules/<dir>/<start-or-opt>/<plug-in-name>
$> git commit -m "Removed <plug-in-name>"
```
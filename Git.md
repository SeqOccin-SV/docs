
Updating submodules

```
git submodule update --init --recursive
```
see https://stackoverflow.com/questions/1030169/easy-way-to-pull-latest-of-all-git-submodules

**Common issues**

* Head detached

Pour un sous-module:
```
HEAD détachée sur 58c1e9c
```
J'avoue ne pas avoir encore tout compris, mais je pense que l'on s'en sort simplement comme cela.
Dans le répertoire du sous-module
```
git checkout master
```
Nous sommes maintenant bien connecté à la branche principale et il est possible de faire
```
git pull
```
Voir quelques indications ici:

https://www.activestate.com/blog/getting-git-submodule-track-branch

et plus complet (voir par exemple Pulling with submodules)

https://www.vogella.com/tutorials/GitSubmodules/article.html



* Changing file permission issue
```
old mode 100755
new mode 100644
```
   Solution 
  https://stackoverflow.com/questions/1257592/how-do-i-remove-files-saying-old-mode-100755-new-mode-100644-from-unstaged-cha 
```  
git config core.filemode false
```


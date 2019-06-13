
Pulling everything (including submodules)

```
git pull --recurse-submodules
```
see https://stackoverflow.com/questions/1030169/easy-way-to-pull-latest-of-all-git-submodules

Check address of the remote repository (works for submodules)
```
git config --get remote.origin.url
```

**Common issues**

* Head detached

Pour un sous-module:
```
HEAD détachée sur 58c1e9c
```
Pas encore tout compris, mais on s'en sort comme cela.
Dans le répertoire du sous-module
```
git checkout master
```
Nous sommes maintenant bien connecté à la branche principale et on peut travailler normalement.

Voir quelques indications ici:
https://www.activestate.com/blog/getting-git-submodule-track-branch

et plus complet 
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


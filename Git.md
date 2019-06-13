
Pulling everything (including submodules)

```
git pull --recurse-submodules
```
see https://stackoverflow.com/questions/1030169/easy-way-to-pull-latest-of-all-git-submodules

Update a submodule version to latest: https://github.com/tj/git-extras/pull/80

```
cd submodule_name
git checkout master && git pull
cd ..
git add submodule_name
git commit -m "updating submodule to latest"
```
Check address of the remote repository (works for submodules)
```
git config --get remote.origin.url
```
Comprendre le fonctionnement des sous-modules (en particulier HEAD détachée) (suggérant qu'il nous faut peut-être procéder autrement ?)

 https://delicious-insights.com/fr/articles/git-submodules/


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
Nous sommes maintenant bien connecté à la branche principale et on peut travailler normalement.<br /> 
Voir quelques indications ici:
https://www.activestate.com/blog/getting-git-submodule-track-branch <br /> 
et plus complet 
https://www.vogella.com/tutorials/GitSubmodules/article.html


* Changing file permission issue
```
old mode 100755
new mode 100644
```
   Solution 
```  
git config core.filemode false
```
see https://stackoverflow.com/questions/1257592/how-do-i-remove-files-saying-old-mode-100755-new-mode-100644-from-unstaged-cha 
```

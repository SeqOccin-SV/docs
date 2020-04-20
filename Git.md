

Some usefull git functionalities

* [Submodules](#submodules)
* [Branches](#branches)
* [Credentials](#credentials)


### <a id="submodules"></a>Submodules

- Pulling everything (including submodules)

```
git pull --recurse-submodules
```
see https://stackoverflow.com/questions/1030169/easy-way-to-pull-latest-of-all-git-submodules

- Get rid of HEAD detatched: https://stackoverflow.com/questions/6474847/how-do-i-git-clone-recursive-and-checkout-master-on-all-submodules-in-a-single/6475033

```
git submodule foreach --recursive git checkout master
```
- Check address of the remote repository (works for submodules)
```
git config --get remote.origin.url
```
- Change address the submodule remote repository

https://stackoverflow.com/questions/913701/how-to-change-the-remote-repository-for-a-git-submodule

- Tie the submodule to a specific commit or branch

https://twoguysarguing.wordpress.com/2010/11/14/tie-git-submodules-to-a-particular-commit-or-branch/

- Comprendre le fonctionnement des sous-modules (en particulier HEAD détachée) (suggérant qu'il nous faut peut-être procéder autrement ?)

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


### <a id="branches"></a> Branches

Creating a new branch
```
 git checkout -b [name_of_your_new_branch]
```
Push the branch on github : 

```
git push origin [name_of_your_new_branch]
```
see https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches/_edit


### <a id="credentials"></a>Credentials

Turn on the credential helper so that Git will save your password in memory for some time. By default, Git will cache your password for 15 minutes.
```
git config --global credential.helper cache
```
see https://help.github.com/en/github/using-git/caching-your-github-password-in-git




**General Common issues**

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

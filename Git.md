
Updating submodules

```
git submodule update --init --recursive
```

**Common issues**

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



### Creating an environment file environment.yaml

```
conda env export | grep -v "^prefix: " > environment.yml
```

### Updating an environment 

```
conda env update -f path_environment_file.yaml
```

### Removing a package
```
conda remove package
```

### Removing an environment
```
conda remove --name myenv --all
```


[Conda documentation](https://docs.conda.io/projects/conda/en/latest/commands.html)


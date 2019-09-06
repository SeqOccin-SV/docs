
### Creating an environment file environment.yaml

```
conda env export | grep -v "^prefix: " > environment.yaml
```

### Creating an environment from a environment.yaml file

```
conda env create -f environment.yaml
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
conda env remove --name myenv
```


[Conda documentation](https://docs.conda.io/projects/conda/en/latest/commands.html)


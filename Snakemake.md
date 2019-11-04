### Running snakemake on the cluster

```
export DRMAA_LIBRARY_PATH="/tools/libraries/slurm-drmaa/slurm-drmaa-1.0.7/lib/libdrmaa.so" 
snakemake --jobs 30 --cluster-config cluster.yaml --drmaa " --mem-per-cpu={cluster.mem}000 --mincpus={threads} --time={cluster.time} -J {cluster.name} -N 1=1" --configfile config.yaml -n -p
```
- You can of course provide a full path for the cluster config file as well as for the config file

### Best practices snakemake workflows

https://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html

### Best practices snakemake workflows

The snakemake machinery

https://bitbucket.org/snakemake/snakemake/issues/295/keyerror-on-cluster-but-not-locally

https://bitbucket.org/snakemake/snakemake/issues/428/adding-list-and-dictionary-expansion-to

### A short course on Snakemake

# First the presentation
  https://slides.com/johanneskoester/snakemake-tutorial#

# Next the step by step tutorial
  https://snakemake.readthedocs.io/en/stable/tutorial/tutorial.html
  
# The important concepts
  * See slide 37 of the presentation on slides.com
  * the wildcards
  * the input functions
  




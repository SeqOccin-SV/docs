### Launching snakemake on the cluster

```
export DRMAA_LIBRARY_PATH="/tools/libraries/slurm-drmaa/slurm-drmaa-1.0.7/lib/libdrmaa.so" 
snakemake --jobs 30 --cluster-config cluster.yaml --drmaa " --mem-per-cpu={cluster.mem}000 --mincpus={threads} --time={cluster.time} -J {cluster.name} -N 1=1" --configfile config.yaml -n -p
```

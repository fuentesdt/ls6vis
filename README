
## setup remote vis

Following https://docs.tacc.utexas.edu/hpc/lonestar6/#vis-paraview

```
sbatch job.vnc -geometry 1680x1000
while [ 1 ] ; do squeue -u fuentes ; sleep 1 ; done
tail vncserver.out
ssh -f -N -L xxxx:localhost:yyyy ls6.tacc.utexas.edu
module load swr qt5 oneapi_rk paraview
swr -p 1 paraview
```

Notice that the image is distributed across 2 nodes by the vtkProcessId.
Each node is running its own instance of pvserver

![distributed vis](/distpv.png)

### multiple ssh-key

```
ssh-agent bash
ssh-add /path/to/id_rsa
```

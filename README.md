# MUMPS-Install
Installation guide of MUMPS for python on Linux
### 1.Create a new conda environment first
```
conda create --name your_name python=3.7
conda activate your_name
```
### 2.Check mpicc environment
If mpi is not installed, you can install mpich or openmp.  
Add to the environment variable, and run the following command to check
```
which mpicc
# e.g. ~/anaconda3/pkgs/mpich-3.3.2-hc856adb_0/bin/mpicc
# Mark this path as "MPI_PATH"
```
### 3.Install mpi4py
```
env MPI_pth conda install mpi4py
# import mpi4py
# from mpi4py import MPI
# Check if it runs successfully
```
### 4.Install MUMPS
```
conda install -c conda-forge mumps
```
### 5.Install pymumps
```
conda install -c conda-forge pymumps
```
### 6.Find the mumps location
```
pip show pymumps
## e.g. ~/anaconda3/envs/py377/lib/python3.7/site-packages 
cd above_pth/mumps
vim __init__.py
```

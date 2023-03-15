# MUMPS-Install
Installation guide of MUMPS for python on Linux
### 1.Create a new conda environment first
```
conda create --name your_env python=3.7
conda activate your_env
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
## e.g. ~/anaconda3/envs/your_env/lib/python3.7/site-packages 
cd above_pth/mumps
vim __init__.py
```
Confirm whether the two underlined lines are commented. If not, comment it.
<div align="center">
<img src="https://github.com/MIA123MIA321/MUMPS-Install/blob/main/check.jpg"  width=50% />
</div>

### 7.Test
```
conda activate your_env
python test.py
## [1.,2.,3.,4.,5.]
```
### 8.References
././ 

### 9.points for attention
If a python file use MUMPS, it cannot import torch, otherwise, errors will occur.




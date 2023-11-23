# MUMPS-Install
Installation guide of MUMPS for python
### 1.Create a new conda environment first
```
conda create --name your_env python=3.7
conda activate your_env
```
### 2.Check mpich environment

```
conda list mpich
conda install -c conda-forge mpich=3.3.2 (if mpich is not found)
```
```
which mpicc
# e.g. ~/anaconda3/pkgs/mpich-3.3.2-hc856adb_0/bin/mpicc
# check if it is the same as `conda list mpich`
# if not found, add it into environment variable
```
### 3.Install mpi4py
```
conda install -c conda-forge mpi4py
# import mpi4py
# from mpi4py import MPI
# Check if it runs successfully
```
### 4.Install MUMPS
```
conda install -c conda-forge mumps
conda install -c conda-forge pymumps
```
### 5.Find the mumps location
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

### 6.Test
```
conda activate your_env
python test.py
## [1.,2.,3.,4.,5.]
```
### 7.References
[PyMUMPS: A parallel sparse direct solver](https://github.com/PyMumps/pymumps)




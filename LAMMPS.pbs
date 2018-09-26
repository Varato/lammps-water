#!/bin/sh
#PBS -N lammps-water
#PBS -l select=2:ncpus=24:mpiprocs=24:ompthreads=4:mem=96gb
#PBS -l walltime=24:00:00
#PBS -j oe
#PBS -P personal

inputfile="in.water_vitrify"
logfile="log.water_vitrify"

# load module environment
module load lammps/11Aug17/cpu

# change directory to the one where the job was submitted
cd ${PBS_O_WORKDIR}

# run the executable
mpirun "$LAMMPS_EXECUTABLE" -in "$inputfile" -log "$logfile"

The data storage is broken into 3 parts: `home`, `barn`, and `scratch`
 - Home is for "dot files", being environment configuration scripts
 - Scratch is for temporary usage, and may be cleared if not used
 - Barn is for longer-term storage and scripts.

Barn has `25GiB` of storage, unless explicitly asked for expansion. If data generation is done correctly and points selected intelligently, Barn will never need more storage.




## Systems of Interest


| Command   | Usage                                           |
| --------- | ----------------------------------------------- |
| `squeue`  | Lists my jobs in queue                          |
| `sinfo`   | Lists the state of all nodes in the system      |
| `sprio`   | Shows priorities of pending jobs and calcuation |
| `sacct`   | Displays data about jobs                        |
| `sbatch`  | Submit a batch script                           |
| `scancel` | Cancel a batch job                              |
| `salloc`  | Allocates an interactive session (for testing)  |



### Example Interactive Session
`salloc -t 30 --qos=interactive --gres=gpu:1 srun --pty bash -i`


erp01

### Example SBatch file
[Slurm Job Scheduler - Center for Computational Innovation - Documentation](https://docs.cci.rpi.edu/Slurm/)
```
#!/bin/bash 

#Slurm Directives
#SBATCH --mail-user=goodws2@rpi.edu
#SBATCH --mail-type=end,fail
#SBATCH -N 4
#SBATCH --time=00:02:00
#SBATCH --gres=gpu:4
#SBATCH -p dcs-2024

# Clear the environment from any previously loaded modules
module purge > /dev/null 2>&1

# Load the module environment suitable for the job
module load gcc
module load xl_r
module load spectrum-mpi/10.4
module load cuda/11.2

#Optional debugging information
echo "Starting at `date`"
echo "Running on hosts: $SLURM_NODELIST"
echo "Running on $SLURM_NNODES nodes."
echo "Running $SLURM_NTASKS tasks."
echo "Current working directory is `pwd`"

#Run the script that does your work
srun /gpfs/u/home/PROJ/PROJuser/barn/my_job.sh

#Optional debugging information
echo "Program finished with exit code $? at: `date`"
```



export http_proxy=http://proxy:8888
export https_proxy=http://proxy:8888


v4.12 was needed for x86_64 cluster, latest worked with DCS.




conda install --file src_hpc/requirements.txt -c conda-forge
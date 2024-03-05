# README.md

## Simulation Start Files
* Each directory labeled `4w5?--[ligand_name]` contains the T4-lysozyme complex gromacs simulation start files (`.gro` and `.top`)
	* The directories are labeled in the form `[xtal_protein_system]--[xtal_ligand]`
		* Ex: 
			* `4w52--benzene` is the 4w52 closed protein with its native ligand benzene bound
			* `4w52--butylbenzene` is a mixed system with 4w52 closed protein and the xtal binding mode of the 4w57 butylbenzene bound

## Simulation Run Files
* the simulation run files (gromacs `.mdp` files and slurm submission scripts) can be found in the `simulation_run_files` directories
	* `simulation_run_files/EM` contains the energy minimization `.mdp` file simulation settings
	* `simulation_fun_files/NVT_equil` contains the equilibration NVT `.mdp` file simulation settings
	* `simulation_fun_files/run_em_nvtequil.sh` SLURM submission script for EM and NVT equilibration
	* `simulation_fun_files/NPT_equil` contains the equilibration NPT `.mdp` file simulation settings
	* `simulation_fun_files/run_nptequil.sh` SLURM submission script for NPT equilibration
	* `simulation_fun_files/NPT_prod` contains the production NPT `.mdp` file simulation settings and SLURM submission script for NPT production

# msm_notebooks

## What's here:
- `[structure_name]-[ligand_name].ipynb`: notebooks of MSMs for each system studied in this work
- `all_systems_MSM_analysis.ipynb`: analysis of all systems and estimating transition timescales between discrete states
- `combined_trajectory.ipynb`: identifies TICA coordinates from a concatenated trajectory used for each system MSM 
- `extract_F_helix.ipynb`: extracts F-helix atoms from each system trajectory 

### tica
- `combined_traj_TICA.npy`: TICA coordinates for each frame of the concatenated trajectory
- `[structure_name]-[ligand_name].npy`: array of each system trajectory converted to TICA coordinates
- `[structure_name]-[ligand_name]_cluster_assign.npy`: microstate assignments of each system frame
- `[structure_name]_helix_TICA.npy`: TICA coordinates for different crystal structures
- `xtal_RMSDs.npy`: RMSD of each frame of the concatenated trajectory to each crystal structure

## Procedure
Included are all the notebooks we used to generate the data for this work. All notebooks can be run independently and do not require the original input trajectories. We provide both the TICA coordinates and microstate cluster assignments for each system that are needed to run the notebooks.

For users who wish to reproduce our work in more detail, we performed the following procedure.

1. Refer to our simulation details in the manuscript and starting files provided in the `simulation_files` directory to reproduce the trajectories.

2. For each trajectory, run the `extract_F_helix.ipynb` notebook to get trajectories of only the F-helix (residues 107-115) of each system.

3. Run the `combined_trajectory.ipynb` notebook to resolve a set of TICA coordinates which capture the opening of the T4 L99A binding pocket across different systems.

4. Run each `[structure_name]-[ligand_name].ipynb` notebook to create MSMs based on the slowest motions along the resolved TICA coordinates for each system.

5. Analyze all system MSMs and estimate transition timescales in the `all_systems_MSM_analysis.ipynb` notebook.  

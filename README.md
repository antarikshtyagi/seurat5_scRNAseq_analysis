# seurat5_scRNAseq_analysis
This jupyter notebook uses seurat5 R-conda environment. This environment can be installed using the seurat5.yml file
To install this environment run the following commands in an interactive session:

1. module load miniconda
2. conda env create -f seurat5.yml
3. Update the new conda environment on McCleary by 
	ycrc_conda_env.sh update
4. Before starting the analysis, mkdir matrix and copy the cellRanger filtered_feature_bc_matrix folder to the "matrix" folder named by sample. for example
ls matrix
KO_filtered_feature_bc_matrix   WT_filtered_feature_bc_matrix

5. Start a jupyter session in Open On demand and select seurat5 in the drop down menu. 12 hours, 1 CPU, 400G
6. open the sc_RNAseq_seurat5.ipynb and follow the comments in the cells

################
Note on azimuth reference

This notebook uses Azimuthh for cell type annotation. The reference database should be downloaded and saved in a folder
Download the appropriate reference from the Zenodo links available in this page: https://azimuth.hubmapconsortium.org/references/
unzip and save the two extracted files (idx.annoy and ref.Rds) under a folder. That folder will be used when running the RunAzimuth step of the notebook: 

RunAzimuth(seurat_obj, reference = "heart/") #"heart/" is the reference folder here

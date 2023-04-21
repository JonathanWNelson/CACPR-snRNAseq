# Instructions for Running CACPR snRNAseq Analysis
Jonathan Nelson
4.21.23

Step 1: Download folders and files from GitHub as a zip folder and place it on your computer (perhaps desktop?)

Step 2: Close R studio (if open) and then open the "Setup" RMD file and run each chunk in order to 1) create a .here file and 2) create file architecture below

	**Note** The code uses the package "here" (https://github.com/jennybc/here_here) in order to identify relative file locations. 
	It is critical that when you run the "here()" code in the console that it returns back the location of the "main" folder. 

	For instance, if you place the main folder on your desktop, the here() command should return: 
	[1] "C:/Users/jonat/OneDrive/Desktop/CACPR-snRNAseq-main"

* Main/
  * GitHub/
     * Pre-processing
     * Analysis
     * Figures
  * IRI dataset/
  * GEO/
     * Cell Ranger/
       * CACPR/
       * Sham/
  * Outputs/
  * .here 
  * Setup.RMD
  * ReadMe.md

Step 3: Download and place Cell Ranger output folders into the folder 

"../GEO/Cell Ranger/CACPR"
	filtered_feature_bc_matrix
	raw_feature_bc_matrix
"../GEO/Cell Ranger/Sham"
	filtered_feature_bc_matrix
	raw_feature_bc_matrix

Step 4: Place IRI files from GEO GSE139107 (https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE139107) into folder "../IRI dataset"
	GSE139107_MouseIRI_control.dge
	GSE139107_MouseIRI_12hours.dge

Final file architecture needs to look like this for the code to work. 

* Main/
  * GitHub/
     * Pre-processing
     * Analysis
     * Figures
  * IRI dataset/
     * GSE139107_MouseIRI_control.dge
     * GSE139107_MouseIRI_12hours.dge
  * GEO/
     * Cell Ranger/
       * CACPR/
         * filtered_feature_bc_matrix/
           * barcodes.tsv
           * features.tsv
           * matrix.mtx
         * raw_feature_bc_matrix/
           * barcodes.tsv
           * features.tsv
           * matrix.mtx
       * Sham/
         * filtered_feature_bc_matrix/
           * barcodes.tsv
           * features.tsv
           * matrix.mtx
         * raw_feature_bc_matrix/
           * barcodes.tsv
           * features.tsv
           * matrix.mtx
  * Outputs/
  * .here 
  * Setup.RMD
  * ReadMe.md

Step 5: Make sure that you have all packages installed nesseseary for running the Rmarkdown files

Step 6: Start by running the RMD files in the Main/GitHub/Pre-process folder in order from 1-4.

	**Note** Outputs from the analysis will appear in ../Outputs folder 

Step 7: Run analysis RMD files 1-5

Step 8: If only interested in running files to make figures: download the supplemental .rds and .rdata files from GEO and place in the "Outputs" folder and then run the code for creating each figure. 


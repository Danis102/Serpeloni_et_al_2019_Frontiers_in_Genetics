# Serpeloni_et_al_2019_Frontiers_in_Genetics-
Updated scripts that was originally published in Serpeloni et al. 2019 (Frontiers in Genetics vol 10).

This script was written by Dr Daniel Natt
Version 1.1 02/10/2019

--------------------------------------------------------------------------------
#          Initial notes

 These script will automatically generate some of the key results reported in Serpeloni et al 2019 (Frontiers in Genetics)

 All file inputs needed to perform the methylome switching analysis in the 
 Brazilian (target population for the current paper) and the publically 
 available African American Grady dataset, are available in the file 
 'Start_files.zip' which was published as a supplementary to 
 Serpeloni et al. 2019 (Frontiers in Genetics).

 Especially the Grady analysis is hardware demanding. The script worked fine on   
 a desktop computer having a i7-3930K 3.2GHz CPU with 48 GB of RAM, but failed on 
 a laptop having a i5-4210U CPU 2.4GHz with 8GB of RAM.

 Info about a functional session environment is listed in the end of this script. 
 The script are especially depending on: R version 3.5.1, GEOquery 2.48.0, minfi 1.26.2, reshape 0.8.7, limma 3.36.3,
 ggplot2 3.0.0, IlluminaHumanMethylation450kanno.ilmn12.hg19 0.6.0      
 IlluminaHumanMethylation450kmanifest 0.4.0

 Important: Sharing raw data from the Brazilian samples are regulated by 
 strict ethical protocols/permits to protect children and women living in criminal 
 environments. Therefore, we can only provide anonymized beta-values of the 
 1% top differentially methylated CpGs. By doing so we abolish the risk that 
 unauthorized persons may extract genetic fingerprints from the data. While   
 such possibility exists if providing raw data, the analytical pipeline that 
 was used here to generate the top 1% tables has been optimized for the     
 removal of microarray probes that may carry genetic information. This optimization
 was done in three steps:
		(1) Specific SNP probes on the array was omitted. 	
		(2)	We disregard CpG probes that overlap with genomic regions known to have
			  common polymorphism, as described in Chen et al. 2013 (Epigenetics, 8, 203-9).  	
		(3) We use robust statistics, which is a common method to minimize the effect of 
			  outliers. Since polymorphism often appears as data outliers, by using
			  robust statistics we minimize the number of probes that may unintentionally
			  hold genetic information in the 1% top tables. For more about this see Fig. S4.

 It must be noted that the Brazilian raw data can be acquired by contacting the main
 authors of this paper, but will be subjected to individual written consents, and 
 assurance that all research done on the material will follow the ethical protocols.  

 Nevertheless, by downloading the freely available Grady dataset from Gene Expression 
 Omnibus (GEO) anyone that which to validate the pipeline that we used to generate the 
 top 1% table from the Brazilian subjects may do so using the Grady dataset.  

 Lastly, we also provide scripts that will perform the novel methylome switching 
 on the Brazilian and Grady datasets side-by-side using the top 1% differentially 
 methylated CpGs of each dataset.

 We hope you will find our scripts useful. If you encounter any problems with the script
 please contact Dr Daniel N?tt, on daniel.natt@liu.se.
or check Daniel's github for possible script updates: https://github.com/Danis102



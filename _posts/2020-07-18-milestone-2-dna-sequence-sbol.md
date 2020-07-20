---
title: Milestone # 2: Incorporating dna sequence in SBOL file
date: 2020-07-18
categories: GeneTech, Python, GSoC-20, SynBio
---

- Started exploring the dna sequencing part
	
	- Explored the components used in the circuit
	
	- What is RBS? CDS? Promotor? Terminator? Ribozyme? where are they placed
	
	- How does SBOL format work
	
	- How is the current code doing it. What changes are needed?
	
	- Having power cuts and internet issues. So hard to maintain the same productivity. Progress got a bit slow
	
	- CELLO:
		- studied main paper (not entirely because not familiar with the technicalities, mainly the tables and figures)
			https://science.sciencemag.org/content/352/6281/aac7341
		- studied supplementary material (not entirely because not familiar with the technicalities, mainly the tables and figures)
			https://science.sciencemag.org/content/sci/suppl/2016/03/30/352.6281.aac7341.DC1/Nielsen.SM.pdf
		- Their git repo. SBOL .xml examples to see how the dna sequencing is embedded in it
		- Their website to see what they generate and how they do it
		- Compared their circuit .xml file to our sample .xml files. Figured out:
			- They mostly have insulated circuits. 
			- We are making non-insulated gate circuits
			- GeneTech doesn't specify what terminator it is using (we just use a dummy id for the terminator)
			- GeneTech has no information of the RBS whatsoever (its not even included)
			- For non-insualted circuits, Cello paper had the same terminator  
			
	- SBOL:
		- read briefly the data specification document (https://sbolstandard.org/wp-content/uploads/2016/06/SBOL2.3.0.pdf)
		- GeneTech report by Bhutto et. al to understand how they are doing it
		- pySBOL documentation
		- pySBOL paper
		- Created an example device to see how it works
		- sbol tutorials: 
			- https://sbolstandard.org/wp-content/uploads/2016/08/pysbol-crispr-tutorial.pdf
			- tutorial on their github
			- exampels on their github.
	
	- Made a database of the parts used in our Circuits:
		- All Input promoters
		- All output promoters
		- All CDS
		- Included a terminator
		- YFP
		- The links to the repository for each of these
		- Used pysbol to query the link for each of these and populated the database. 
    
	

		


- bugs: component definition [j][1] instead of [j][k]
- function.py



























**_Reference_**
- <https://synbiohub.programmingbiology.org/public/Eco1C1G1T1/YFP/1> (Info of YFP Sequence SynBioHub)
- <https://pysbol2.readthedocs.io/en/latest/getting_started.html> (pysbol2)
- <https://sbolstandard.org/wp-content/uploads/2015/07/pySBOL-tutorial.pdf> (A brief description of the CRISPR circuit using SBOL 2.0 data model)
- <https://readthedocs.org/projects/pysbol2/downloads/pdf/latest/> (pysbol reference guide)
- GeneTech2.0 Developers' Guide
- GeneTech2.0 Report
- <https://science.sciencemag.org/content/sci/suppl/2016/03/30/352.6281.aac7341.DC1/Nielsen.SM.pdf> (Nielson's Supplementary Material)
- <https://science.sciencemag.org/content/352/6281/aac7341> (Genetic Circuit Design Automation)
- <https://sbolstandard.org/wp-content/uploads/2016/06/SBOL2.3.0.pdf> (SBOL reference guide) 
- <https://github.com/CIDARLAB/cello/>(Cello's repository)

---
title:  "Milestone 1: Converstion of Java into Python"
date:   2020-6-17
categories: update
tags: GSoC
---

Welcome to the first blog posts of Mudasir Hanif Shaikh's GSoC journey working with GeneTech. This post presents updates on the first milestone of my project, that is, conversion of Java codebase of GeneTech into Python. I worked on this for over 5 weeks starting from mid-May of Community bonding period to week 3 of evaluation 1, and was able to convert all java code into python and integrate it with existing code. More updates to follow.

### Community Bonding Period and Week1
- Updates to follow
### Week2 to Week3
- Completed the conversion of the last class (TechMapping.Java) to Python
	
	- Fixed bugs in Tech mapping
	
	- Integration with existing python UI
	
	- Trying to resolve pySBOL issues. Tried:
		- Conda environment 
			- python 3.6 
			- python 3.7
			- python 3.8
		
		- Virutal environment
		
		- Online IDE (linux based, python 3.6.9, pysbol 2.3.3.post5 works well)
		
		- Replicated above configuration on my machine; didn't work. 
		
		- Python 3.8.3 with pysbol 2.3.3 works well on Linux and Mac whereas on my Windows machine python 3.8.3 couldn;t find pysbol 2.3.3.
		
		- Conclusion: pysbol 2.3.2 has libsbol bugs (fails when saving the sbol file as xml). pysbol 2.3.3 works fine on mac and linux but is not avaible for windows.
	
	- Switched to pySBOL2 (sbol2) which is a pure python implementation of pySBOL
	
	- The tool works now. 
	
	- Tried a bunch of stuff for packaging the tool. Issues faced:
		- The exe couldnt find the resources
		- Images and GatesLib not found
		- Resolved it by putting those in the distribution folder
		- Changed the distribution from a folder with loads of loaded libraries to a single file exe
	
	- Generated files are now saved in a separate user_files folder.

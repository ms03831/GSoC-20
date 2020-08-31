---
title: Final Report | GeneTech | Google Summer of Code 2020
date: 2020-08-30
tags: GSoC
mentor: Hasan Baig | Ritwik
organization: NRNB
---
<hr>

# Overview
GeneTech allow users to develop genetic logic circuits only by specifying a Boolean function. The tool first performs Boolean optimisation, followed by synthesis and technology mapping. Currently, a user can define the desired behavior in the standard Boolean notation. We would like to add the support for designing a circuit via drag and drop method on a design canvas. This functionality would allow users, specially electrical/electronic engineers, to design a genetic circuit by constructing the circuit schematic on a design canvas using drag-drop-wire approach. GeneTech will then transform the circuit schematic into the corresponding genetic circuit and represent it in the standard SBOL notation. The results produced by the current version of GeneTech do not include the DNA basepair encoding of circuit components. We would like to update the tool to be able to embed the DNA sequence of generated circuits in the SBOL file. 

Moreover, most of the existing source code at the backend of GeneTech is in Java. We would like to convert the Java code to python to make GeneTech an all python application. 

# Milestones 
## Milestone # 1: Conversion of Java codebase into Python
### About the task: 
  Before I started working on GeneTech, most of the source code at the backend was in Java. How this worked was that the Java code was precompiled and then the compiled executable was called from within python. This was an additional overhead and also produced some additional dependancies. For example the Java executable (an .exe) made it impossible for it to be run on unix based machines. There could have been workarounds but even those would have created addtional overhead. Therefore I suggested that we convert the Java code into Python. The milestone was successfully completed.
  ##### Related code and PR: [code](https://github.com/hasanbaig/GeneTech/tree/master/src) / [PR](https://github.com/hasanbaig/GeneTech/pull/4)
  <hr> 
## Milestone # 2: Incorporating dna sequence in SBOL file
### About the task: 
   Find more details about this at the following [post](https://ms03831.github.io/GSoC-20/update/milestone-2-dna-sequence-sbol/)
   #### note for future contributors:
   Try to look into the possibility of integrating **realtime online search** support for genetic parts that are not in the genetech library. 
   #### Related PR: [PR](https://github.com/hasanbaig/GeneTech/pull/5)
   <hr> 
## Milestone # 3: Adding Drag-Drop-Connect canvas for circuit equations
  Find more details about this at the following [post](https://ms03831.github.io/GSoC-20/final-milestone-drag-drop-canvas/)
### About the task: 
 ##### Related code: [code](https://github.com/hasanbaig/GeneTech/tree/circuit-builder)

# Future work

Although the following was not the part of my project I would like to work on these in the future. Will open the issues shortly and work with my mentor to resolve them.
  
  - Look into the issue that GeneTech sometimes doesn't generate circuits (optimisation issue)
  - The functions.py by previous contributors $MAY$ have some bugs, look into that!
  - Refactoring the code.
  - Support future contributors. 

  
# Parting words
I learned a great deal from this project. Special shoutout to NRNB for the support as well as my mentors, specially Hasan Baig for his constant support througout the project. He was very responsive, helpful and understanding. The project may not have been very successful if he had not been this helpful.  

Thank you NRNB, Google and Hasan Baig for providing me with the opportunity to be a part of this wonderful program! 
  
# Some regrets
Even though I tried my best and at times exceeded my own limits in terms of working on the project but I think I still didn't do as good a job as I had hoped. This was mainly due to the issues I faced throughout. This was a difficult time and I hope the project came at a different time, it would have been a lot better for everyone involved. 

%---
%permalink: /about/
%title: "About"
%---

# Generating detailed SBOL representation of genetic logic circuits along with improved designing capability, and SBML export in GeneTech

GeneTech allow users to develop genetic logic circuits only by specifying a Boolean function. The tool first performs Boolean optimisation, followed by synthesis and technology mapping. Currently, a user can define the desired behavior in the standard Boolean notation. I would like to add the support for designing a circuit via drag and drop method on a design canvas. This functionality would allow users, specially electrical/electronic engineers, to design a genetic circuit by constructing the circuit schematic on a design canvas using drag-drop-wire approach. GeneTech will then transform the circuit schematic into the corresponding genetic circuit and represent it in the standard SBOL notation. The results produced by the current version of GeneTech do not include the DNA basepair encoding of circuit components. I would like to update the tool to be able to embed the DNA sequence of generated circuits in the SBOL file. Finally, to be able to simulate the generated models, I plan to develop an API to convert the SBOL files into the corresponding SBML file. This will allow users to take the SBML files of the generated circuits to any SBML-compliant tool for functional verification.

## Organisation: 
### NRNB

## Mentors:
### - Hasan Baig
### - Ritwik Agarwal

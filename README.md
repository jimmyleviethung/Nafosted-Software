
DESCRIPTION:

It's is a novel software tool that, given a protein's structural model, search for similar structures from the list of input structure defined by the user.
The algorithm implemented by this software is based on a Fr-TM-align algorithm to find the largest subset of similar residues between an input protein and a collection of known functional and structure sites. 


SYSTEM REQUIREMENTS:

Software has been developed in Java SE 7. The application is meant to run locally on any operating system (Linux, Windows and Apple iOS systems) provided that they are equipped with a suitable 64-bit Java Virtual Machine (JVM) and with a Java Runtime Environment (JRE) version 1.7 or higher.


INSTALLATION:

Windows,Linux and Mac:
Download from this URL:https://github.com/jimmyleviethung/Nafosted-Software/
To extract all files and folders, right-click the compressed directory and then click "Extract all".

EXECUTION:

Windows:
To run the program, double-click on the executable file FrTMalign.jar. 

Linux and Mac:
type "java FrTMalign.jar" from the command line.

For all the operating systems:
The main panel interface will appear. Go to the "Run" menu and choose "Core algorithm". In the "Core algorithm panel" that appears, you can load your input protein coordinates in pdb format by choosing your "Input protein file".
In the "Known binding sites folder" you should choose which database (folder) you want to use.

In the same input panel you can specify several running parameters:
1) the minimum percentage of similar residues between the input protein site and the known site (default value 70%);
2) the minimum size (number of residues) of the similar site (default value 5);
3) the maximum RMSD value of the alignments (default value 2.5 A);
4) the interresidue distance similarity threshold (default value 1.5 A);
5) the structure level at which the comparison is made (backbone, sidechain or both):
6) the criterion used to calculate the percentage of similarity between the input protein site and the known site (residue identity or similarity, using the BLOSUM62 matrix):
7) the criterion to be used to initially sort the alignments (by their score value, corresponding to the clique size, or their RMSD value. The alignments can still be sorted afterwards in the output table according to different criteria).

For the detection of ligand binding sites, the user can also set the option to eliminate from the final output table all the alignments in which the residues of the input protein display steric clashes with the rototranslated ligand. This is done by checking the option "Check steric clashes?".
Results will be displayed as a tabular view with each record representing the alignment detected by the program. For each alignment the following information are reported: 
the alignment number, the known protein's name and PDB ID, the ligand's name, the groups of residues aligned from the input and the known protein, the residues building up the functional site from the known protein, the size of the known functional site, the percentage identity between the input protein's site and the known site, the clique size and the RMSD value.
For each of the alignments the user is given the possibility of displaying three-dimensional representations of the alignment via the embedded JMol program. These include: (i) the input protein with its aligned residues highlighted in green, upon which the corresponding functional site from the known protein is superimposed, and (ii) the known protein with the residues from its active (or ligand binding) site highlighted in red. The putative ligand is highlighted in yellow.
Lastly, an "info" button provides information regarding the known protein (and ligand in the case of binding sites) and links to the relevant PubMed and Protein Data Bank web pages.
It must be noted that, in order for the latter two functionalities to work correctly (displaying the known protein with the residues from its active/ligand binding site and showing info from PubMed/PDB) an Internet connection is required.

SAVING THE OUTPUT
For all operating systems:
To save the output results, select the "File" menu in the main panel and click on "Save" or "Save as". You will be able to save the results in the desired destination as a file with the ".alg" extension. You can specify the name of such output file in the "selection" field. You will also be able to re-display results of a previous execution by selecting the "File" and choosing "Open", and then browsing your file system for an .alg file earlier saved.

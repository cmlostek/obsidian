The **Protein Data Bank** (PDB) is a publicly accessible repository of three-  
dimensional (3D) structural data of biological macromolecules, such as proteins,  
nucleic acids, and complex assemblies. It serves as a critical resource for  
researchers studying molecular biology, biochemistry, and related fields.  
[Main Webpage](https://www.rcsb.org/ ) 
[Details](https://www.sciencedirect.com/science/article/pii/S0022283620306227 )
1. Explain what type of data is stored in PDB? Who are the end-users of PDB? 
	1. Data on proteins, their structure, the number of amino acids, and more are examples of types of data stored within PDB. The end-users of the PDB are individuals who may need to use it for research (Scientists, Bioinformaticists, Students) 
2. List at least three possible metadata for PDB records. How are they useful? Add screenshots if needed.
	1. Molecule name
		1. Useful when identifying the molecule you are looking for rather than having to use the Primary key / ID
	2. Sequences
		1. Useful if you only know the sequence for the protein.
	3. Chemistry
		1. Useful to help identify how it may interact with other proteins / chemical structures within the body. 
3. What type of data models PDB implements and how does it help curation, visualization, statistical analyses etc? 
	1. Relational Database Model is used to describe, Atomic level details, biological assemblies, and some annotations like functional sites and domain structures. It also uses mmCIF or Macromolecular Crystallographic Information Files) to represent data which replaces the pdb file format. This helps curation by standardizing file formats, allows for automation, and works better to track version control. 
4. How does the PDB ensure that data from different users are consistent and standardized?
	1. By using standardized formats, dictionaries to validate language in specific fields, consistent naming conventions, submission standards, etc... the PDB ensures all entries are consistent, easily readable, and accessible to any one trying to access files within the database. 
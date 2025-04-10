# CyclotideScreen
## Contributor
- [Ajaya Kumar Sahoo](https://github.com/ajayaksahoo)

## Reference
This repository provides the input files for reproducing the protein-cyclotide docking results and the MD simulation results of the docked protein-cyclotide complexes and the co-crystallized protein-small molecule complex reported in the following manuscript:

Sreejanani Sankar<sup>#</sup>, Ajaya Kumar Sahoo<sup>#</sup>, Shanmuga Priya Baskaran, R. Babu, Smita Srivastava* and Areejit Samal*, [<i>Computational prediction of cyclotides from Viola odorata as potential inhibitors against the neuraminidase of Streptococcus pneumoniae</i>](https://www.biorxiv.org/content/10.1101/2024.12.08.627407), bioRxiv 2024.12.08.627407.<br>

(<sup>#</sup> Joint-First authors, * Corresponding authors) 

## Repository Organization
- [Docking](./Docking): This folder contains the input pdb files required to perform protein-cyclotide docking in FRODOCK 2.0 server and the generated best docked pose of the protein-cyclotide complex.
- [MDsimulation](./MDsimulation): This folder contains the parameter files to run MD simulation in GROMACS for the best docked pose of the protein-cyclotide complex from the [Output](./Docking/Output) folder. Additionally, this folder contains the input pdb, ligand topology and the parameter files to run MD simulation of the co-crystallized protein-small molecule complex in GROMACS, as reported in this manuscript.

## Instruction
- To run protein-cyclotide docking in [FRODOCK 2.0 server](https://frodock.iqf.csic.es/), use the following files:
  - receptor file: [SpNanA.pdb](./Docking/Input/SpNanA.pdb)
  - ligand files: [CyV_O15.pdb](./Docking/Input/CyV_O15.pdb), [CyV_O36.pdb](./Docking/Input/CyV_O36.pdb), [Kalata_B1.pdb](./Docking/Input/Kalata_B1.pdb), [Kalata_S.pdb](./Docking/Input/Kalata_S.pdb), [Vodo_L12.pdb](./Docking/Input/Vodo_L12.pdb)
- To run the MD simulation of the protein-ligand complex in [GROMACS](https://www.gromacs.org/), use the following files:
  - input files for protein-cyclotide complex: [Output](./Docking/Output)
  - parameter files for protein-cyclotide complex: [Parameter](./MDsimulation/Parameter)
  - input file for co-crystallized protein-small molecule complex: [Protein_ligand.pdb](./MDsimulation/Protein-Smallmolecule/Protein_ligand.pdb)
  - input file for small molecule topology: [ligand.itp](./MDsimulation/Protein-Smallmolecule/ligand.itp)
  - parameter files for protein-small molecule complex: [Protein-Smallmolecule](./MDsimulation/Protein-Smallmolecule)
  - detailed steps involved in running MD simulation in GROMACS can be viewed in this [tutorial](http://www.mdtutorials.com/gmx/complex/index.html)

# DACUM
The Database of binding Affinity Change Upon Mutations in protein complexes

## Format
**SKEMPI_ID:** The column is a combination of columns “Protein” and “Mutation (s)_PDB” from SKEMPI database.  In SKEMPI_ID, there are 4 parts separated by underscore “_”. The first part is PDB entry for the complex, the second and third parts are chain identifiers for two subunits of the complex, and the last part is mutation corresponding to the residue numbering in Protein Data Bank. The characters of the mutation part are one letter amino acid code of original residue, chain identifier, residue number followed residue insertion code where applicable, and mutant residue, respectively.

**ΔΔG:** The values of binding affinity change on mutation in kcal/mol from experiments.

**Position:** The position of single point mutation, i.e. interface (ITF) or non-interface (NIF) mutation, is defined based on the column “Location(s)” in SKEMPI database. The mutation located on COR, RIM or SUP region is defined as interface mutation, while the one on INT or SUR region as non-interface mutation.

**Method:** The abbreviation of experimental methods for each mutation. The corresponding full names of methods are listed in the following table of Experimental measurement methods.

**Reference:** The column is extracted from the “Reference” in SKEMPI database. The PubMed ID is given where available, otherwise the whole reference is provided.

## Experimental measurement methods
| Abbreviation | Full name                                  |
|--------------|--------------------------------------------|
| ITC          | Isothermal Titration Calorimetry           |
| SPR          | Surface Plasmon Resonance                  |
| FL           | Fluorescence                               |
| SP           | Spectroscopy                               |
| SFFL         | Stopped-Flow Fluorescence                  |
| SFSP         | Stopped-Flow Spectroscopy                  |
| IAFL         | Inhibition Assay Fluorescence              |
| IASP         | Inhibition Assay Spectroscopy              |
| IAGE         | Inhibition Assay Gelelectrophoresis        |
| IARA         | Inhibition Assay Radioactivity             |
| RA           | Radioactivity                              |
| CSPRIA       | Competition Solid-Phase Radio-Immune Assay |
| ELFA         | Enzyme-Linked Functional Assay             |
| ELISA        | Enzyme-Linked Immunosorbent Assay          |
| EMSA         | Electrophoretic Mobility Shift Assay       |

## Citation
Cunliang Geng, Anna Vangone and Alexandre M.J.J. Bonvin, Exploring the interplay between experimental methods and the performance of predictors of binding affinity change upon mutations in protein complexes. 2016, To be submitted.



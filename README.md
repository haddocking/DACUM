# DACUM
**D**atabase of binding **A**ffinity **C**hange **U**pon **M**utations in protein complexes

The DACUM is a cleaned subset of the SKEMPI database (Moal and Fernández-Recio, 2012), which contains 1872 non-redundanted, single point mutations with additional information on the experimental methods used to measure the binding affinity. 

## Format
**1. SKEMPI_ID:** The column is a combination of columns “Protein” and “Mutation_PDB” from SKEMPI database (see below).

**2. Protein:** (SKEMPI) The PDB entry for the complex, followed by the chain identifiers for the two subunits. The first chain(s) correspond to protein 1 (column 16) and the second chain(s) correspond to protein 2 (column 17). Here is the [Protein Data Bank](http://www.rcsb.org/pdb/home/home.do).

**3. Mutation_PDB:** (SKEMPI) The mutation corresponding to the residue numbering found in the Protein Data Bank. The first character is the one letter amino acid code for the original residue, the second character is the chain identifier, the third to penultimate characters indicate the residue number, followed by the residue insertion code where applicable, and the final character indicates the mutant amino acid. Where multiple mutations are present, they are separated by commas.

**4. Mutation_cleaned:** (SKEMPI) The mutation corresponding to the residue numbering in the 'cleaned' pdb files provided by SKEMPI, in the same format as for column 3 "Mutation_PDB". Here are the [cleaned PDB files]( http://life.bsc.es/pid/mutation_database/SKEMPI_pdbs.tar.gz).

**5. Location:** (SKEMPI) The location of the mutation in or away from the binding site, i.e. COR, RIM, SUP, INT and SUR, as defined in (Levy, 2010).

**6. Position:** The position of single point mutation, i.e. interface (ITF) or non-interface (NIF) mutation, is defined based on the column 5 “Location”. The mutation located on COR, RIM or SUP region is defined as interface mutation, while the one on INT or SUR region as non-interface mutation.

**7. Kd_mut (M):** (SKEMPI) The dissociation constant of the mutant form.

**8. Kd_wt (M):** (SKEMPI) The dissociation constant of the wild-type form, or form in the PDB structure.

**9. dG_mut (kcal mol^(-1)):** The binding free energy of the mutant form. dG_mut = RTln(Kd_mut), R the ideal gas constant (0.0019872 kcal K^(-1) mol^(-1)), T the temperature (column 12) in Kelvin.  

**10. dG_wt (kcal mol^(-1)):** The binding free energy of the wild-type form, or form in the PDB structure. dG_wt = RTln(Kd_wt).

**11. ddG (kcal mol^(-1)):** The binding affinity change on mutation. ddG = dG_mut - dG_wt = RTln(Kd_mut/Kd_wt).

**12. Temperature (K):** (SKEMPI) The temperature at which the experiment was performed.

**13. Method:** The abbreviation of experimental measurement method for each entry. The corresponding full names of methods are listed in the following table of Experimental measurement methods.

**14. Hold_out_type:** (SKEMPI) Some of the complexes are classified as protease-inhibitor (PI), or antibody-antigen (AB). This classification was introduced to aid in the cross-validation of empirical models trained using the data in the SKEMPI database. so that proteins of a similar type can be simultaneously held out during a cross-validation.

**15. Hold_out_proteins:** (SKEMPI) This column contains the PDB identifiers (column 2) and/or hold-out types (column 14) for all the protein complexes which should be excluded from the training when cross-validating an empirical model trained on this data, so as to avoid contaminating the training set with information pertaining to the binding site being evaluated.

**16. Protein 1:** (SKEMPI) This is the name of the protein which corresponds to the first chain(s) given in column 2 "Protein".

**17. Protein 2:** (SKEMPI) This is the name of the protein which corresponds to the second chain(s) given in column 2 "Protein".

**18. kon_mut (M^(-1)s^(-1)):** (SKEMPI) The association rate for the mutant protein, where available.

**19. kon_wt (M^(-1)s^(-1)):** (SKEMPI) The association rate for the wild-type protein or protein in the crystal structure, where available.

**20. koff_mut (s^(-1)):** (SKEMPI) The dissociation rate for the mutant protein, where available.

**21. koff_wt (s^(-1)):** (SKEMPI) The dissociation rate for the wild-type protein or protein in the crystal structure, where available.

**22. dH_mut (kcal mol^(-1)):** (SKEMPI) The enthalpy of association for the mutant protein, where available.

**23. dH_wt (kcal mol^(-1)):** (SKEMPI) The enthalpy of association for the wild-type protein or protein in the crystal structure, where available.

**24. dS_mut (cal mol^(-1) K^(-1)):** (SKEMPI) The entropy of association for the mutant protein, where available.

**25. dS_wt (cal mol^(-1) K^(-1)):** (SKEMPI) The entropy of association for the wild-type protein or protein in the crystal structure, where available.

**26. Reference:** The column is extracted from the “Reference” in SKEMPI database. The PubMed ID is given where available, otherwise the whole reference is provided.

**27. Notes:** (SKEMPI) Notes regarding the entry.

**28. Notes_method:** Notes regarding the column 13 "Method".


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
Cunliang Geng, Anna Vangone and Alexandre M.J.J. Bonvin, [Exploring the interplay between experimental methods and the performance of predictors of binding affinity change upon mutations in protein complexes. ][1] _Protein Engineering, Design, and Selection_, 29, 291-299 (2016).


## Reference
- Moal, I. H. & Fernández-Recio, J. SKEMPI: a Structural Kinetic and Energetic database of Mutant Protein Interactions and its use in empirical models. Bioinformatics 28, 2600–2607 (2012).
- Levy, E. D. A Simple Definition of Structural Regions in Proteins and Its Use in Analyzing Interface Evolution. Journal of Molecular Biology 403, 660–670 (2010).

[1]: https://doi.org/10.1093/protein/gzw020

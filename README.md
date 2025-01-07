# Antiviral Drug Repurposing for Monkeypox Virus With Genomic Evolution

Collaborators: Lige Zhang (DKU '26), Bruce Zhou (DKU '24), Prof. Gaoyang Li, Prof. Huansheng Cao.

# Molecular Docking

## Screening Library

The screening library was obtained from Enamine Bioactive Compounds Collection, which consists of annotated compounds and FDA-approved drugs. It can be accessed at: https://enamine.net/compound-libraries/bioactive-libraries.

## Ligand Preparation

The screening library was originally prepared in 2D SDF format. We used the Open Babel 3.0.1 on Linux to generate the 3D coordinates for each compound. The quality was set to "slowest", which performs "Force field cleanup (500 cycles) + Slow rotor search".

## AutoDock Preparation

We prepared the PDBQT files needed for docking with AutoDock Vina using the [Meeko package](https://github.com/forlilab/Meeko/tree/release). Specifically, we used the mk_prepare_ligand.py script to turn 3D SDF files into the PDBQT files needed for docking.

The receptors were prepared using the AutoDockTools GUI following the standard workflow.

## Docking

A blind docking strategy was adopted. For each receptor, the docking grid size was determined manually to make sure that the search covers the whole protein.

The maximum number of binding modes to generate was set to 50, and the exhaustiveness was set to 16 to increase search converage.

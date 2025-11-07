This repository contains the additional simulation data and analyses of the study “Helical transition of the bridge helix of Cas12a is an allosteric regulator of R-loop formation and RuvC activation.” Within the pca folder, trajectory files and videos for pca1 and pca2 are available. The correlationMatrices folder provides the main correlation analysis results, compiled into an Excel spreadsheet (.xls). In addition, supplementary information about the simulation setups and conditions is included below to provide further context for reproducing and interpreting the results.

<b> 1.0 SYSTEM SETUP

| System            | Box dimensions (Å)       | Total atoms | Water molecules | Na⁺ ions | Salt concentration note            |
| ----------------- | ------------------------ | ----------: | --------------: | -------: | ---------------------------------- |
| FnoCas12aKD2P-S2  | 152.82 × 152.99 × 152.78 |     321,238 |          99,541 |       21 | Neutralization   |
| FnoCas12aKD2P-S4b | 150.08 × 150.44 × 150.28 |     300,672 |          92,456 |       43 | Neutralization  |
| FnoCas12aWT-I2    | 157.18 × 156.79 × 156.96 |     347,398 |         107,936 |       50 | Neutralization  |
| FnoCas12aWT-I4    | 152.82 × 152.99 × 152.78 |     320,234 |          98,612 |       75 | Neutralization  |


<b>1.1 RMSD ANALYSIS</b>

We observed minimal fluctuations in the RMSD across the different systems, indicating that the MD simulations are very stable, and possibly trapped in the local minima (Fig. 1). The absence of side chains in the FnoCas12aWT I2 experimental structure led to greater structural rearrangements during the initial phase of MD simulation until reaching a minimum energy configuration, albeit less than that observed in other systems.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/d4e9d807-227e-4d1e-8da6-0f7391dbf92d" />

<b> Figure 1. Root Mean Squared Deviation (RMSD) of FnoCas12aWT and FnoCas12aKD2P states.</b> Colored lines represent the individual states: FnoCas12aKD2P S2 (purple), FnoCas12aKD2P S4b (green), FnoCas12aWT I2 (blue), and FnoCas12aWT I4 (orange). The RMSD was calculated by comparing each frame of the 1 μs MD trajectory to the corresponding average structure of each system.

<b>1.2 RMSF ANALYSIS</b>

RMSF analysis revealed high atomic fluctuations across all four states, limiting its utility in distinguishing functionally relevant differences between conformations (Fig. 2). No consistent pattern emerged that clearly defined transitions along the activation pathway. However, notable exceptions were observed in the REC2 and Nuc domains, which displayed pronounced fluctuations in states S4b and I2 (Figure SX2B and SX2C, respectively). These elevated dynamics may reflect their structural rearrangement roles during the conformational progression of Cas12a. Despite this, the widespread and overlapping flexibility profiles suggest that RMSF alone is insufficient to capture the coordinated domain motions critical for functional activation. Therefore, to better understand the relationship between states, we performed PCA analysis and cross-correlation network analysis.

<center><img width="500" alt="image" src="https://github.com/user-attachments/assets/e080fb5b-cc54-4301-949e-109124e283b7" /></center>

<b>Figure 2. Root Mean Squared Fluctuation (RMSF) analysis of FnoCas12aKD2P and FnoCas12aWT states.</b> RMSF profile for states A) S2 (FnoCas12aKD2P), B) S4b (FnoCas12aKD2P), C) I2 (FnoCas12aWT), and D) I4 (FnoCas12aWT). RMSF was computed over the production trajectories, with highlighted structural domains REC1 (light green), REC2 (dodger blue), PI (salmon), RuvC (medium purple), BH (hot pink), H1 (purple), WED (tan) and Nuc (grey) and also shown in a representative structure of state I4 (left).

<b>1.3 Interaction Distances</b>

We analyzed key interaction distances of a set of amino acids between different protein regions and with crRNA and DNA throughout the simulation time for all the structures. These interactions were analyzed to assess the DNA cleavage results obtained for the alanine substituents. As noted in the figure legends below, some interactions are present in earlier states of the conformational cascade and is associated with an occluded RuvC pocket, while others form in the pre-catalytic state to open the RuvC pocket and to position the crRNA and DNA to stabilize the full R-loop. 

The changes in the inter-residue distances observed during MD simulations between states S2, S4b, and I4 provide insights into the conformational transition of FnoCas12a, especially the interaction network between the BH-H1 and lid regions (Figure 3). As can be observed in the distance probability distributions, states S4b and I4 display increased frequency of short distance interactions when compared to S2. During FnoCas12a transition from early S2 state toward more active I4 state, the BH-H1 and lid regions come into closer proximity. Moreover, these results support the idea that S4b presents an intermediate with more interactions than S2, but not as strong as I4.

<img width="453" height="252" alt="image" src="https://github.com/user-attachments/assets/ff5a7abf-a43d-4966-9846-e59425de0650" />


Figure 3. Probability density distribution obtained during MD simulations of the distances between (A) E961 OE1 and K1021 NZ, (B) R968 NH1 and E1020 OE1, (C) R968 NH2 and E1020 OE2, (D) R964 NE and E1020 OE1, (E) K981 NZ and E1020 OE1, and (E) K981 NZ and N1022 OE1 in the systems FnoCas12aKD2P (S2) in purple, FnoCas12aKD2P (S4b) in green, FnoCas12aWT (I2) in blue, and FnoCas12aWT (I4) in orange. E1020-K981 interaction (panel E) occludes the RuvC active pocket and is present in earlier states in the conformational cascade, while E961-K1021 (panel A), R968/R964-E1020 (panels B, C, and D), and K981-N1022 (panel F) form in pre-catalytic state and opens the RuvC pocket.

A similar pattern is observed in the interactions between the protein and both DNA and RNA, reinforcing the notion that S4b represents a transitional state (Figure 4) towards the fully activated I4 conformation (Figure 4). This suggests that similar to the BH-H1/lid contacts, protein and nucleic acid interactions also become progressively stronger and more frequent as the system advances towards the activation pathway.

<img width="454" height="189" alt="image" src="https://github.com/user-attachments/assets/6f6ce2af-e510-45a7-9692-1e0e24898674" />

Figure 4. Probability density distribution obtained during MD simulations of the distances between (A) Cas12aKD2P S4b state interactions R964 NH2 and -dT8 O3’ DNA (purple), R964 NH1 and -dT7 OP1 DNA (green), and R968 NE and U10 O3’ RNA (blue) and (B) Cas12aWT I4 state interactions R964 NH2 and -dT8 O3’ DNA (purple), R964 NH1 and -dT7 OP1 DNA (green), and R968 NE and U10 O3’ RNA (blue). The interactions with crRNA/DNA are formed in the pre-catalytic state.


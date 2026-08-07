## 3/31/26

Paper: [citation](https://arxiv.org/pdf/1909.13107)
## Goals

- Improve data reduction of the VLT/SPHERE instrument.
### My Questions

- How do we correct instrumental polarization for NIRC2?
## Abstract

This paper provides an overview of the VLT/SPHERE polarimetric imaging mode. They compare two data reduction methods on observations of **TW Hydrae**: minimization of noise image $U_{\phi}$; and a model-based correction in a second paper. They used the model based correction to explain variability in polarized intensity. There are a few suggestions on VLT/SPHERE configuration and a pipeline reccomendation.
- **TW Hydrae** - type of variable star 10 Myr old and 80% the mass of the sun that accretes a protoplanetary disk face-on to the Earth
## Introduction

SPHERE observes in two color filters with **dual band imaging (DBI)** to detect planets
- uses linear polarization filters
- great promise for the characterization of polarized substellar companion
- Van Holstein et al. (2017) searched for a polarization signal in HR 8799 and PZ Tel, 
- similar attempts with GPI for HD 19467 B by Jensen-Clem et al. (2016) and β Pic b by Millar-Blanchaer et al. (2015).

SPHERE's intrumental polarization can be broken into two types
1) introduction of polarization
2) mixing of palarization states in the light beam, or instrumental polarization

Section 2: description of DBI
Section 3: optical components
Section 4: data reduction principles
Section 5.1: TW Hydrae observations
Section 5: instrumental polarization
Section 6: application of the model correction
Section 7: reccomendations for SPHERE
Section 8: comparison to other NIR AO polarimetric imagers

 [jargon dictionary](https://docs.google.com/document/d/1sLHNH8eOdbiF976ITBlYeP2iv0-voBHO4pVBTXUDlHc/edit?usp=sharing). 

- Concept 1: (paste the information and links here)  

- Concept 2: (paste the information and links here)  

- Concept 3: (paste the information and links here)

The incident beam goes into a beam splitter where one side gets rotates by 90°. Then, the intensities are measured. The stokes parameters are
$$
\begin{align}
I=I_{1}+I_{2} \\
Q=I_{1}-I_{2}
\end{align}
$$
In an ideal polarimeter, we use a HWP is placed upstream of the beamsplitter, and then the intensities are measured.
$$
\frac{I_{1}}{I_{2}}=\frac{1}{2}(I\pm U)
$$
In a real polarimeter, we use two HWP angles, 0° and 45°, upstream of the beamsplitter to correct for IP. The second HWP changes the signs of the beam’s original Q component but leaves the IP created downstream from the HWP unaltered.
$$
\begin{align}
Q^{+}=Q+P_{I}:\theta=0^{\circ} \\
Q^{-}=-Q+P_{I}:\theta=45^{\circ}
\end{align}
$$
We then retrieve all the Stokes parameters
$$
\begin{align}
Q=\frac{1}{2}(Q^{+}-Q^{-}) \\
I_{Q}=\frac{1}{2}(I_{Q^{+}}+I_{Q^{-}}) \\
U=\frac{1}{2}(U^{+}-U^{-}) \\
I_{U}=\frac{1}{2}(I_{U^{+}}+I_{U^{-}}) \\
\end{align}
$$

---
## Methods

Read through the methods section of the paper, trying not to get bogged down in jargon and details. Remember, this is the section of a paper that is written for experts in the particular subfield, so read for the big picture only. 

  

What tools did the authors employ in their study (observations? simulations? what kinds?).

Be specific. What telescopes? What kinds of codes? What instruments? What wavelengths?
### Data Reduction

To substract IP, take the median $c_{Q}$ of the Q/I signal in an annulus centered around the star.
- should include non-scatted starlight
$$
\begin{align}
Q_{IPS}=Q-I_{Q}c_{Q} \\
U_{IPS}=U-I_{U}c_{U} \\
\end{align}
$$

---
## Figures, Graphs and Tables

After reading abstract, intro and methods, but *before* reading the results and discussion sections, read through all of the figures/graphs/tables in the remainder of the paper and their captions. If you find you’re struggling with placing them into context, you might also consider reading the results section to solidify your understanding of the final conclusion of the research and therefore the figures. Try to get as much information out of them as possible. 

Identify and include the two most compelling/persuasive/conclusive figures or tables from the paper below (i.e. your highlight reel). For each figure, answer the following:

Figure or Table 1

1. Write a caption for the figure in your own words. What is being displayed? What does it reveal?

2. How are these measurements made?(it may be helpful to paste in the description from the methods)

3. What conclusions can you draw from this data?

4. How does this data contribute to the argument the authors are making?

5. What questions does this data raise for you?  


Figure or Table 2

1. Write a caption for the figure in your own words. What is being displayed? What does it reveal?

2. How are these measurements made?(it may be helpful to paste in the description from the methods)

3. What conclusions can you draw from this data?

4. How does this data contribute to the argument the authors are making?

5. What questions does this data raise for you?

*Optional* If there are other key figures or tables that it would benefit you to reference later, please do the same for these in the space below. 

---
## Results and Discussion 

After reading the results and discussion section(s), answer the following questions:

- Describe the main conclusion(s) of the study, referring to the figures mentioned above.  

- What does this study add to the broader science question it aimed to inform? What is still unknown?  

- In your opinion, how strong is the evidence in support of the results/conclusions of this study? How conclusive are the results?

- What is the next logical step to follow this study? What is the next question that should be answered?

---
## Take-Home

- Are any of the methods or concepts from the paper relevant to your own project or interests?  
    For example: "Good introduction that explains...", "Table 2 has a collection of data for types of stars similar to my project", "Interesting examples of young stellar object lightcurves", etc. 

- Did the paper answer the questions you wanted it to? If it did not, which questions do you still want answered and where might you go to find those answers?  

- What do you think is the most important knowledge you gained from reading this paper? (Including any new knowledge you encountered while searching for jargon)  

- What questions do you still have about the content of the article? These could be specific tricky phrases/equations/plots or broad ideas that are still fuzzy for you. List at least two questions that you’d like to discuss with a mentor. 
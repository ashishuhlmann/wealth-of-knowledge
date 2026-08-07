## 4/20/26

Paper: [citation]()
## Goals

I want to understand how NIRC2 works and what we need to consider for our pipeline.
## Abstract

NIRC2-Pol is a new imaging mode on the Keck II telescope (the largest IR polarimetry camera now), and first light images were taken of the AB Arigae circumstellar disk. No polarization intensity peak was detected at it's companion location confirming it is not a disk artifact. These images also revealed the spiral arms more clearly.
## Introduction

Polarimetry is of interst in HCI, the galactic center, and AGN.
- NIRC2 now images from Y-M bands.

Polarimeters capabilities typically only go up to the K band, excluding the IR L' band.
- VLT/SPHERE/IRDIS
- Subaru/SCExAO/CHARIS
- Gemini/GPI

A full Mueller Matrix model is currently being developed to account for full instrumental polarization, and for now a proccessing pipeline is also being made (our project).

---
## Methods

### How to Observe

NIRC2 includes
- **vector vortex** coronographic mask - has spatially-varying retardance, altering the polarization of incoming light and making data processing more complex
- Wollaston prism - splits beam into two orthogonal polarization states
- HWP1 - rotates polarization state optimized for J/H/K bands with 92% throughput
- HWP2 - optimzed for L' band with >90% throughput
- field mask - ensures that ordinary and extraordinary images do not overlap
- **precision calibration unit (PCU2)** - rotates HWP or moves pinhole mask

Generally, a HWP cycle should aim for 4 minutes (1 minute per angle).

There are three tested modes
- standard imaging polarimetry
- high-contrast imaging polarimetry with traditional **Lyot coronagraphs**
- high-contrast imaging polarimetry with a vortex coronagraph

L' presents high thermal background. It is reccommended to take sky flats with each observation for three HWP angles.

The derotator angle strongly affects polarization efficiency.
- most affected at shorter wavelengths
- 45° produces the best efficiency, while 0° and 90° should be avoided.

Commissioning observations measured an average Strehl ratio of 56.6±0.9%.
- NCPAs from the Wollaston are a likely culprit for the degradation of the correction.

we recom-324 mend taking a sequence of images with HWP angles 0325 to 180 degrees after each installation to confirm the fast326 axis orientation of the waveplate.
### Data Processing

1. Dark subtract and flat field the data.
2. Remove bad pixels with a 7x7 median window.
3. Split ordinary and extraordinary images.
4. Subtract the mean thermal background.
5. Center the frames.
6. Retrieve Stokes $Q$ and $U$ with a double difference
$$
\begin{align}
Q&=\frac{1}{2}(Q^{+}-Q^{-})=\frac{1}{2}(I_{1}(0^{\circ})-I_{2}(0^{\circ})-I_{1}(45^{\circ})-I_{2}(45^{\circ})) \\
U&=\frac{1}{2}(U^{+}-U^{-})=\frac{1}{2}(I_{1}(22.5^{\circ})-I_{2}(22.5^{\circ})-I_{1}(67.5^{\circ})-I_{2}(67.5^{\circ})) \\
\end{align}
$$
7. Switch to sky reference frame through a rotation matrix.
	- The angle accounts for the image rotator position relative to the bench, and the offset of the HWP fast axis from zero (59.7° measured in daytime)
	- The position angle of each frame is calculated as the parallactic angle (`PARANG`) plus the image rotator position relative to the sky (`ROTPOSN`) minus the NIRC2 instrument offset angle (`INSTANGL`) plus an offset as reported. Use the header keywords `theta = -PARANG + EL + ROTPDEST + 59.7`.
8. Derotate the images using `pyklip.rotate`.
9. Switch to Stokes radial parameters.
$$
\begin{align}
Q_{\phi}=Q\cos{(2\theta)}-U\sin{(2\theta)} \\
U_{\phi}=Q\sin{(2\theta)}-U\cos{(2\theta)} \\
\end{align}
$$
10. Preform a minimization of $U_{\phi}$ on each frame to find the best fit center positions and two instrumental polarization terms (one each for $Q$ and $U$). 
11. Combine the images with inverse noise weighting (those with the lowest standard deviation in $U_{\phi}$ are weighted the403 highes)

Total intensity can be recovered from polarimetric ob-405 servations by averaging the double sums (IQ and IU ) de-406 rived from the 0/45◦ and 22.5/67.5◦ cycles respectively

Read through the methods section of the paper, trying not to get bogged down in jargon and details. Remember, this is the section of a paper that is written for experts in the particular subfield, so read for the big picture only. 

What tools did the authors employ in their study (observations? simulations? what kinds?).

Be specific. What telescopes? What kinds of codes? What instruments? What wavelengths?

---
## Figures, Graphs and Tables

Figure 1

1. Write a caption for the figure in your own words. What is being displayed? What does it reveal?
A raw image of a star is shown. The top and bottom are the two ordinary and extraordinary images. There are a few defects and a bright stripe in the middle where the images overlap by accident.

2. How are these measurements made?(it may be helpful to paste in the description from the methods)

3. What conclusions can you draw from this data?

4. How does this data contribute to the argument the authors are making?

5. What questions does this data raise for you?  


Figure or Table 2

1. Write a caption for the figure in your own words. What is being displayed? What does it reveal?
NIRC2-Pol images of AB Aur in total intensity, $Q_{\phi}$, and $U_{\phi}$ are shown.

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
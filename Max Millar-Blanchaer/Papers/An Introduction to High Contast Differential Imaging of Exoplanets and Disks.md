## 2/21/26

**near infrared (NI)** - 806-3450 nm wavelength light

**high contast imaging** - technique to isolate light from faints and disks against stars
- best technique to characterize planets

**contrast** - ratio of the brightness between a source (like a planet or disk) and its host star
- **high contast** - when the ratio is small, or the source is much fainter than the star
- **low contrast** - when the ratio is high, or the source is brighter relative to the star
**throughput** - ratio of an object's injected to recovered brightness
- computed with the brightness of the peak pixel before and after PSF subtraction

The brightness of planets depends on mass and age.
- directly imaged exoplanet brightness can be truned to a mass estimate under the assumptions of stellar age and the planetary formation pathway

**cold start** - gradual assembly of solid material in a circumstellar disk

**hot start** -  rapid gravitational collapse of material
- creates high masses and wide separations
## Technologies

**Strehl ratio (SR)** - ratio of a star's observed peak intensity to its theoretical diffraction-limited peak intensity

**adaptive optics (AO)** - a technology used to enhance the performance of optical systems by reducing wavefront distortions in real-time, primarily correcting for atmospheric turbulence in ground-based telescopes to achieve near-diffraction-limit imaging
- uses **deformable mirrors (DM)** with magnetic actuators in real time to counter atmospheric distortion of light
- **extreme adaptive optics (ExAO)** - achieve SR's of 80-90% in NI, but only 10-30% in optical

**quasi-static speckles** - created by imperfect wavefront corrections in AO
- can mimic planets

**coronagraphy** - uses physical optics inside an instrument to supress direct and diffracted starlight from reaching the detector
## High Contrast Image Anatomy

**point spread function (PSF)** - describes the light intensity across an image plane of a point source
- creates an **airy pattern** of ripples when coming through a telescope aperture
- optics create an analogue FFT of incoming bench function to create radial ripple pattern

**spot of Arago** - bright point in the middle of the coronographic mask from Fresnel diffraction

**optical abberations** - deviations in the airy pattern

**speckles** - uncorrected instrumental abberations that blend into a diffuse halo with atmospheric changes

**control region** - boundary between sensed wavefron and unsensed wavefront

**wind artifacts** - creates elongation in speckle pattern in the direction of wind

**satellite spots** - injected artifacts at known brightness locations relative to the host star using mirror deformations to calculate through and X-shape exactly where the star is

**instrument throughput** - fraction of light entering the aperture at a certain wavelength that makes it to the detector
## Differential Imaging Techniques

**self-subtraction** - subtracting planet light from images by mistake

**polarimetric differential imaging (PDI)** - selecting for certain polarizations to obtain the light from one source
- scattered light off a disk is polarized while direct starlight is not
- electric field vector is aligned orthogonal to the line of sight of the disk and the distance from the grain to the star
- done by a **Wollaston prism**

**referencial differential imaging (RDI)** - subtracting other star images from the science target
- have large reference star libraries
- use stars in similar parts of the sky with similar colors and instrument properties

**angular differential imaging (ADI)** - using different rotations of the target in the sky to subtract out background and add together planet or disk light

**spectral differential imaging (SDI)** - uses different wavelengths where planets are dimmer to construct a PSF that avoids self-subtraction
- **Integral Field Spectrographs (IFS)** - simultaneously images multiple wavelengths
- **spaxel** - spectral pixel in the image plane with multi-wavelength information
## Image Proccessing 

**unsharp masking** - convolving the image with a gaussian (gaussian blur) and then subtracting that from the original image

**principal component analysis (PCA)** - using orthogonal vectors to show all the variance in a clump of data plotted with different characteristics
- **principle component axis** - axis through variation of the data
- first few PCA's represent large structures like core and halo, and the others represent speckles

**Karhunen Loeve image proccessing (KLIP)** - images are converted to 1-D column vectors and correlated with others in a time sequence using principal component analysis

**Locally Optimized Combinations of Images (LOCI)** - computes least-squares PSF fit to the target image using many reference images
- template: designed for SDI imaging, where a planet spectrum is specified to limit self-subtraction
- adaptive: subtracting teh radial profile of the star
## Analysis

**Signal to noise** is calculated through standard deviation of post-proccessed images computed in small concentric rings going outward from the star.
- Signal 5x above noise is considered robust.

Questions for Analysis
1. Is throughput corrected?
2. What factor has the noise level been multiplied?
3. Has the noise level been corrected to fit around the star?
4. How azimuthally symmetric is the post-processed image?

**False Positives**
- background objects
- disk features
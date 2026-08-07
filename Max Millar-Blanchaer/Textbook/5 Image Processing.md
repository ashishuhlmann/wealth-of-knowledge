## 3/27/26

Pixel values are proportional to the number of electrons stored in each pixel and the number of incident photons.

Pixel values must be **color mapped** to a grayscale.
- **negative image** - reverse grayscale map
- **false color** - artificial color mapping
- **true color** - real object color to create and **RGB** image

RGB images can be created by adding together B, V, and R-band images.
## Image Arithmetic

Let a digital image $S$ be $N_{x}\times N_{y}$ pixels in size. All elementary mathematical operations are element-wise operations, and images must be of same dimension to do them.
### CCD Data Correction
$$
R=E\cdot S+B
$$
- $S$ is the underlying perfect image
- $E$ is the efficiency factor for each pixel
- $B$ is background noise and added signal.

**bias (zero) frame** - frame taken from a cleared CCD with zero exposure time
- typically, about ten bias frames are averaged together, which gives a good estimate of the background
- some CCD's will **overscan** horizontally after the last pixel has been read out to create an extended bias portion of the image

**dark frame** - frame taken from a cleared CCD with no light exposure for some time
- exposure times are usually equal to or longer than image times

**Master dark frames** are created by subtracting bias frames from a sample of dark frames.
$$
D=\text{median}(\frac{d_{1}-Z}{t_{d}^{1}},\frac{d_{2}-Z}{t_{d}^{2}},...,\frac{d_{n}-Z}{t_{d}^{n}})
$$
- $d_{i}$ is the dark frame sample
- $Z$ is the master bias frame
- $t_{d}^{i}$ is the exposure time

**flat-field image** - frame taken with uniform illumination
$$
E=(R-B)/S
$$
- $S$ is the perfect image that can be approximated by the median of $R-B$.

Suppose we have $n$ raw flats $f_{i}$ with corresponding exposures $t_{i}$. We also took our master dark frame $D$ and our master bias $B$. 
1. Subtract the background from each raw flat.
$$
F_{i}=f_{i}-Dt_{i}-Z
$$
2. Compute the media pixel value $\tilde{F_{i}}$ of each flat image $F_{i}$.
3. Compute the efficiency.
$$
E=\text{median}(\frac{F_{1}}{\tilde{F_{1}}},\frac{F_{2}}{\tilde{F_{2}}},...,\frac{F_{n}}{\tilde{F_{n}}})
$$
## Processing Image Data
$$
S_{i}=\frac{R_{i}-Dt_{i}-Z}{E}
$$
- multiplying $S_{i}$ by the CCD gain will finally give the number of **photoelectrons** for each pixel 
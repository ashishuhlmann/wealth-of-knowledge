## 3/26/26
## Measurement

**charge coupled device (CCD)** - two-dimensional array of photosensitive cells or **pixels**
- pixels are 5-20 micrometers in size, with detectors having several megapixels
- each pixel is a **metal-oxide-semiconducter (MOS)** capacitor
- the maximum number of electrons that can be stored in a pixel is called the **full-well capacity**, between 10,000 and 500,000 electrons
- CCD's typically have a linear response to the number of incident photons until the pixel saturates to full-well capacity

1. Open the shutter for a desired exposure time.
2. Shift all the parallel registers up by one row, and shift the top row into the **serial register**.
3. Shift the serial register charges to the right, and the right-most pixel into the **output node**.
4. Amplify and read the output node charge.
5. Convert the charge to a digital number.
6. Store all the pixel values into an array.

**parallel register** - column of pixels
- **serial register** - special row added to shift all the charge up by one register

**output node** - MOS capacitor to dumb pixel charge into for reading
- charge is converted by an **analog-to-digital converter (ADC)**

**blooming** - charge from one pixel exceeding the full-well capacity and spilling into other pixels
- **channel stops** prevent charge from moving between rows, so blooming only happens along columns

**charge-transfer-efficiency (CTE)** - fraction of electrons that move from on pixel to the next durign readout

**gain** - number of electrons that correspond to one **analog to digital unit (ADU)**

**electronic bias** - pixel 
## Dark Current

**dark current** - thermal agitation of electrons into each pixel
$$
\dot{n}_{D}=AT^{\frac{3}{2}}\exp{(\frac{-E_{g}}{2kT})}
$$
- $A$ is a constant.
- $E_{g}$ is the **bandgap energy** of the semiconductor.

Dark current can be essentially eliminated by cooling CCD's to -100°C.
## [[5 Image Processing]]
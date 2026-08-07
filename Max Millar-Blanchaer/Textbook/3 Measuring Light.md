## 3/25/26
## Flux

**flux** - amount of energy crossing through a certain area per unit of time

**luminosity** - power output

A star's flux measured a distance $d$ away is given by the **inverse square law**
$$
F=\frac{L}{4\pi d^{2}}
$$
- $L$ is the star's luminosity

Power, or energy per time is simply $P=AF$.

**bolumetric flux** ($F_{bol}$) - ideal flux measured across every wavelength of light

**bolumetric luminosity** ($L_{bol}$) - power output across every wavelength of light

**monochromatic flux (spectral irradiance)** ($F_{\lambda}$) - flux per unit wavelength
- integrating monochromatic flux gives the entire bolometric flux
$$
F_{bol}=\int_{0}^{\infty}F_{\lambda}d\lambda=\int_{0}^{\infty}F_{\nu}d\nu
$$
- $F_{\nu}$ can be measured in Janskies

Different detectors are sensitive to different kinds of light varying with wavelength. The flux measured by a telescope is
$$
F=\int_{0}^{\infty}R(\lambda)F_{\lambda}d\lambda
$$
- $R(\lambda)$ is the **response function**, specifying the fraction of the flux of wavelength $\lambda$ registered by the detector-telescope system.
- Multiplying by the telescope's aperture gives the power measured by the detector-telescope system.

The response function of an optical system is
$$
R(\lambda)=T_{0}E(\lambda)\phi(\lambda)
$$
- $T_{0}$ is the reflectivity and transmitivity of the system.
- $E(\lambda)$ is the **quantum efficiency** at detecting light at a certain wavelength $\lambda$, or fraction of photons actually detected.
- $\phi(\lambda)$ is the tramsitivity of the filter or **filter function**

**UBVRI system** - standard response functions for tuning every telescope-detector system

**color index** - difference between magnitudes in two different band passes
$$
B-V=-2.5\log{(\frac{F_{B}}{F_{V}})}+C_{B}-C_{V}=M_{B}-M_{V}
$$
## Magnitude

Magnitude is based on the Greek astronomy Hipparchus of Nicea in the second century BC.
- He classified magnitude one stars as the brightest in the sky and magnitude six stars as the faintest in the sky.
- Five magnitudes corresponds to a factor of *exactly* 100 in flux.

The magnitude $m$ is defined as
$$
m=-2.5\log{(F)+C}
$$
- $C=-2.5\log{(F_{0})}$ is the **zero point** of the magnitude system, where $F_{0}$ is the flux of an $m=0$ star.
- The factor of 2.5 is really just an approximation of the *fifth root* of 100, from the definition above

In practice, magnitude is measured in comparison with known stars
$$
m_{1}-m_{2}=-2.5\log{(\frac{F_{1}}{F_{2}})}
$$
- $F_{1}$ and $F_{2}$ are the fluxes of stars of magnitudes $m_{1}$ and $m_{2}$, respectively.

**absolute magnitude** - the **aparent magnitude** of a source viewed from 10 parsecs away
$$
M=-2.5\log{(L)}+C'
$$
To calculate the distance $r$ to a source, we can compare its absolute and aparent magnitudes through the **distance modulus**
$$
\mu\equiv m-M=5\log{(r)}-5
$$
### UBVRI Magnitude

Magnitudes for each band are designated by the capital letter
$$
U=-2.5\log{(F_{U})}+C_{U}
$$
- $C_{U}$ is the U-band zero point.
$$
F_{U}=\int_{0}^{\infty}R_{U}(\lambda)F_{\lambda}d\lambda
$$
## Counting Photons

The photon count rate is
$$
\dot{n}=A\int_{0}^{\infty}R_{p}(\lambda)\dot{n}_{\lambda}d\lambda
$$
- $A$ is the aperture.
- $R_{p}(\lambda)$ is the **photon response function**.
- $\dot{n}_{\lambda}$ is the **monochromatic photon flux**, or the monochromatic flux divided by the energy of a single photon
$$
\dot{n}_{\lambda}=\frac{F_{\lambda}}{hc/\lambda}
$$
### Uncertainty

Each measurement of a star's photons is drawn from a **Poisson distribution**. The uncertainty in the number $n$ photons measured is $\delta n=\sqrt{n}$. The **signal-to-noise ratio** is
$$
\text{SNR}=\frac{n}{\delta n}
$$
If detector noise $\sigma_{det}$ isn't correlated with counting noise, then
$$
\delta n=\sqrt{n+\sigma_{det}^{2}}
$$
## [[4 Charge Coupled Devices]]
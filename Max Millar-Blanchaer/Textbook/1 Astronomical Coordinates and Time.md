## 3/7/26

## Spherical Coordinates

**fundamental plane** - divides sphere in two hemisphers 
- traditionally, it is the $xy$-plane

**fundamental direction** - direction of one of the axes

**directions of increasing angle**
-  $\theta$ is the angle from the positive $z$-axis
- $\phi$ is the angle in the $xy$-plane from the positive $x$-axis

**celestial sphere** - spherical coordiante system around the Earth
## Altitude-Azimith

The origin is taken to be the observer, and the fundamental plane is the tangent plane to the surface of the Earth. The fundamental direction is due north.
- A position in the sky is an **altitude** angle from the horizon and an **azimuth** angle from the north direction.

**zenith** - point on the celestial sphere directly above the observer
- **zenith distance** - angle of a point on the celestial sphere from the upward or $z$-axis

**nadir** - point on the celestial sphere directly under the observer

**local meridian** - arc on the celestial sphere from the point at due south to the point at due north, passing through the zenith

**solar day** - period of successive transits on the Sun through the celestial sphere, or 24 hours

**sidereal day** - period of successsive transits of background stars through the celestial sphere, or 23 hours and 56 minutes

**ecliptic** - apparent path of the Sun along the celstial sphere

**zodiacal constellations** - twelve constellations along the ecliptic
## Equatorial Coordinates

The origin is taken to be the center of the Earth. The fundamental plane slices through the Earth's equator and defines the **celestial equator**. The Earth's poles are aligned with the **north** and **south** **celestial poles** (NCP and SCP). The fundamental direction $\boldsymbol{\gamma}$ points toward the **First Point of Aries**. It is the point of intersection of the ecliptic and the celestial equator at the September **equinox**.
- **right ascension** ($\alpha$) - angle in from the fundamental direction measured in hours, minutes, and seconds
- **declination** ($\delta$) - angle measured from the celestial equator
- **equinox** - time when the path of the Sun crosses the celestial equator (September 22 and March 20)
- **June Solstice** - northern-most excursion of the Sun from the celestial equator
- **December Solstice** - sourthern-most excursion of the Sun from the celestial equator
- **meridian plane** - plane containing the NCP, SCP, and the zenith
### Angular Separation

The angular separation $\beta$ in spherical coordinates between two points $A=(\alpha_{A},\delta_{A})$ and $B=(\alpha_{B},\delta_{B})$ for sufficiental small angles $\Delta\delta$ and $\Delta\alpha$ is
$$
\beta^{2}=\Delta\delta^{2}+\cos^{2}{(\frac{\delta_{A}+\delta_{B}}{2})}\Delta\alpha^{2}
$$
## Conversions

**latitude** - angle between the NCP and the zenith

**hour angle (HA)** - angle between the meridian plane and the plane containing the SCP, target star, and NCP measured in hours, minutes, and seconds from (-12 hours to +12 hours)
$$
H_{A}=\alpha_{M}-\alpha
$$
-  $\alpha_{M}$ is the **local siderial time**
- all points east of the local meridian have negative HA
- all points west of the local meridian have positive HA

**[local siderial time (LST)](https://www.localsiderealtime.com/)** - right ascension of the local meridian
$$
\alpha_{M}\approx\frac{n}{360\text{d}}(24\text{h})
$$
where $n$ is the number of days since the September 22nd equinox.

To convert between coordinate systems
$$
\begin{align}
\sin{(h)}&=\sin{(\delta)}\sin{(\phi)}+\cos{(\delta)}\cos{(\alpha_{M})}\cos{(\phi)} \\
\cos{(h)}\sin{(A)}&=\cos{(\delta)}\sin{(\alpha_{M})} \\
\end{align}
$$
An object with a delcination such that its altitude is never negative at a given latitude is **circumpolar** and visible all year.
## Precession and Nutation

**precession** - slow movement of the Earth's axis of rotation around an axis perpendicular to the ecliptic
- It takes around 26,000 years for the axis of rotation to make one complete cycle around the ecliptic pole.
- The first point of Aries also precesses.

**obliquity** - The angle between the ecliptic pole and the celetial pole is around 23.4 degrees.

**nutation** - short term small oscillation around the precessional path of the celestial pole

**epoch** - date of coordinates for an observation
- **J2000 epoch** - Julian date measured after 12h GMT on 1st January, 2000

The new coordinates of a target $(\alpha,\delta)$ $N$ years after a reference observation at $(\alpha_{0},\delta_{0})$ are roughly
$$
\begin{align}
\alpha&=\alpha_{0}+(m+n\sin{(\alpha_{0})}\tan{(\delta_{0})})N \\
\delta&=\delta_{0}+(n\cos{(\alpha_{0})})N \\
\end{align}
$$
where $m$, $n$, and $n'$ are constants
## Telescope Mounts

**altitude-azimuth** - rotates around a vertical axis and upwards from the plane

**equatorial mount** - aligned parallel to the Earth's rotation axis and rotates along with right ascention and declination
## Galatic Coordinates

The origin is taken to be the sun. The fundamental is the plane of the galaxy.
- **galatic latitude** ($b$) - angle above the galatic plane to an object in degrees
- **galatic longitude** ($\ell$) is the angle in the galatic plane from the center of the galaxy in degrees
## Ecliptic Coordinates

The origin is taken to be the Earth, but the fundamental plane is instead coincident with the ecliptic plane. The fundamental direction is the First Point in Aries. It is a right handed coordinate system with angles measured in degrees.
- useful for describing solar system objects
## Astronomical Time

**second** - 9,192,631,770 periods of radition originating between two energy levels of the cesium-133 atom

**International Atomic Time TAI** - exact time
- accurate to less than a fraction of a second in over a million years
- about 35 seconds out of sync with the sun

**Coordinated Universal Time (UTC)** - time system based on TAI with leap seconds to make up for the sun
- time zones are reference to UTC

**apparent solar time** - based on the position of the Sun in the sky
$$
T_{AS}=H_{A}+12\text{hr}
$$
- $H_{A}$ is the hour angle of the Sun

**mean solar time** - defined by a fictional Sun that moves at the mean rate of the real Sun

**equation of time (EOT)** - difference between the mean solar time and apparent solar time
$$
E_{OT}=T_{MS}-T_{AS}
$$
### Julian Date

**Julian day numbers (JD)** - decimal number of days since 12:00 PM UTC on January 1st, 4713 bc.

**modified Julian day (MJD)** - JD minus 2,400,000.5
## [[2 Telescopes]]
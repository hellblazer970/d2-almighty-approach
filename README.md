# d2-almighty-approach

This is the github repo containing the raw data for a trajectory of the Almighty from Mercury to Earth during Destiny 2's Season of the Worthy.

Planetary positions are provided from the NASA Jet Propulsion Laboratory's [DE405 Epheremis](https://en.wikipedia.org/wiki/Jet_Propulsion_Laboratory_Development_Ephemeris). Coordinate system is J2000, the same one the planetary positions are defined in.

Almighty's trajectory was computed by solving [Lambert's Problem](https://en.wikipedia.org/wiki/Lambert%27s_problem). The starting position was Mercury's orbital position at the start of Season of the Worthy (March 10, 2020) and the final position was Earth's orbital position at the end of Season of the Worthy (June 9, 2020).

The CSV file contains the data of:
* Date (Epheremis Time)
* Required Velocity Change to Prevent Almighty from hitting Earth and instead flying by at 1000 km altitude (kilometers per second)
* Almighty's Relative Distance from Earth (kilometers)
* Almighty's Relative Velocity to Earth (kilometers per second)
* Almighty's Trajectory Relative to the Sun in EME2000 Coordinates (kilometers & kilometers per second)
  * X 
  * Y
  * Z
  * DX
  * DY
  * DZ
* Mercury's Orbital Position Relative to the Sun in EME2000 Cooordinates (kilometers & kilometers per second)
  * X 
  * Y
  * Z
  * DX
  * DY
  * DZ
* Earth's Orbital Position Relative to the Sun in EME2000 Cooordinates (kilometers & kilometers per second)
  * X 
  * Y
  * Z
  * DX
  * DY
  * DZ



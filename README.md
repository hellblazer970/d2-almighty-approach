# d2-almighty-approach

This is the github repo containing the raw data for a trajectory of the Almighty from Mercury to Earth during Destiny 2's Season of the Worthy.

## Website GUI

I made a very basic interface to see the Almighty's current position using [plotly](https://plotly.com/javascript/). You can see it here:

https://hellblazer970.github.io/d2-almighty-approach/almighty.html

I am not very good at visiualizations. Someone else can probably do a better job than me, which is why I make this data available.

## Planetary Positions and Trajectory Calculations

Planetary positions are provided from the NASA Jet Propulsion Laboratory's [DE405 Epheremis](https://en.wikipedia.org/wiki/Jet_Propulsion_Laboratory_Development_Ephemeris). Coordinate system is J2000. There are several web-based interfaces to access this data, such as JPL's [Horizons](https://ssd.jpl.nasa.gov/horizons.cgi) or JPL's [WebGeoCalc](https://naif.jpl.nasa.gov/naif/webgeocalc.html). Or, for those who program, you can use the Planetary Data System's [SPICE](https://naif.jpl.nasa.gov/naif/aboutspice.html) API. 

Almighty's trajectory was computed by solving [Lambert's Problem](https://en.wikipedia.org/wiki/Lambert%27s_problem). The starting position was Mercury's orbital position at the start of Season of the Worthy (March 10, 2020) and the final position was Earth's orbital position at the end of Season of the Worthy (June 9, 2020).

A very rudementary calculation was made to compute the required maneuver (velocity change) to divert away from hitting Earth and instead cause the Almighty to miss Earth by 1000 km altitude. This was computed by again solving Lambert's problem between the Almighty's current position at a given date (using [two-body propagation](https://en.wikipedia.org/wiki/Two-body_problem)) and an adjusted coordinate 1000 km away from Earth at the end of the Season of the Worthy (June 9). I don't really trust the answer to this as the Almighty gets very close to Earth (in the last few days) because I am not accounting for [third body effects](https://en.wikipedia.org/wiki/Three-body_problem).

## Data file format and units

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



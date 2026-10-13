# Methodology

## Measurement strategy

Controlled one-dimensional laser position scans were used to measure the response of individual detector readout elements as a function of known illumination position. The detector remained fixed while the laser was translated with motorised stages.

The acquisition chain combined a PiLAS pulsed laser, FastIC front-end electronics, picoTDC timing readout and MuDAQ-based triggered acquisition. The principal observables used in the analysis were hit count, time of arrival (ToA), time over threshold (ToT) and occupancy.

## Independent laser characterisation

The transverse laser profile was measured with a CCD camera before detector scans were interpreted because the finite illumination width contributes directly to the measured position-scan profile.

Two illumination conditions were used in the principal analyses:

- **LAPPD:** micro-focused beam; horizontal effective width = **0.900 mm**
- **HRPPD:** collimated beam; horizontal top-hat width = **5.173 mm**

The focused spot was visibly structured rather than perfectly uniform. The horizontal profile was more stable than the vertical profile under changes of profile position and fit range, so the horizontal measurement was used as the finite-width input to the principal LAPPD analysis.

## Spatial-response model

A finite detector readout element is represented by a top-hat response. The finite laser illumination contributes a second measured finite-width term. A Gaussian term is then used to describe the remaining effective broadening.

**Response model**

R(x) = A · [T_readout ⊗ T_laser ⊗ G(σ_eff)] + B

The signal normalisation, response centre, background and effective Gaussian broadening are fitted. The readout and laser widths are fixed from detector geometry and independent beam measurements.

## Interpretation of σ_eff

The fitted Gaussian term is deliberately treated as an **effective response parameter**. It can contain contributions from charge-cloud transport, capacitive or direct readout, electronic threshold effects, and departures of the real laser profile from the idealised model.

It should therefore not be identified directly with the intrinsic MCP electron-cloud width without additional measurements.

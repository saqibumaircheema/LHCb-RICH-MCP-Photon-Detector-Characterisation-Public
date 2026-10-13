# Methodology

## Measurement strategy

The project used controlled one-dimensional laser position scans to measure the response of individual detector readout elements as a function of known illumination position. The detector remained fixed while the laser was moved with motorised translation stages.

The acquisition chain combined a PiLAS pulsed laser, FastIC front-end electronics, picoTDC timing readout and MuDAQ-based triggered acquisition. The principal observables used in the analysis were hit count, time of arrival (ToA), time over threshold (ToT) and occupancy.

## Independent laser characterisation

The transverse laser profile was measured with a CCD camera before interpreting detector scans. This was necessary because the finite illumination width contributes directly to the measured position-scan profile.

Two illumination regimes were used:

- **micro-focused beam for LAPPD scans:** horizontal effective top-hat width (W_x=0.900) mm;
- **collimated beam for HRPPD scans:** horizontal top-hat width (W_x=5.173) mm.

The focused beam was visibly structured rather than perfectly uniform. The horizontal profile was more stable than the vertical profile under changes of profile position and fit range, so the horizontal result was used as the finite-width input to the principal LAPPD analysis.

## Spatial-response model

A finite detector readout element is represented by a top-hat response. The finite laser illumination is represented by a second measured finite-width term. Their convolution describes the geometrical overlap expected during a position scan. A Gaussian term is then used to represent the remaining effective broadening:

[
R(x)=A,[T_{m readout}(x)otimes T_{m laser}(x)otimes G(x;sigma_{m eff})]+B.
]

The fit parameters are the signal normalisation, response centre, background and effective Gaussian broadening. The readout and laser widths are fixed from detector geometry and independent beam measurements.

## Interpretation of (sigma_{mathrm{eff}})

The fitted Gaussian term is deliberately described as an effective response parameter. It can include contributions from charge-cloud transport, readout coupling, electronic threshold effects and departures of the real laser profile from the idealised model. It should therefore not be identified directly with an intrinsic MCP electron-cloud width without additional measurements.

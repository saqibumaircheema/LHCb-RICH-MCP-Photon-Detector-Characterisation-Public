# MCP-Based Photon Detector Characterisation for the LHCb RICH Upgrade II

MSc research project in Particle and Nuclear Physics at the University of Edinburgh.

**Saqib Umair**  
Supervisors: Dr Silvia Gambetta and Dr Dan Foulds-Holt  
Dissertation submitted: 21 August 2026

This repository presents selected results from my dissertation on the spatial response of microchannel-plate photon detectors considered for the LHCb RICH Upgrade II. The work compares a Gen-II Large Area Picosecond Photodetector (LAPPD) and a High-Rate Picosecond Photodetector (HRPPD) using controlled laser position scans, independently measured laser profiles and convolution-based response models.

The central question was practical: **how do detector geometry, readout architecture and operating conditions shape the measured spatial response?**

## Experimental approach

The detector was held fixed while a pulsed PiLAS laser was translated across the active area with motorised stages. Signals were processed with FastIC front-end electronics and picoTDC timing readout, with MuDAQ used for triggered acquisition. CCD measurements were used to characterise the transverse laser profile before detector scans were interpreted.

<p align="center">
  <img src="figures/experimental-apparatus.png" alt="Experimental apparatus and data-acquisition chain" width="95%">
</p>

The analysis separates known finite-width contributions from the remaining measured broadening. The response model combines the laser profile, readout-element width and an additional Gaussian term:

[
R(x) = A,[T_{mathrm{readout}} otimes T_{mathrm{laser}} otimes G(sigma_{mathrm{eff}})] + B.
]

Here, (sigma_{mathrm{eff}}) is an **effective one-dimensional broadening parameter** under the tested conditions. It is not treated as a direct measurement of the intrinsic MCP electron-cloud width.

<p align="center">
  <img src="figures/spatial-response-model.png" alt="Top-hat and Gaussian convolution model" width="95%">
</p>

## Laser characterisation

The illumination profile was measured independently with a CCD camera. For the collimated configuration used in the HRPPD study, the horizontal top-hat width was

[
W_{mathrm{laser}} = 5.173;mathrm{mm}.
]

For the micro-focused configuration used in the LAPPD study, the more stable horizontal profile gave

[
W_{mathrm{laser}} = 0.900;mathrm{mm}.
]

<table>
<tr>
<td width="50%"><img src="figures/collimated-laser-x.png" alt="Collimated laser horizontal profile"></td>
<td width="50%"><img src="figures/focused-laser-x.png" alt="Focused laser horizontal profile"></td>
</tr>
<tr>
<td align="center"><b>Collimated illumination</b></td>
<td align="center"><b>Micro-focused illumination</b></td>
</tr>
</table>

## LAPPD spatial response and bias dependence

The LAPPD position scans used a 2.9 mm external pickup width and the measured 0.900 mm focused-laser width as fixed geometrical inputs. The common MCP1–MCP2 and MCP2–anode gap voltage was varied while the other principal bias settings were held fixed.

| Common gap setting | Fitted (sigma_{mathrm{eff}}) |
|---:|---:|
| 150 V | (4.541 pm 0.024) mm |
| 200 V | (4.781 pm 0.025) mm |
| 250 V | (5.254 pm 0.026) mm |

The fitted effective width increased by about **16%** from the low- to high-bias configuration.

<p align="center">
  <img src="figures/lappd-bias-fits.png" alt="LAPPD response at low nominal and high bias" width="100%">
</p>

<p align="center">
  <img src="figures/lappd-bias-dependence.png" alt="LAPPD effective spatial width versus common gap voltage" width="70%">
</p>

This trend is a measured property of the **complete tested bias configuration**. Because the MCP1–MCP2 and MCP2–anode gaps were varied together, the measurement does not isolate a single transport gap. The simple symmetric convolution also does not reproduce all shoulder and tail structure, so the fitted width is used as a comparative effective parameter rather than a complete detector model.

## HRPPD spatial response

The HRPPD channel-52 scan used a 3.0 mm pixel width and the independently measured 5.173 mm horizontal collimated-laser width. The fit gave

[
sigma_{mathrm{eff}} = 1.538 pm 0.003;mathrm{mm}.
]

<p align="center">
  <img src="figures/hrppd-spatial-response.png" alt="HRPPD channel 52 position scan" width="70%">
</p>

The finite laser and pixel widths are included explicitly in the model. The remaining Gaussian term therefore represents additional broadening required by the fit, but it can still contain contributions from detector transport, readout, threshold effects and imperfections in the idealised laser model.

The LAPPD and HRPPD values were obtained under different illumination and readout conditions, so they are **not presented as a direct ranking of intrinsic detector spatial resolution**.

## My contribution

For this MSc project I:

- performed the laser-profile characterisation and position-scan analysis;
- wrote the motorised translation-stage control used for the scans;
- developed and modified ROOT/C++ and Python analysis tools;
- constructed and tested convolution models for the measured spatial response;
- investigated LAPPD bias dependence, occupancy and timing-related checks;
- analysed the HRPPD position response and exploratory neighbouring-channel signal sharing.

## Technical scope

**Detector instrumentation:** LAPPD, HRPPD, MCP-PMT concepts, FastIC, picoTDC, MuDAQ, PiLAS laser, CCD beam profiling, motorised translation stages  
**Analysis:** ROOT/C++, Python, NumPy, SciPy, Matplotlib, uproot, nonlinear fitting, detector response modelling, ToA/ToT observables, uncertainty-aware interpretation

## Repository scope

This public repository contains selected figures, methodology and research conclusions. It intentionally does **not** contain raw detector data, internal collaboration software or the working analysis source code. Those materials are kept separate because of data provenance, collaborator contributions and redistribution constraints.

See [Methodology](docs/METHODOLOGY.md), [Results and limitations](docs/RESULTS_AND_LIMITATIONS.md), and [Data and attribution](docs/DATA_AND_ATTRIBUTION.md) for additional detail.

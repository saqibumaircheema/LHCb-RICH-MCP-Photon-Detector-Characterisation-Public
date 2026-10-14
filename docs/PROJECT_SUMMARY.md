# Research summary

This page summarises the MSc project without publishing the full dissertation.

## Project

**Characterisation of MCP-Based Photon Detectors for the LHCb RICH Upgrade II**

Saqib Umair  
MSc Particle and Nuclear Physics, University of Edinburgh  
Supervisors: Dr Silvia Gambetta and Dr Dan Foulds-Holt  
2026

## Research question

The project examined how the measured spatial response of microchannel-plate photon detectors is shaped by the detector, readout geometry, laser illumination and operating conditions.

Two detector systems were studied: a Gen-II LAPPD and an HRPPD. Controlled laser position scans measured response as a function of known illumination position. The laser profile was measured independently with a CCD camera so that its finite width could be included explicitly in the response model.

## Main results

**LAPPD, nominal bias:** sigma_eff = 4.781 +/- 0.025 mm

| Common gap voltage | sigma_eff |
|---:|---:|
| 150 V | 4.541 +/- 0.024 mm |
| 200 V | 4.781 +/- 0.025 mm |
| 250 V | 5.254 +/- 0.026 mm |

The fitted LAPPD width increased by approximately 16% from the low- to high-bias configuration. The MCP1-MCP2 and MCP2-anode gaps were varied together, so the measurement does not isolate which transport gap is responsible for the trend.

**HRPPD, channel 52:** sigma_eff = 1.538 +/- 0.003 mm

The HRPPD and LAPPD measurements used different illumination and readout configurations, so the fitted values are not presented as a direct ranking of intrinsic detector spatial resolution.

## Laser characterisation

Collimated beam used for HRPPD: W_x = 5.173 mm, sigma_x = 0.631 mm.

Micro-focused beam used for LAPPD: W_x = 0.900 mm, sigma_x = 0.07729 mm.

## My contribution

- laser-profile characterisation from CCD measurements;
- motorised translation-stage control for detector position scans;
- ROOT/C++ and Python position-scan analysis;
- convolution-based response fitting;
- LAPPD bias-dependence, occupancy and timing checks;
- HRPPD position-response analysis.

## Public repository scope

The full dissertation is not published here. The repository is limited to selected research outputs, methodology, results and figures that are appropriate for public release.
# Results and limitations

## LAPPD

At nominal bias:

**σ_eff = 4.781 ± 0.025 mm**

The common MCP1–MCP2 and MCP2–anode gap voltage was varied from 150 V to 250 V:

| Bias setting | Common gap voltage | σ_eff | χ² / ndf |
|---|---:|---:|---:|
| Low | 150 V | 4.541 ± 0.024 mm | 770.1 / 37 |
| Nominal | 200 V | 4.781 ± 0.025 mm | 934.5 / 37 |
| High | 250 V | 5.254 ± 0.026 mm | 1083.3 / 37 |

The effective width increased monotonically, corresponding to an increase of approximately **16%** from the low- to high-bias configuration.

### Limitation of the fit

The χ² / ndf values are large. The simple symmetric convolution captures the overall spatial width but does not reproduce all shoulder and tail structure, particularly at higher common gap bias.

The quoted σ_eff values are therefore used to compare the tested configurations; they are not presented as evidence that the model gives a complete microscopic description of the response.

### Limitation of the voltage scan

The MCP1–MCP2 and MCP2–anode gaps were changed simultaneously. The measurement therefore does not identify which gap is primarily responsible for the observed trend.

## HRPPD

For HRPPD channel 52, with a 3.0 mm pixel width and the measured 5.173 mm collimated-laser width included explicitly:

**σ_eff = 1.538 ± 0.003 mm**

The idealised model also gives a large χ² / ndf (1726 / 13). The result is therefore treated as an effective one-dimensional response parameter rather than as a direct intrinsic electron-cloud width.

## Comparing the two detector measurements

The LAPPD and HRPPD values were obtained under different conditions:

- LAPPD: micro-focused illumination and capacitive external pickup
- HRPPD: broader collimated illumination and direct pixelated anode

The comparison is useful for understanding the complete measured detector/readout configurations, but not for ranking intrinsic detector spatial resolution.

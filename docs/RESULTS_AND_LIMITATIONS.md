# Results and limitations

## LAPPD

At nominal bias, the fitted effective broadening was

[
sigma_{mathrm{eff}}=4.781pm0.025;mathrm{mm}.
]

A bias scan changed the common MCP1–MCP2 and MCP2–anode gap setting from 150 V to 250 V:

| Bias setting | Common gap voltage | (sigma_{mathrm{eff}}) | (chi^2/mathrm{ndf}) |
|---|---:|---:|---:|
| Low | 150 V | (4.541pm0.024) mm | 770.1 / 37 |
| Nominal | 200 V | (4.781pm0.025) mm | 934.5 / 37 |
| High | 250 V | (5.254pm0.026) mm | 1083.3 / 37 |

The effective width increased monotonically across the three configurations, corresponding to an increase of approximately 16% between the low- and high-bias settings.

The large (chi^2/mathrm{ndf}) values are important. The simple symmetric convolution captures the overall spatial width but not all shoulder and tail structure, particularly at higher common gap bias. The result is therefore a comparative trend in the tested configuration, not a claim that the model gives a complete microscopic description of the detector response.

The two transport gaps were changed simultaneously. The measurement therefore does not determine which gap is primarily responsible for the observed trend.

## HRPPD

For HRPPD channel 52, with a 3.0 mm pixel width and the measured 5.173 mm collimated-laser width included explicitly, the fitted additional Gaussian term was

[
sigma_{mathrm{eff}}=1.538pm0.003;mathrm{mm}.
]

The fit quality was also poor for an idealised model ((chi^2/mathrm{ndf}=1726/13)). The fitted width is therefore treated as an effective one-dimensional response parameter rather than as a direct measurement of the intrinsic electron-cloud width.

## LAPPD versus HRPPD

The numerical values should not be compared as if both detectors were measured under identical conditions. The LAPPD measurement used micro-focused illumination and capacitive external pickup, whereas the HRPPD measurement used a broader collimated beam and direct pixelated readout. The comparison is useful for understanding the complete detector/readout configurations, but not for ranking intrinsic detector spatial resolution.

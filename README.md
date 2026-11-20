# QRamsey

Research notebooks accompanying Brani Vidakovic's *Sensitivity as Scale: Multiscale Inference for Latent Phase Drift from Ordered Ramsey Records*. These examples illustrate how a Ramsey circuit encodes detuning, how multiple waits and quadratures help resolve aliases, and how a sequential estimate can inform a delayed correction.

## Notebooks

| Notebook | What it reproduces |
| --- | --- |
| [Ramsey inference](notebooks/Ramsey_Inference_Qiskit2.ipynb) | Exact binomial likelihood, calibration, detuning inference, and latency-aware prediction. The saved run uses the analytic binomial simulator. |
| [Qiskit Experiments Ramsey protocols](notebooks/Ramsey_IBM_Protocols_Qiskit2.ipynb) | Aer runs of T2Ramsey and RamseyXY, signed detuning recovery, frequency aliases, and sequential tracking. Its final figure supplies the circuit-level tracking illustration in the paper. |
| [Aer feedback](notebooks/Ramsey_Aer_Feedback.ipynb) | A synthetic phase trajectory, Bayesian monitoring, and a simulated phase correction. |

## Run locally

Create a Python 3.11 environment and install the dependencies.

```bash
python -m pip install -r requirements.txt
jupyter lab
```

Open a notebook and run its cells in order. The examples use synthetic observations and run locally without access to an IBM Quantum device. The archive analyses and the paper's main multiscale Monte Carlo require separate reproduction scripts.

## External data

The trapped-ion Ramsey observations analyzed in the paper are from Timothy Proctor et al., *Detecting and tracking drift in quantum information processors*, Nature Communications **11**, 5396 (2020). Obtain the experimental files and the original analysis code from the authors' archive. Keep downloaded files under `data/raw/` locally.

- [Original Proctor et al. trapped-ion data and analysis code](https://doi.org/10.5281/zenodo.4033077)
- [Proctor et al. article](https://doi.org/10.1038/s41467-020-19074-4)

## Citation

Cite the accompanying manuscript for the QRamsey methods and cite the original paper and archive for analyses using the trapped-ion observations.

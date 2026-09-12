<h1 align="center">DDPR</h1>

<h3 align="center">Dominant Degradation Planning with Latent Residual-Guided Adaptive Editing for All-in-One Image Restoration</h3>

<p align="center">
  Qi Wang<sup>1</sup>, Xian Hu<sup>2</sup>, Hainuo Wang<sup>3</sup>, Wei Deng<sup>2,*</sup>, Chengli Peng<sup>1,*</sup>
</p>

<p align="center">
  <sup>1</sup> School of Geosciences and Info-Physics, Central South University, Changsha, China<br>
  <sup>2</sup> Xiaomi Corporation, Wuhan, China<br>
  <sup>3</sup> School of Computer Science and Technology, Tianjin University, Tianjin, China
</p>

<p align="center"><sup>*</sup> Corresponding authors</p>

<p align="center">
  <a href="https://wangq6588-a11y.github.io/DDPR/"><strong>Project Page</strong></a>
  &nbsp;&middot;&nbsp; Paper: Forthcoming
  &nbsp;&middot;&nbsp; Code: Coming soon
  &nbsp;&middot;&nbsp; Dataset: Soon
</p>

Official project repository for **DDPR**, a framework for progressive, region-adaptive All-in-One image restoration. The project page is available now; code and dataset releases are forthcoming.

## Overview

Real-world images often contain multiple degradations that interact with one another. DDPR identifies the current dominant degradation, restores the image, and reassesses what remains. Within each restoration step, it adapts the strength of editing across regions to balance content preservation and degradation removal.

[![Overview of DDPR: dominant degradation planning and latent residual-guided adaptive image restoration.](docs/assets/overview.webp)](docs/assets/overview.webp)

The framework brings together three components:

- **Dominant Degradation Planner:** selects the next restoration objective and reassesses the updated image after each step.
- **Degradation-Aware Latent Residual Assessor (DLRA):** learns from VAE latent residuals to predict a regional degradation gate.
- **Degradation-Gated Dual-Branch LoRA (DGDB-LoRA):** uses the gate to balance content-preservation and degradation-restoration branches in a shared restoration model.

## Results and benchmarks

DDPR is evaluated across three complementary restoration settings:

| Benchmark | Setting |
| --- | --- |
| **RealComp-Bench** | Real-world compound degradations; 221 images curated in this work. |
| **AgenticIR Benchmark** | Synthetic compound degradations. |
| **RealIR-Bench** | Real-world single degradations. |

Explore **interactive input/result comparisons, restoration trajectories, and quantitative results** on the [project page](https://wangq6588-a11y.github.io/DDPR/).

## Release status

| Resource | Status |
| --- | --- |
| [Project page](https://wangq6588-a11y.github.io/DDPR/) | Available |
| Paper | Forthcoming; the paper link and citation will be added when available. |
| Code | Not yet released; code will be published in this repository. |
| RealComp-Bench dataset | Coming soon; the download link will be added when available. |

The repository currently contains this README and the static project page in [`docs/`](docs/), served through GitHub Pages. Setup and usage instructions will accompany the code release.

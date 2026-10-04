# The Evolution of Command-and-Control (C2) Traffic and NDR Blind Spots

> [!IMPORTANT]
> The primary research repository is [ByGh00st/c2-timing-ndr-blindspots](https://github.com/ByGh00st/c2-timing-ndr-blindspots). It contains the full technical README, mathematical explanations, architecture diagram, engineering artifacts, and [finalized v1.0 release](https://github.com/ByGh00st/c2-timing-ndr-blindspots/releases/tag/v1.0). Use that repository for the research and future updates. This repository retains a publication copy.

### Advanced Blue Team Tactics Against Shaped Timing Dynamics

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23141650.svg)](https://doi.org/10.5281/zenodo.23141650)
[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![Version: v1.0](https://img.shields.io/badge/version-v1.0-blue.svg)](https://github.com/ByGh00st/c2-ndr-blind-spots/releases/tag/v1.0)
[![Languages: Turkish | English](https://img.shields.io/badge/languages-Turkish%20%7C%20English-blue.svg)](#publications)

[Türkçe README](README_TR.md)

## Overview

This defensive cybersecurity research publication examines the evolution of command-and-control (C2) traffic timing and the limitations of network detection and response (NDR) based on flow observations alone. It connects statistical traffic analysis with cross-layer telemetry, detection engineering, and detector validation.

The research covers event-time jitter versus interval jitter, Inter-Arrival Time (IAT) analysis, periodicity and spectral analysis, self-similarity, Long-Range Dependence (LRD), the Hurst exponent, heavy-tailed traffic, and the Hill estimator. It examines how endpoint, process, session, and identity context can inform the interpretation of network observations, with ETW and eBPF defensive telemetry and a T1-T20 detection/correlation catalog.

Sigma, KQL, SPL, and eBPF-oriented detection engineering are discussed alongside baseline calibration, false-positive management, and validation. The PDFs are the authoritative technical source; this repository provides publication access, citation metadata, and integrity information.

## Core Research Areas

- C2 timing models, IAT statistics, periodicity, and spectral analysis.
- Self-similarity, LRD, Hurst estimation, and heavy-tail diagnostics using the Hill estimator.
- Flow-level detection limitations and cross-layer correlation across processes, sessions, identities, and endpoint state.
- Defensive telemetry using ETW and eBPF.
- T1-T20 defensive detection/correlation concepts and Sigma, KQL, SPL, and eBPF-oriented detection engineering.
- Baseline calibration, false-positive management, and detector validation.

## Key Architectural Thesis

A network flow merely appearing “human-like” is not sufficient evidence of legitimacy. Detection should evaluate whether the process, session, identity, endpoint state, and network behavior producing that flow are mutually consistent.

This is an architectural position motivating contextual detection and validation, not an experimentally proven universal theorem.

## Mathematical Scope

- **Model A: event-time jitter** and its distinction from **Model B: interval jitter**.
- The distinction between an event train and a scalar IAT sequence when interpreting statistics and spectra.
- A lag-1 autocorrelation result under explicit assumptions, with its scope and limitations defined in the publication.
- Renewal spectrum analysis and its relationship to timing models.
- Self-similar/LRD traffic and Hurst exponent estimation.
- Heavy-tail diagnostics, including the Hill estimator and interpretation limits.

Mathematical results should be read with their stated assumptions. This overview does not reproduce operational procedures.

## Tactical Catalog

The publication contains **T1-T20 defensive detection and correlation concepts**. These connect statistical observations to contextual telemetry and detection engineering. Technical detail, assumptions, calibration requirements, and validation considerations remain in the PDFs.

## Publications

| Edition | Publication | Document ID |
| --- | --- | --- |
| English | [Technical Report EN v1.0](publications/ByGhost-C2-NDR-Technical-Report-EN-v1.0.pdf) | `SOC-NDR-MASTER-001-EN` |
| Turkish | [Technical Report TR v1.0](publications/ByGhost-C2-NDR-Technical-Report-TR-v1.0.pdf) | `SOC-NDR-MASTER-001` |

## Zenodo / DOI

- **Version DOI:** [10.5281/zenodo.23141650](https://doi.org/10.5281/zenodo.23141650) identifies v1.0 specifically.
- **Concept DOI:** [10.5281/zenodo.23141649](https://doi.org/10.5281/zenodo.23141649) resolves to the latest Zenodo version.

Use the version DOI when citing this edition.

## Citation

Erarslan, Oğulcan (ByGhost). (2026). *The Evolution of Command-and-Control (C2) Traffic and NDR Blind Spots: Advanced Blue Team Tactics Against Shaped Timing Dynamics*. Version 1.0. ByGhost Security. Zenodo. [https://doi.org/10.5281/zenodo.23141650](https://doi.org/10.5281/zenodo.23141650).

Machine-readable citation metadata is available in [CITATION.cff](CITATION.cff).

## Public-Release Scope

This publication focuses on defensive detection, measurement, telemetry, validation, and detection engineering. It does not disclose proprietary C2 implementation architecture, operational weaponization procedures, adversary traffic-generation code, deployment parameters, or evasion recipes.

## File Integrity

The SHA-256 digests below were calculated from the finalized source PDFs before copying. Both repository copies were verified to match their source files byte-for-byte; only the copy filenames were changed.

| Filename | SHA-256 |
| --- | --- |
| `ByGhost-C2-NDR-Technical-Report-EN-v1.0.pdf` | `96d8138312ca84f2cdfe905a64566aede2fdcc0de4d7a589dbdb8e471e27bc85` |
| `ByGhost-C2-NDR-Technical-Report-TR-v1.0.pdf` | `d1da8d191cdb5ff661a659c56aa13c7645bf5b2ce77af149c7b076d048ae4e2a` |

## License

The repository's publication material is distributed under [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)](https://creativecommons.org/licenses/by-nc-nd/4.0/), unless explicitly stated otherwise. See [LICENSE.md](LICENSE.md).

## Author

**Oğulcan (ByGhost) Erarslan**

Senior Solutions Architect | Cyber Security Specialist

ByGhost Security

- [Website](https://byghost.tr/)
- [GitHub](https://github.com/ByGh00st)
- [LinkedIn](https://linkedin.com/in/byghost-tr)

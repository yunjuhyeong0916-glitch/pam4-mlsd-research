<a id="page-top"></a>

<p align="right">
<a href="README.md" title="한국어 연구 소개 보기"><img src="assets/readme/nav-ko.svg" alt="한국어" width="87" height="30"></a>
</p>

# Juhyeong Yun | PAM4 MLSD Research (In Progress)

Kwangwoon University · Master's thesis research

This repository covers my **DS-SBM master’s thesis** and follow-up **DP-SMM journal research**. I design candidate selection and parallel processing for PAM4 detection, connecting model–RTL verification with RFSoC physical-channel evaluation.

<p>
<a href="projects/pam4-mlsd-thesis/README.md"><img src="assets/readme/status-thesis-en.svg" alt="Thesis · In progress" width="160" height="30"></a>
<a href="projects/dp-smm-journal/README.md"><img src="assets/readme/status-journal-en.svg" alt="Journal · In progress" width="166" height="30"></a>
</p>

## Master's Thesis | DS-SBM Design and RFSoC Verification (In Progress)

**Manuscript being finalized.** Two survivor branches per reduced state and segment metric-matrix composition form the DS-SBM detector. I verified operation on a **4-GS/s, 8-Gb/s PAM4** physical path using ZCU208, XM655 and an ISI board.

<a href="projects/pam4-mlsd-thesis/docs/implementation.md"><img src="projects/pam4-mlsd-thesis/assets/rfsoc_signal_path.png" alt="DS-SBM thesis transceiver path through DAC, physical channel and ADC" width="840"></a>

With an estimated total path loss of **about 41 dB at 2 GHz**, the reported BER is **< 10⁻⁷ for PRBS7** and **< 2×10⁻⁶ for PRBS15**. Detector-only resources decrease by **35.7% in LUTs and 22.5% in FFs** relative to RS-ACS.

[Thesis project](projects/pam4-mlsd-thesis/README.en.md) · [Detector architecture](projects/pam4-mlsd-thesis/docs/architecture.md) · [RFSoC implementation](projects/pam4-mlsd-thesis/docs/implementation.md) · [Measurements and resources](projects/pam4-mlsd-thesis/docs/validation.md)

## Journal Preparation | DP-SMM Design and Verification (In Progress)

DP-SMM retains two paths in each segment metric-matrix entry and rescores them using actual symbol histories. I verified agreement between the reference model and RTL and completed FPGA place-and-route. Board measurements are planned with **21-tap RX FFE + DP-SMM**.

**A patent application for DP-SMM is in preparation.**

[Journal project](projects/dp-smm-journal/README.md) · [Detector architecture](projects/dp-smm-journal/docs/architecture.md) · [RTL verification and FPGA implementation](projects/dp-smm-journal/docs/validation.md)

## DS-SBM and DP-SMM: Signal Paths and Candidate Retention

![DS-SBM and DP-SMM comparison: 21-tap RX FFE signal paths, retained candidates and rescoring](projects/dp-smm-journal/assets/ds_sbm_dp_smm_21tap_comparison.svg)

[Follow-up architecture comparison](projects/dp-smm-journal/docs/ds-sbm-comparison.md) · [Candidate-retention results](projects/dp-smm-journal/docs/candidate-retention.md) · [Verification status](docs/validation-status.md)

DP-SMM board measurements are pending. Candidate-retention comparisons, RTL verification and FPGA implementation results are documented in the journal project.

## Related Research and Development Workflow

- [A-SSCC 2026 · DS-SBM PAM4 DSP transceiver](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/projects/zcu208-pam4-dsp-portfolio/README.md): RFSoC measurements through an ISI board and FPGA implementation results.
- [AI, toolboxes and measurement automation harness](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/docs/ai-assisted-dsp-workflow.en.md): assistance with RTL, testbench and automation code.
- [High-Speed Interface & DSP Transceiver portfolio](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/README.en.md): A-SSCC and LPDDR/USB interface research.

[Research index](projects/README.md) · [Publication and patent preparation](docs/publications.md)

<!-- page-navigation:bottom -->
<p>
  <a href="#page-top" title="Back to top"><img src="assets/readme/nav-top.svg" alt="Back to top" width="100" height="30"></a>
</p>
<!-- /page-navigation:bottom -->

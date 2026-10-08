<a id="page-top"></a>

<p align="right">
<a href="README.md" title="한국어 연구 소개 보기"><img src="assets/readme/nav-ko.svg" alt="한국어" width="87" height="30"></a>
</p>

# Juhyeong Yun | PAM4 MLSD Research (In Progress)

Kwangwoon University · Master's thesis research

This repository covers my **DS-SBM–DP-SMM thesis comparison** and **DP-SMM journal preparation**. I use models and RTL to study how the location and number of retained path candidates affect final decisions.

<p>
<a href="projects/pam4-mlsd-thesis/README.md"><img src="assets/readme/status-thesis-en.svg" alt="Thesis · In progress" width="160" height="30"></a>
<a href="projects/dp-smm-journal/README.md"><img src="assets/readme/status-journal-en.svg" alt="Journal · In progress" width="166" height="30"></a>
</p>

## Master's Thesis | DS-SBM–DP-SMM Comparison (In Progress)

I compare the signal paths, candidate retention and frame-boundary updates of the two architectures. Within DP-SMM, I apply identical inputs to cores that retain one or two paths per matrix entry to evaluate the effect on error counts.

[Thesis project](projects/pam4-mlsd-thesis/README.md) · [Architecture comparison](projects/pam4-mlsd-thesis/docs/architecture.md) · [Model–RTL comparison](projects/pam4-mlsd-thesis/docs/validation.md)

## Journal Preparation | DP-SMM Design and Verification (In Progress)

DP-SMM retains two paths in each segment metric-matrix entry and rescores them using actual symbol histories. I verified agreement between the reference model and RTL and completed FPGA place-and-route. Board measurements are planned with **21-tap RX FFE + DP-SMM**.

**A patent application for DP-SMM is in preparation.**

[Journal project](projects/dp-smm-journal/README.md) · [Detector architecture](projects/dp-smm-journal/docs/architecture.md) · [RTL verification and FPGA implementation](projects/dp-smm-journal/docs/validation.md)

## DS-SBM and DP-SMM: Signal Paths and Candidate Retention

![DS-SBM and DP-SMM comparison: 21-tap RX FFE signal paths, retained candidates and rescoring](projects/dp-smm-journal/assets/ds_sbm_dp_smm_21tap_comparison.svg)

[Comparison details](projects/dp-smm-journal/README.md#ds-sbm에서-확장한-점) · [Verification status](docs/validation-status.md)

DP-SMM board measurements are pending. Model, RTL and FPGA results are documented separately from the measured DS-SBM results in A-SSCC.

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

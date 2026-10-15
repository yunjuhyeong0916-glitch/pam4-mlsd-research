<a id="page-top"></a>

<p align="right">
<a href="README.en.md#page-top" title="View this research overview in English"><img src="assets/readme/nav-en.svg" alt="English" width="96" height="30"></a>
</p>

# 윤주형 | PAM4 MLSD 연구 (진행 중)

광운대학교 · 석사 학위논문 연구

PAM4 수신기의 **DS-SBM 학위논문 연구**와 후속 **DP-SMM Journal 준비 연구**를 정리합니다. 검출 구조의 후보 선택과 병렬 처리를 설계하고, 모델·RTL 검증에서 RFSoC 물리채널 평가로 연결합니다.

<p>
<a href="projects/pam4-mlsd-thesis/README.md#page-top"><img src="assets/readme/status-thesis.svg" alt="학위논문 · 진행 중" width="157" height="30"></a>
<a href="projects/dp-smm-journal/README.md#page-top"><img src="assets/readme/status-journal.svg" alt="Journal · 진행 중" width="153" height="30"></a>
</p>

## 학위논문 | DS-SBM 설계·RFSoC 검증 (진행 중)

**원고 마무리 중.** 상태별 두 생존 분기와 구간 메트릭 행렬 합성으로 PAM4 검출기를 설계했습니다. ZCU208·XM655·ISI 보드의 **4 GS/s·PAM4 8 Gb/s** 물리 경로에서 동작을 확인했습니다.

<a href="projects/pam4-mlsd-thesis/docs/implementation.md#page-top"><img src="projects/pam4-mlsd-thesis/assets/rfsoc_signal_path.png" alt="DS-SBM 학위논문의 DAC·물리채널·ADC 송수신 경로" width="840"></a>

추정 전체 경로 손실 **약 41 dB @ 2 GHz**, PRBS7 **BER < 10⁻⁷**, PRBS15 **BER < 2×10⁻⁶**. 검출기 단독 자원은 RS-ACS 대비 **LUT 35.7%·FF 22.5% 감소**했습니다.

[학위논문 프로젝트](projects/pam4-mlsd-thesis/README.md#page-top) · [검출기 구조](projects/pam4-mlsd-thesis/docs/architecture.md#page-top) · [RFSoC 구현](projects/pam4-mlsd-thesis/docs/implementation.md#page-top) · [측정·자원 결과](projects/pam4-mlsd-thesis/docs/validation.md#page-top)

## Journal 준비 | DP-SMM 설계·검증 (진행 중)

구간 메트릭 행렬에 두 경로를 보존하고, 실제 심볼 이력으로 비용을 재평가하는 검출기를 설계했습니다. 참조 모델과 RTL의 일치를 확인하고 FPGA 배치배선을 수행했습니다. **21-tap RX FFE + DP-SMM** 구성으로 보드 실측을 준비합니다.

**DP-SMM 특허 출원 준비 중.**

[Journal 프로젝트](projects/dp-smm-journal/README.md#page-top) · [검출기 구조](projects/dp-smm-journal/docs/architecture.md#page-top) · [RTL 검증·FPGA 구현](projects/dp-smm-journal/docs/validation.md#page-top)

## DS-SBM과 DP-SMM의 신호 경로·후보 보존

![DS-SBM과 DP-SMM의 21-tap RX FFE 신호 경로, 후보 보존 위치와 비용 재평가 비교](projects/dp-smm-journal/assets/ds_sbm_dp_smm_21tap_comparison.svg)

[후속 DP-SMM의 구조 비교](projects/dp-smm-journal/docs/ds-sbm-comparison.md#page-top) · [후보 보존 효과](projects/dp-smm-journal/docs/candidate-retention.md#page-top) · [검증 현황](docs/validation-status.md#page-top)

DP-SMM 보드 측정은 예정입니다. 두 경로 보존의 모델·RTL 비교와 FPGA 구현 결과는 Journal 프로젝트에 정리했습니다.

## 관련 연구·개발 방법

- [A-SSCC 2026 · DS-SBM PAM4 송수신 DSP](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/projects/zcu208-pam4-dsp-portfolio/README.md#page-top): RFSoC·ISI 보드 측정과 FPGA 구현 결과.
- [AI 활용·Toolbox·측정 자동화 harness](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/docs/ai-assisted-dsp-workflow.md#page-top): RTL·테스트벤치와 반복 검증·측정 자동화 코드 구성.
- [High-Speed Interface·DSP Transceiver 포트폴리오](https://github.com/yunjuhyeong0916-glitch/jhyun#page-top): A-SSCC와 LPDDR·USB 인터페이스 연구.

[연구 목록](projects/README.md#page-top) · [논문·특허 준비](docs/publications.md#page-top)

<!-- page-navigation:bottom -->
<p>
  <a href="#page-top" title="페이지 맨 위로 이동"><img src="assets/readme/nav-top.svg" alt="페이지 맨 위로 이동" width="100" height="30"></a>
</p>
<!-- /page-navigation:bottom -->

<a id="page-top"></a>

<p align="right">
<a href="README.en.md" title="View this research overview in English"><img src="assets/readme/nav-en.svg" alt="English" width="96" height="30"></a>
</p>

# 윤주형 | PAM4 MLSD 연구 (진행 중)

광운대학교 · 석사 학위논문 연구

PAM4 수신기의 **DS-SBM·DP-SMM 비교 연구**와 **DP-SMM Journal 준비 연구**를 정리합니다. 경로 후보를 어디에, 몇 개 남기느냐에 따라 최종 판정이 어떻게 달라지는지 모델·RTL에서 확인하고 있습니다.

<p>
<a href="projects/pam4-mlsd-thesis/README.md"><img src="assets/readme/status-thesis.svg" alt="학위논문 · 진행 중" width="157" height="30"></a>
<a href="projects/dp-smm-journal/README.md"><img src="assets/readme/status-journal.svg" alt="Journal · 진행 중" width="153" height="30"></a>
</p>

## 학위논문 | DS-SBM·DP-SMM 비교 (진행 중)

두 구조의 신호 경로·후보 보존·프레임 경계 갱신을 비교합니다. DP-SMM에서는 행렬 원소마다 경로를 하나 또는 두 개 남기는 코어에 동일 입력을 적용해, 후보 보존이 오류 수에 미치는 영향을 확인했습니다.

[학위논문 프로젝트](projects/pam4-mlsd-thesis/README.md) · [구조 비교](projects/pam4-mlsd-thesis/docs/architecture.md) · [모델·RTL 비교 결과](projects/pam4-mlsd-thesis/docs/validation.md)

## Journal 준비 | DP-SMM 설계·검증 (진행 중)

구간 메트릭 행렬에 두 경로를 보존하고, 실제 심볼 이력으로 비용을 재평가하는 검출기를 설계했습니다. 참조 모델과 RTL의 일치를 확인하고 FPGA 배치배선을 수행했습니다. **21-tap RX FFE + DP-SMM** 구성으로 보드 실측을 준비합니다.

**DP-SMM 특허 출원 준비 중.**

[Journal 프로젝트](projects/dp-smm-journal/README.md) · [검출기 구조](projects/dp-smm-journal/docs/architecture.md) · [RTL 검증·FPGA 구현](projects/dp-smm-journal/docs/validation.md)

## DS-SBM과 DP-SMM의 신호 경로·후보 보존

![DS-SBM과 DP-SMM의 21-tap RX FFE 신호 경로, 후보 보존 위치와 비용 재평가 비교](projects/dp-smm-journal/assets/ds_sbm_dp_smm_21tap_comparison.svg)

[비교 그림 설명](projects/dp-smm-journal/README.md#ds-sbm에서-확장한-점) · [검증 현황](docs/validation-status.md)

DP-SMM 보드 측정은 예정입니다. 현재 모델·RTL·FPGA 구현 결과와 A-SSCC의 DS-SBM 실측 결과는 각 프로젝트에서 확인할 수 있습니다.

## 관련 연구·개발 방법

- [A-SSCC 2026 · DS-SBM PAM4 송수신 DSP](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/projects/zcu208-pam4-dsp-portfolio/README.md): RFSoC·ISI 보드 측정과 FPGA 구현 결과.
- [AI 활용·Toolbox·측정 자동화 harness](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/docs/ai-assisted-dsp-workflow.md): RTL·테스트벤치와 반복 검증·측정 자동화 코드 구성.
- [High-Speed Interface·DSP Transceiver 포트폴리오](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/README.md): A-SSCC와 LPDDR·USB 인터페이스 연구.

[연구 목록](projects/README.md) · [논문·특허 준비](docs/publications.md)

<!-- page-navigation:bottom -->
<p>
  <a href="#page-top" title="페이지 맨 위로 이동"><img src="assets/readme/nav-top.svg" alt="페이지 맨 위로 이동" width="100" height="30"></a>
</p>
<!-- /page-navigation:bottom -->

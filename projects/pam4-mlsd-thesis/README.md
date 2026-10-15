<a id="page-top"></a>

<p align="right"><a href="README.en.md#page-top"><img src="../../assets/readme/nav-en.svg" alt="English" width="96" height="30"></a></p>

# 학위논문 | DS-SBM 기반 PAM4 수신기 설계·검증 (진행 중)

<!-- page-navigation:top -->
<p>
  <a href="../README.md#page-top" title="연구 목록로 돌아가기"><img src="../../assets/readme/nav-back-research.svg" alt="연구 목록로 돌아가기" width="110" height="30"></a>
  <a href="https://github.com/yunjuhyeong0916-glitch/pam4-mlsd-research#page-top" title="홈으로 돌아가기"><img src="../../assets/readme/nav-home.svg" alt="홈으로 돌아가기" width="70" height="30"></a>
</p>
<!-- /page-navigation:top -->

<p align="right"><a href="README.en.md#page-top">English</a></p>

고손실 PAM4 채널에서 시퀀스 검출의 연산량과 순차 의존성을 줄이기 위해 **DS&#8209;SBM 축소 상태 검출기**를 설계했습니다. 상태별 두 생존 분기로 후보를 남기고 구간 메트릭 행렬을 병렬 합성한 뒤, ZCU208의 DAC–물리채널–ADC 경로에서 복원 성능을 확인했습니다.

**석사 학위논문 · 원고 마무리 중**

[DS&#8209;SBM 구조](docs/architecture.md#page-top) · [RFSoC 구현](docs/implementation.md#page-top) · [측정·자원](docs/validation.md#page-top)

## 대표 결과

**측정 조건:** ZCU208·XM655·ISI 보드, 4&nbsp;GS/s, 추정 전체 경로 손실 약 41&nbsp;dB @ 2&nbsp;GHz. BER은 각 패턴의 선정 PR 응답 조건입니다.

| 평가 항목 | 결과 |
|---|---|
| 물리 송수신 경로 | **PAM4 8&nbsp;Gb/s** |
| PRBS7 BER | **< 10⁻⁷** |
| PRBS15 BER | **< 2×10⁻⁶** |
| RS-ACS 대비 검출기 자원 | **LUT 35.7%·FF 22.5% 감소** |

<a href="docs/implementation.md#page-top"><img src="assets/rfsoc_signal_path.png" alt="PRBS 생성에서 TX FFE·DAC·ISI 보드·ADC·RX FFE·PR 필터·DS-SBM을 거쳐 오류를 검사하는 물리 송수신 경로" width="840"></a>

## 두 생존 분기와 구간 행렬을 결합한 이유

기억 길이 2의 PAM4 전체 상태 검출은 16상태와 심볼당 64개 전이 후보를 다룹니다. DS-SBM은 이를 네 축소 상태로 묶고, 상태마다 비용이 작은 두 분기를 다음 경로 구성에 전달합니다. 현재 샘플에서 후보를 하나로 좁히는 대신, 이후 구간의 누적 비용 비교에 참여할 여지를 남겼습니다.

심볼별 PM 갱신을 길게 연결하면 이전 연산 결과를 기다리는 경로가 길어집니다. 32심볼을 여덟 4심볼 구간으로 나누어 비용을 병렬 계산하고, 행렬을 트리 형태로 합성하도록 구성했습니다. 대표 이력에 따른 BM 계산, 행렬 원소별 한 경로 선택, 프레임 경계 PM 갱신을 [동작 그림과 수치 예제](docs/architecture.md#page-top)로 설명합니다.

## 필터부터 오류 검사까지 연결한 RFSoC 검증

8-tap TX FFE, 21-tap RX FFE와 3-tap PR 필터를 검출기와 연결했습니다. RX FFE의 채널 보상 조건을 유지하면서 PR 응답을 바꿀 수 있도록 두 수신 필터를 분리했고, 실제 채널을 통과한 복원 비트를 PRBS 검사기로 평가했습니다. [송수신 데이터 경로·PS 제어](docs/implementation.md#page-top) · [BER 컨투어·FPGA 자원](docs/validation.md#page-top)

## 관련 연구

논문 제목: *A PAM4 Reduced-State Maximum-Likelihood Sequence Detector Using Dual Survivors and Segmented Metric Matrices*

학위논문은 [A-SSCC 2026의 DS-SBM 송수신기 연구](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/projects/zcu208-pam4-dsp-portfolio/README.md#page-top)를 바탕으로 검출 구조의 동작과 RFSoC 구현·측정 결과를 상세히 정리합니다. 행렬 원소에 두 경로를 보존하는 후속 DP-SMM 연구는 [Journal 프로젝트](../dp-smm-journal/README.md#page-top)에서 다룹니다.

<!-- page-navigation:bottom -->
<p>
  <a href="../README.md#page-top" title="연구 목록로 돌아가기"><img src="../../assets/readme/nav-back-research.svg" alt="연구 목록로 돌아가기" width="110" height="30"></a>
  <a href="https://github.com/yunjuhyeong0916-glitch/pam4-mlsd-research#page-top" title="홈으로 돌아가기"><img src="../../assets/readme/nav-home.svg" alt="홈으로 돌아가기" width="70" height="30"></a>
  <a href="#page-top" title="페이지 맨 위로 이동"><img src="../../assets/readme/nav-top.svg" alt="페이지 맨 위로 이동" width="100" height="30"></a>
</p>
<!-- /page-navigation:bottom -->

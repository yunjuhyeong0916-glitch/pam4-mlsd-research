<a id="page-top"></a>

# 연구 검증 현황

<!-- page-navigation:top -->
<p>
  <a href="README.md" title="문서 목록으로 돌아가기"><img src="../assets/readme/nav-back-docs.svg" alt="문서 목록으로 돌아가기" width="110" height="30"></a>
  <a href="../README.md" title="홈으로 돌아가기"><img src="../assets/readme/nav-home.svg" alt="홈으로 돌아가기" width="70" height="30"></a>
</p>
<!-- /page-navigation:top -->

기준일: **2026-10-07**.

## 학위논문 | DS-SBM·DP-SMM 비교 (진행 중)

| 항목 | 결과 | 조건 |
|---|---|---|
| 구조 비교 | 신호 경로·행렬 후보·경계 PM 갱신 비교 | DS-SBM과 DP-SMM |
| 후보 보존 효과 | R=2의 오류 수가 R=1보다 36.9%·46.1% 감소 | memory-2 합성 응답 A·B, SNR 16 dB, 경계 후보 수 K_H=2 고정 |
| R=1/R=2 코어 RTL | 참조 출력·메트릭·경로 정보 일치 | 연속·간격 입력, reset 후 재시작 |
| DP-SMM 실측 | 예정 | AWG 기반 ADC-DSP 수신 평가 |

[동일 입력 비교·RTL 검증 조건](../projects/pam4-mlsd-thesis/docs/validation.md).

## Journal 준비 | DP-SMM (진행 중)

| 항목 | 결과 | 조건·출처 |
|---|---|---|
| 검출기 코어 RTL | bit-accurate 참조 모델과 일치, 지연 23클록·II=1 | 개정 K=2 및 행렬 K=1 비교 코어 |
| 기존 RX FFE 통합 RTL | 참조와 일치, 지연 24클록·II=1 | 기존 11-tap RX FFE·검출기 통합 구성 |
| 검출기 FPGA 자원 | LUT 266,664·FF 168,330·BRAM 240·DSP 1,664 | Journal 초안의 post-route 구현, RX FFE 제외 |
| 보드 실측 | 예정 | 21-tap RX FFE + DP-SMM, BER·PR 등고선·연속 처리율 |

[Journal RTL 검증·구현 조건](../projects/dp-smm-journal/docs/validation.md).

[A-SSCC DS-SBM 실측·구현 결과](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/projects/zcu208-pam4-dsp-portfolio/docs/validation.md)

<!-- page-navigation:bottom -->
<p>
  <a href="README.md" title="문서 목록으로 돌아가기"><img src="../assets/readme/nav-back-docs.svg" alt="문서 목록으로 돌아가기" width="110" height="30"></a>
  <a href="../README.md" title="홈으로 돌아가기"><img src="../assets/readme/nav-home.svg" alt="홈으로 돌아가기" width="70" height="30"></a>
  <a href="#page-top" title="페이지 맨 위로 이동"><img src="../assets/readme/nav-top.svg" alt="페이지 맨 위로 이동" width="100" height="30"></a>
</p>
<!-- /page-navigation:bottom -->

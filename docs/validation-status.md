<a id="page-top"></a>

# 연구 검증 현황

<!-- page-navigation:top -->
<p>
  <a href="README.md" title="문서 목록으로 돌아가기"><img src="../assets/readme/nav-back-docs.svg" alt="문서 목록으로 돌아가기" width="110" height="30"></a>
  <a href="../README.md" title="홈으로 돌아가기"><img src="../assets/readme/nav-home.svg" alt="홈으로 돌아가기" width="70" height="30"></a>
</p>
<!-- /page-navigation:top -->

기준일: **2026-10-15**.

## 학위논문 | DS-SBM 설계·RFSoC 검증 (진행 중)

원고 마무리 단계입니다. DS-SBM의 동작 설명과 RFSoC 구현·측정 결과를 정리했습니다.

| 항목 | 결과 | 조건 |
|---|---|---|
| 검출 구조 | 네 축소 상태·상태별 두 분기·행렬 원소별 한 경로 | 32심볼을 여덟 4심볼 구간으로 처리 |
| 물리채널 BER | PRBS7 < 10⁻⁷, PRBS15 < 2×10⁻⁶ | 4 GS/s·PAM4 8 Gb/s, 추정 손실 약 41 dB @ 2 GHz, 선정 PR 응답 |
| 검출기 자원 | LUT 166k·FF 62k | RS-ACS 대비 LUT 35.7%·FF 22.5% 감소 |
| 전체 송수신기 | LUT 189,108·FF 188,846·DSP 950·BRAM 24.5 | TX·RX 필터와 인터페이스·제어 포함 |

[DS-SBM 구조](../projects/pam4-mlsd-thesis/docs/architecture.md) · [측정·구현 결과](../projects/pam4-mlsd-thesis/docs/validation.md)

## Journal 준비 | DP-SMM (진행 중)

| 항목 | 결과 | 조건·출처 |
|---|---|---|
| 검출기 코어 RTL | bit-accurate 참조 모델과 일치, 지연 23클록·II=1 | 개정 K=2 및 행렬 K=1 비교 코어 |
| 기존 RX FFE 통합 RTL | 참조와 일치, 지연 24클록·II=1 | 기존 11-tap RX FFE·검출기 통합 구성 |
| 검출기 FPGA 자원 | LUT 266,664·FF 168,330·BRAM 240·DSP 1,664 | Journal 초안의 post-route 구현, RX FFE 제외 |
| 보드 실측 | 예정 | 21-tap RX FFE + DP-SMM, BER·PR 등고선·연속 처리율 |

[Journal RTL 검증·구현 조건](../projects/dp-smm-journal/docs/validation.md) · [동일 입력의 후보 보존 효과](../projects/dp-smm-journal/docs/candidate-retention.md).

[A-SSCC DS-SBM 실측·구현 결과](https://github.com/yunjuhyeong0916-glitch/jhyun/blob/main/projects/zcu208-pam4-dsp-portfolio/docs/validation.md)

<!-- page-navigation:bottom -->
<p>
  <a href="README.md" title="문서 목록으로 돌아가기"><img src="../assets/readme/nav-back-docs.svg" alt="문서 목록으로 돌아가기" width="110" height="30"></a>
  <a href="../README.md" title="홈으로 돌아가기"><img src="../assets/readme/nav-home.svg" alt="홈으로 돌아가기" width="70" height="30"></a>
  <a href="#page-top" title="페이지 맨 위로 이동"><img src="../assets/readme/nav-top.svg" alt="페이지 맨 위로 이동" width="100" height="30"></a>
</p>
<!-- /page-navigation:bottom -->

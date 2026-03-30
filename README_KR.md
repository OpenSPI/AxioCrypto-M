# AxioCryptoM

> English version: [README.md](README.md)

AxioCryptoM은 KCMVP 검증필 암호모듈 AxioCrypto와 PQC(NIST), K-PQC 알고리즘을 임베디드 MCU 플랫폼에서 사용할 수 있도록 제공하는 라이브러리입니다.

일반 및 TrustZone 환경에서 동작하며, KCMVP 검증필 암호 알고리즘과 PQC(NIST), K-PQC 알고리즘을 통해 강력한 보안 기능을 제공합니다.

Nuvoton, STMicroelectronics, Microchip 등을 포함한 다수의 MCU에서 사용이 가능합니다.

---

## 암호모듈

| 암호모듈명 | 검증번호 | 검증일 | 효력만료일 | 개발사 | 모듈형태 | KCMVP | 
|---------------------|----------|--------|------------|--------|----------|-------|
| AxioCrypto v2.1.0 | CM-280-2030.10 | 2025-10-14 | 2030-10-14 | 시큐리티플랫폼㈜ | F/W | 검증필 |
| AxioCrypto v2.2.0 | ➖ | ➖ | ➖ | 시큐리티플랫폼㈜ | F/W | 검증예정 |

---


## AxioCryptoM v2.1.0

### 지원 플랫폼
상세 내용 및 사용방법은 각 MCU라인의 README를 참고하십시오.

| # | 제조사 | MCU 라인 | 파트넘버 | 코어 | 보드 | KCMVP 검증 | 샘플 코드 |
|:---:|--------|--------|--------|-----|------|-------------|------|
| 1 |Nuvoton| M2351 | M2351ZIAAE | Cortex-M23 | Custom Board| ✅ |✅ |
| 2 |Nuvoton| M2351 | M2351SIAAE | Cortex-M23 | Custom Board| ✅ |✅ |
| 3 |Nuvoton| M2351 | M2351KIAAE | Cortex-M23 | NuMaker-PFM-M2351| ✅|✅ |
| 4 |Nuvoton| M2354 | M2354LJFAE | Cortex-M23 | Custom Board| ✅|✅ |
| 5 |Nuvoton| M2354 | M2354SJFAE | Cortex-M23 | Custom Board| ✅|✅ |
| 6 |Nuvoton| M2354 | M2354KJFAE | Cortex-M23 | NuMaker-PFM-M2354| ✅|✅ |
| 7 |STMicroelectronics| STM32H563 | STM32H563ZI | Cortex-M33 | NUCLEO-H563ZI| ✅|✅ |
| 8 |STMicroelectronics| STM32H562 | STM32H562VG | Cortex-M33 | Custom Board| ✅|예정 |
| 9 |Renesas| RA6 | R7FA6M4AF3CFB | Cortex-M33 | Custom Board| ✅|예정 |
| 10 |Renesas| RA6 | R7FA6M5BH3CFC | Cortex-M33 | Custom Board| ✅|예정 |
| 11 |Renesas| RA6 | R7FA6E10F2CFP | Cortex-M33 | Custom Board| ✅|예정 |
| 12 |Renesas| RA4 | R7FA4M2AD3CFP | Cortex-M33 | Custom Board| ✅|예정 |
| 13 |Renesas| RA4 | R7FA4M3AF3CFB | Cortex-M33 | Custom Board| ✅|예정 |
| 14 |Renesas| RA4 | R7FA4E10D2CFM | Cortex-M33 | Custom Board| ✅|예정 |

### 지원 암호 알고리즘

| 제조사 | MCU 라인 | PQC | ARIA | AES | LEA | SHA | HMAC | Random Generator | TRNG | ECDSA | ECDH | PBKDF2 | HKDF | Key Management |
|--------|--------|:----:|:----:|:---:|:---:|:-------:|:----:|:-----------:|:----:|:-----:|:----:|:------:|:----:|:------:|
| Nuvoton | M2351 | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Nuvoton | M2354 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32H563 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

| 항목 | 세부 알고리즘 |
|------|--------------|
| PQC DSA(NIST) | ML-DSA-44 (Dilithium2), SLH-DSA-Shake128f (SPHINCS+), FN-DSA-512 (Falcon-512) |
| PQC KEM(NIST) | ML-KEM-512 (Kyber-512) |
| K-PQC DSA | AIMer-128f, HAETAE-2 |
| K-PQC KEM | NTRU-768, SMAUG-1 |
| ARIA | ARIA-128 / 192 / 256, CBC / CTR / GCM |
| AES | AES-128 / 192 / 256, CBC / CTR / GCM |
| LEA | LEA-128 / 192 / 256, CBC / CTR / GCM |
| SHA | SHA-256 |
| HMAC | HMAC-SHA-256 |
| Random Generator | Hash_DRBG (SHA-256) |
| TRNG | True Random Number Generator (하드웨어 난수 발생기) |
| ECDSA | ECDSA P-256 |
| ECDH | ECDH P-256 |
| PBKDF2 | PBKDF2-HMAC-SHA-256 |
| HKDF | HKDF-SHA-256 |
| Key Management | 키 생성 / 저장 / 삭제 / 조회 |

---

## AxioCryptoM v2.2.0(지원 예정)

### 업데이트 사항
AES 검증모드에서 사용 가능하도록 변경

### 지원 플랫폼

상세 내용 및 사용방법은 각 MCU라인의 README를 참고하십시오.

| # | 제조사 | MCU 라인 | 파트넘버 | 코어 | 보드 | KCMVP 검증 | 샘플 코드 |
|:---:|--------|--------|---------|-----|------|-------------|----------|
| 1 | Nuvoton | M2351 | M2351ZIAAE | Cortex-M23 | Custom Board | 예정 | 예정 |
| 2 | Nuvoton | M2351 | M2351SIAAE | Cortex-M23 | Custom Board | 예정 | 예정 |
| 3 | Nuvoton | M2351 | M2351KIAAE | Cortex-M23 | NuMaker-PFM-M2351 | 예정 | 예정 |
| 4 | Nuvoton | M2354 | M2354LJFAE | Cortex-M23 | Custom Board | 예정 | 예정 |
| 5 | Nuvoton | M2354 | M2354SJFAE | Cortex-M23 | Custom Board | 예정 | 예정 |
| 6 | Nuvoton | M2354 | M2354KJFAE | Cortex-M23 | NuMaker-PFM-M2354 | 예정 | 예정 |
| 7 | STMicroelectronics | STM32F207 | STM32F207ZG | Cortex-M3 | NUCLEO-F207ZG | 예정 | 예정 |
| 8 | STMicroelectronics | STM32F303 | STM32F303RE | Cortex-M4 | NUCLEO-F303RE | 예정 | 예정 |
| 9 | STMicroelectronics | STM32F401 | STM32F401RE | Cortex-M4 | NUCLEO-F401RE | 예정 | 예정 |
| 10 | STMicroelectronics | STM32F767 | STM32F767ZI | Cortex-M7 | NUCLEO-F767ZI | 예정 | 예정 |
| 11 | STMicroelectronics | STM32G0B1 | STM32G0B1RE | Cortex-M0+ | NUCLEO-G0B1RE | 예정 | 예정 |
| 12 | STMicroelectronics | STM32G474 | STM32G474RE | Cortex-M4 | NUCLEO-G474RE | 예정 | 예정 |
| 13 | STMicroelectronics | STM32H563 | STM32H563ZI | Cortex-M33 | NUCLEO-H563ZI | 예정 | 예정 |
| 14 | STMicroelectronics | STM32H563 | STM32H563ZG | Cortex-M33 | NUCLEO-H563ZI | 예정 | 예정 |
| 15 | STMicroelectronics | STM32H562 | STM32H562VG | Cortex-M33 | Custom Board | 예정 | 예정 |
| 16 | STMicroelectronics | STM32H562 | STM32H562VI | Cortex-M33 | Custom Board | 예정 | 예정 |
| 17 | STMicroelectronics | STM32H753 | STM32H753ZI | Cortex-M7 | NUCLEO-H753ZI | 예정 | 예정 |
| 18 | STMicroelectronics | STM32L152 | STM32L152RE | Cortex-M3 | NUCLEO-L152RE | 예정 | 예정 |
| 19 | STMicroelectronics | STM32L452 | STM32L452RE | Cortex-M4 | NUCLEO-L452RE-P | 예정 | 예정 |
| 20 | STMicroelectronics | STM32L476 | STM32L476RG | Cortex-M4 | NUCLEO-L476RG | 예정 | 예정 |
| 21 | STMicroelectronics | STM32L496 | STM32L496ZG | Cortex-M4 | NUCLEO-L496ZG-P | 예정 | 예정 |
| 22 | STMicroelectronics | STM32L4R5 | STM32L4R5ZI | Cortex-M4 | NUCLEO-L4R5ZI-P | 예정 | 예정 |
| 23 | STMicroelectronics | STM32L552 | STM32L552ZE | Cortex-M33 | NUCLEO-L552ZE-Q | 예정 | 예정 |
| 24 | STMicroelectronics | STM32U385 | STM32U385RG | Cortex-M33 | NUCLEO-U385RG-Q | 예정 | 예정 |
| 25 | STMicroelectronics | STM32U545 | STM32U545RE | Cortex-M33 | NUCLEO-U545RE-Q | 예정 | 예정 |
| 26 | STMicroelectronics | STM32U575 | STM32U575ZI | Cortex-M33 | NUCLEO-U575ZI-Q | 예정 | 예정 |
| 27 | STMicroelectronics | STM32WB55 | STM32WB55CG | Dual Core (M4+M0+) | P-NUCLEO-WB55 | 예정 | 예정 |
| 28 | STMicroelectronics | STM32WBA52 | STM32WBA52CG | Cortex-M33 | NUCLEO-WBA52CG | 예정 | 예정 |
| 29 | STMicroelectronics | STM32WL55 | STM32WL55JC | Dual Core (M4+M0+) | NUCLEO-WL55JC1 | 예정 | 예정 |
| 30 | Renesas | RA6 | R7FA6M4AF3CFB | Cortex-M33 | Custom Board | 예정 | 예정 |
| 31 | Renesas | RA6 | R7FA6M5BH3CFC | Cortex-M33 | Custom Board | 예정 | 예정 |
| 32 | Renesas | RA6 | R7FA6E10F2CFP | Cortex-M33 | Custom Board | 예정 | 예정 |
| 33 | Renesas | RA4 | R7FA4M2AD3CFP | Cortex-M33 | Custom Board | 예정 | 예정 |
| 34 | Renesas | RA4 | R7FA4M3AF3CFB | Cortex-M33 | Custom Board | 예정 | 예정 |
| 35 | Renesas | RA4 | R7FA4E10D2CFM | Cortex-M33 | Custom Board | 예정 | 예정 |
| 36 | Microchip | PIC32CX-MT | PIC32CXMTSH | Dual Core (M4+M0+) | PIC32CXMTSH-DB | 예정 | 예정 |
| 37 | Microchip | PIC32CX-MT | PIC32CXMTC | Dual Core (M4+M0+) | PIC32CXMTC-DB | 예정 | 예정 |

> **참고:** STMicroelectronics 제품군은 동일 MCU 라인의 모든 하위 파트넘버에서 동작을 보장합니다.  
> 예) `STM32H563` 라인 → STM32H563**AG** / **AI** / **IG** / **II** / **LI** / **MI** / **RG** / **RI** / **VG** / **VI** / **ZG** / **ZI** 등


### 지원 암호 알고리즘


| 제조사 | MCU 라인 | PQC | ARIA | AES | LEA | SHA | HMAC | Random Generator | TRNG | ECDSA | ECDH | PBKDF2 | HKDF | Key Management |
|--------|--------|:----:|:----:|:---:|:---:|:-------:|:----:|:-----------:|:----:|:-----:|:----:|:------:|:----:|:------:|
| Nuvoton | M2351 | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Nuvoton | M2354 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32F207 | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32F303 | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32F401 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32F767 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32G0B1 | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32G474 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32H563 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32H562 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32H753 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32L152 | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32L452 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32L476 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32L496 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32L4R5 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32L552 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32U385 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32U545 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32U575 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32WB55 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32WBA52 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32WL55 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Renesas | RA4 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Renesas | RA6 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Microchip | PIC32CX-MT | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ |


| 항목 | 세부 알고리즘 |
|------|--------------|
| PQC DSA(NIST) | ML-DSA-44 (Dilithium2), SLH-DSA-Shake128f (SPHINCS+), FN-DSA-512 (Falcon-512) |
| PQC KEM(NIST) | ML-KEM-512 (Kyber-512) |
| K-PQC DSA | AIMer-128f, HAETAE-2 |
| K-PQC KEM | NTRU-768, SMAUG-1 |
| ARIA | ARIA-128 / 192 / 256, CBC / CTR / GCM |
| AES | AES-128 / 192 / 256, CBC / CTR / GCM |
| LEA | LEA-128 / 192 / 256, CBC / CTR / GCM |
| SHA | SHA-256 |
| HMAC | HMAC-SHA-256 |
| Random Generator | Hash_DRBG (SHA-256) |
| TRNG | True Random Number Generator (하드웨어 난수 발생기) |
| ECDSA | ECDSA P-256 |
| ECDH | ECDH P-256 |
| PBKDF2 | PBKDF2-HMAC-SHA-256 |
| HKDF | HKDF-SHA-256 |
| Key Management | 키 생성 / 저장 / 삭제 / 조회 |

---

## 라이선스
본 라이브러리 및 예제 소스는 개인적 용도에 한해 자유롭게 사용할 수 있습니다.  
상업적 사용, 재배포, 수정, 무단 복제, 리버스 엔지니어링은 금지됩니다.  
상용 라이선스 문의는 시큐리티플랫폼㈜으로 연락해주십시오.

---

## 사용 제한

본 AxioCryptoM 라이브러리는 **공개용(Evaluation)** 버전으로, API 사용 횟수에 제한이 있습니다.  
제한 해제 및 상용 라이선스 문의는 시큐리티플랫폼㈜으로 연락해주십시오.

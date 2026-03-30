# AxioCryptoM

> Korean version: [README_KR.md](README_KR.md)

AxioCryptoM is a library that provides the KCMVP-certified cryptographic module AxioCrypto along with PQC (NIST) and K-PQC algorithms for use on embedded MCU platforms.

It operates in both standard and TrustZone environments, delivering robust security features through KCMVP-certified cryptographic algorithms as well as PQC (NIST) and K-PQC algorithms.

Compatible with a wide range of MCUs including those from Nuvoton, STMicroelectronics, Microchip, and more.

---

## Cryptographic Module

| Module Name | Cert. No. | Cert. Date | Expiry Date | Developer | Module Type | KCMVP |
|---------------------|----------|--------|------------|--------|----------|-------|
| AxioCrypto v2.1.0 | CM-280-2030.10 | 2025-10-14 | 2030-10-14 | Security Platform Inc. | F/W | Certified |
| AxioCrypto v2.2.0 | ➖ | ➖ | ➖ | Security Platform Inc. | F/W | In Preparation |

---


## AxioCryptoM v2.1.0

### Supported Platforms
Refer to the README of each MCU line for details and usage instructions.

| # | Manufacturer | MCU Line | Part Number | Core | Board | KCMVP Cert. | Sample Code |
|:---:|--------|--------|--------|-----|------|-------------|------|
| 1 | Nuvoton | M2351 | M2351ZIAAE | Cortex-M23 | Custom Board | ✅ | ✅ |
| 2 | Nuvoton | M2351 | M2351SIAAE | Cortex-M23 | Custom Board | ✅ | ✅ |
| 3 | Nuvoton | M2351 | M2351KIAAE | Cortex-M23 | NuMaker-PFM-M2351 | ✅ | ✅ |
| 4 | Nuvoton | M2354 | M2354LJFAE | Cortex-M23 | Custom Board | ✅ | ✅ |
| 5 | Nuvoton | M2354 | M2354SJFAE | Cortex-M23 | Custom Board | ✅ | ✅ |
| 6 | Nuvoton | M2354 | M2354KJFAE | Cortex-M23 | NuMaker-PFM-M2354 | ✅ | ✅ |
| 7 | STMicroelectronics | STM32H563 | STM32H563ZI | Cortex-M33 | NUCLEO-H563ZI | ✅ | ✅ |
| 8 | STMicroelectronics | STM32H562 | STM32H562VG | Cortex-M33 | Custom Board | ✅ | In Preparation |
| 9 | Renesas | RA6 | R7FA6M4AF3CFB | Cortex-M33 | Custom Board | ✅ | In Preparation |
| 10 | Renesas | RA6 | R7FA6M5BH3CFC | Cortex-M33 | Custom Board | ✅ | In Preparation |
| 11 | Renesas | RA6 | R7FA6E10F2CFP | Cortex-M33 | Custom Board | ✅ | In Preparation |
| 12 | Renesas | RA4 | R7FA4M2AD3CFP | Cortex-M33 | Custom Board | ✅ | In Preparation |
| 13 | Renesas | RA4 | R7FA4M3AF3CFB | Cortex-M33 | Custom Board | ✅ | In Preparation |
| 14 | Renesas | RA4 | R7FA4E10D2CFM | Cortex-M33 | Custom Board | ✅ | In Preparation |

### Supported Cryptographic Algorithms

| Manufacturer | MCU Line | PQC | ARIA | AES | LEA | SHA | HMAC | Random Generator | TRNG | ECDSA | ECDH | PBKDF2 | HKDF | Key Management |
|--------|--------|:----:|:----:|:---:|:---:|:-------:|:----:|:-----------:|:----:|:-----:|:----:|:------:|:----:|:------:|
| Nuvoton | M2351 | ➖ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Nuvoton | M2354 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| STMicroelectronics | STM32H563 | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |

| Item | Algorithms |
|------|--------------|
| PQC DSA (NIST) | ML-DSA-44 (Dilithium2), SLH-DSA-Shake128f (SPHINCS+), FN-DSA-512 (Falcon-512) |
| PQC KEM (NIST) | ML-KEM-512 (Kyber-512) |
| K-PQC DSA | AIMer-128f, HAETAE-2 |
| K-PQC KEM | NTRU-768, SMAUG-1 |
| ARIA | ARIA-128 / 192 / 256, CBC / CTR / GCM |
| AES | AES-128 / 192 / 256, CBC / CTR / GCM |
| LEA | LEA-128 / 192 / 256, CBC / CTR / GCM |
| SHA | SHA-256 |
| HMAC | HMAC-SHA-256 |
| Random Generator | Hash_DRBG (SHA-256) |
| TRNG | True Random Number Generator (Hardware RNG) |
| ECDSA | ECDSA P-256 |
| ECDH | ECDH P-256 |
| PBKDF2 | PBKDF2-HMAC-SHA-256 |
| HKDF | HKDF-SHA-256 |
| Key Management | Key Generation / Storage / Deletion / Retrieval |

---

## AxioCryptoM v2.2.0 (Upcoming)

### Updates
Changed to support AES in certification mode.

### Supported Platforms

Refer to the README of each MCU line for details and usage instructions.

| # | Manufacturer | MCU Line | Part Number | Core | Board | KCMVP Cert. | Sample Code |
|:---:|--------|--------|---------|-----|------|-------------|----------|
| 1 | Nuvoton | M2351 | M2351ZIAAE | Cortex-M23 | Custom Board | In Preparation | In Preparation |
| 2 | Nuvoton | M2351 | M2351SIAAE | Cortex-M23 | Custom Board | In Preparation | In Preparation |
| 3 | Nuvoton | M2351 | M2351KIAAE | Cortex-M23 | NuMaker-PFM-M2351 | In Preparation | In Preparation |
| 4 | Nuvoton | M2354 | M2354LJFAE | Cortex-M23 | Custom Board | In Preparation | In Preparation |
| 5 | Nuvoton | M2354 | M2354SJFAE | Cortex-M23 | Custom Board | In Preparation | In Preparation |
| 6 | Nuvoton | M2354 | M2354KJFAE | Cortex-M23 | NuMaker-PFM-M2354 | In Preparation | In Preparation |
| 7 | STMicroelectronics | STM32F207 | STM32F207ZG | Cortex-M3 | NUCLEO-F207ZG | In Preparation | In Preparation |
| 8 | STMicroelectronics | STM32F303 | STM32F303RE | Cortex-M4 | NUCLEO-F303RE | In Preparation | In Preparation |
| 9 | STMicroelectronics | STM32F401 | STM32F401RE | Cortex-M4 | NUCLEO-F401RE | In Preparation | In Preparation |
| 10 | STMicroelectronics | STM32F767 | STM32F767ZI | Cortex-M7 | NUCLEO-F767ZI | In Preparation | In Preparation |
| 11 | STMicroelectronics | STM32G0B1 | STM32G0B1RE | Cortex-M0+ | NUCLEO-G0B1RE | In Preparation | In Preparation |
| 12 | STMicroelectronics | STM32G474 | STM32G474RE | Cortex-M4 | NUCLEO-G474RE | In Preparation | In Preparation |
| 13 | STMicroelectronics | STM32H563 | STM32H563ZI | Cortex-M33 | NUCLEO-H563ZI | In Preparation | In Preparation |
| 14 | STMicroelectronics | STM32H563 | STM32H563ZG | Cortex-M33 | NUCLEO-H563ZI | In Preparation | In Preparation |
| 15 | STMicroelectronics | STM32H562 | STM32H562VG | Cortex-M33 | Custom Board | In Preparation | In Preparation |
| 16 | STMicroelectronics | STM32H562 | STM32H562VI | Cortex-M33 | Custom Board | In Preparation | In Preparation |
| 17 | STMicroelectronics | STM32H753 | STM32H753ZI | Cortex-M7 | NUCLEO-H753ZI | In Preparation | In Preparation |
| 18 | STMicroelectronics | STM32L152 | STM32L152RE | Cortex-M3 | NUCLEO-L152RE | In Preparation | In Preparation |
| 19 | STMicroelectronics | STM32L452 | STM32L452RE | Cortex-M4 | NUCLEO-L452RE-P | In Preparation | In Preparation |
| 20 | STMicroelectronics | STM32L476 | STM32L476RG | Cortex-M4 | NUCLEO-L476RG | In Preparation | In Preparation |
| 21 | STMicroelectronics | STM32L496 | STM32L496ZG | Cortex-M4 | NUCLEO-L496ZG-P | In Preparation | In Preparation |
| 22 | STMicroelectronics | STM32L4R5 | STM32L4R5ZI | Cortex-M4 | NUCLEO-L4R5ZI-P | In Preparation | In Preparation |
| 23 | STMicroelectronics | STM32L552 | STM32L552ZE | Cortex-M33 | NUCLEO-L552ZE-Q | In Preparation | In Preparation |
| 24 | STMicroelectronics | STM32U385 | STM32U385RG | Cortex-M33 | NUCLEO-U385RG-Q | In Preparation | In Preparation |
| 25 | STMicroelectronics | STM32U545 | STM32U545RE | Cortex-M33 | NUCLEO-U545RE-Q | In Preparation | In Preparation |
| 26 | STMicroelectronics | STM32U575 | STM32U575ZI | Cortex-M33 | NUCLEO-U575ZI-Q | In Preparation | In Preparation |
| 27 | STMicroelectronics | STM32WB55 | STM32WB55CG | Dual Core (M4+M0+) | P-NUCLEO-WB55 | In Preparation | In Preparation |
| 28 | STMicroelectronics | STM32WBA52 | STM32WBA52CG | Cortex-M33 | NUCLEO-WBA52CG | In Preparation | In Preparation |
| 29 | STMicroelectronics | STM32WL55 | STM32WL55JC | Dual Core (M4+M0+) | NUCLEO-WL55JC1 | In Preparation | In Preparation |
| 30 | Renesas | RA6 | R7FA6M4AF3CFB | Cortex-M33 | Custom Board | In Preparation | In Preparation |
| 31 | Renesas | RA6 | R7FA6M5BH3CFC | Cortex-M33 | Custom Board | In Preparation | In Preparation |
| 32 | Renesas | RA6 | R7FA6E10F2CFP | Cortex-M33 | Custom Board | In Preparation | In Preparation |
| 33 | Renesas | RA4 | R7FA4M2AD3CFP | Cortex-M33 | Custom Board | In Preparation | In Preparation |
| 34 | Renesas | RA4 | R7FA4M3AF3CFB | Cortex-M33 | Custom Board | In Preparation | In Preparation |
| 35 | Renesas | RA4 | R7FA4E10D2CFM | Cortex-M33 | Custom Board | In Preparation | In Preparation |
| 36 | Microchip | PIC32CX-MT | PIC32CXMTSH | Dual Core (M4+M0+) | PIC32CXMTSH-DB | In Preparation | In Preparation |
| 37 | Microchip | PIC32CX-MT | PIC32CXMTC | Dual Core (M4+M0+) | PIC32CXMTC-DB | In Preparation | In Preparation |

> **Note:** For STMicroelectronics product families, operation is guaranteed across all sub-part numbers within the same MCU line.  
> e.g.) `STM32H563` line → STM32H563**AG** / **AI** / **IG** / **II** / **LI** / **MI** / **RG** / **RI** / **VG** / **VI** / **ZG** / **ZI**, etc.


### Supported Cryptographic Algorithms


| Manufacturer | MCU Line | PQC | ARIA | AES | LEA | SHA | HMAC | Random Generator | TRNG | ECDSA | ECDH | PBKDF2 | HKDF | Key Management |
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


| Item | Algorithms |
|------|--------------|
| PQC DSA (NIST) | ML-DSA-44 (Dilithium2), SLH-DSA-Shake128f (SPHINCS+), FN-DSA-512 (Falcon-512) |
| PQC KEM (NIST) | ML-KEM-512 (Kyber-512) |
| K-PQC DSA | AIMer-128f, HAETAE-2 |
| K-PQC KEM | NTRU-768, SMAUG-1 |
| ARIA | ARIA-128 / 192 / 256, CBC / CTR / GCM |
| AES | AES-128 / 192 / 256, CBC / CTR / GCM |
| LEA | LEA-128 / 192 / 256, CBC / CTR / GCM |
| SHA | SHA-256 |
| HMAC | HMAC-SHA-256 |
| Random Generator | Hash_DRBG (SHA-256) |
| TRNG | True Random Number Generator (Hardware RNG) |
| ECDSA | ECDSA P-256 |
| ECDH | ECDH P-256 |
| PBKDF2 | PBKDF2-HMAC-SHA-256 |
| HKDF | HKDF-SHA-256 |
| Key Management | Key Generation / Storage / Deletion / Retrieval |

---

## License
This library and sample source code may be freely used for personal purposes only.  
Commercial use, redistribution, modification, unauthorized copying, and reverse engineering are prohibited.  
For commercial licensing inquiries, please contact Security Platform Inc.

---

## Usage Restrictions

This AxioCryptoM library is a **public (Evaluation)** version and has limitations on the number of API calls.  
For lifting restrictions and commercial licensing inquiries, please contact Security Platform Inc.



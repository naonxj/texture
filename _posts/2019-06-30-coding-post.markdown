---
layout: post
title:  "NETWORK SECURITY PROJECT"
description: personal project
date:   2025-08-11 15:03:36 +0530
categories: GNS3 pfSense Rocky Ubuntu kali OSSEC ZABBIX
---

본 프로젝트는 GNS3 환경에서 방화벽, VPN, NIDS, HIDS, 모니터링 툴을 통합 적용하여 다양한 네트워크 보안 시나리오를 실습하고 결과를 정리한 것입니다. 각 항목별로 구성도, 규칙, 실행 결과 캡처를 포함하였습니다.

![포폴로지](assets/images/개인과제 - 네트워크.PNG)

---

## GNS3 상세
![GNS3 상세 1](사진_URL "GNS3 상세 1")
![GNS3 상세 2](사진_URL "GNS3 상세 2")

---

## Firewall Rule

1. **Firefox3 → inside** : http, telnet 접속  
   ![결과 1](사진_URL)

2. **Webterm2 → dmz** : telnet 접속  
   ![결과 2](사진_URL)

3. **PC1 → Webterm1** : ping 가능  
   ![결과 3](사진_URL)

4. **Webterm1 → R1** : http, telnet 가능  
   ![결과 4](사진_URL)

5. **Webterm2 → PC1** : ping 가능  
   ![결과 5](사진_URL)

---

## openVPN
![OpenVPN 성공](사진_URL)

---

## Snort / Suricata Rule

1. Win10 → OSSEC : http, ping 탐지  
2. CentOS7 → Win10 : ping 탐지  
3. HIDS → CentOS7 : `/etc/passwd` command injection 공격 탐지  
4. Kali → Win10 : Rand Source Attack DDoS 탐지  
5. Kali → CentOS7 : SYN Flag Scanning 탐지  

---

## SNORT 실행 결과
![Snort 결과 1](사진_URL)
![Snort 결과 2](사진_URL)
![Snort 결과 3](사진_URL)
![Snort 결과 4](사진_URL)
![Snort 결과 5](사진_URL)

---

## Suricata 실행 결과
![Suricata 결과 1](사진_URL)
![Suricata 결과 2](사진_URL)
![Suricata 결과 3](사진_URL)
![Suricata 결과 4](사진_URL)
![Suricata 결과 5](사진_URL)

---

## OSSEC
**Server**  
![OSSEC Server](사진_URL)

**Agent**  
![OSSEC Agent](사진_URL)

**Windows**  
![OSSEC Windows](사진_URL)

---

## Zabbix
**Server**  
![Zabbix Server](사진_URL)

**Agent**  
![Zabbix Agent](사진_URL)

**Windows**  
![Zabbix Windows](사진_URL)

---

*본 페이지의 모든 이미지는 클릭하면 원본 크기로 볼 수 있습니다.*

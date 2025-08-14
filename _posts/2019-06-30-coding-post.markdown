---
layout: post
title:  "NETWORK SECURITY PROJECT"
description: personal project
date:   2025-08-11 15:03:36 +0530
categories: GNS3 pfSense Rocky Ubuntu kali OSSEC ZABBIX
---

본 프로젝트는 GNS3 환경에서 방화벽, VPN, NIDS, HIDS, 모니터링 툴을 통합 적용하여 다양한 네트워크 보안 시나리오를 실습하고 결과를 정리한 것입니다. 각 항목별로 구성도, 규칙, 실행 결과 캡처를 포함하였습니다.

![GNS3 상세 1]({{ site.baseurl }}/assets/images/popo.PNG)

---

## GNS3 상세

![GNS3 상세 2]({{ site.baseurl }}/assets/images/popo2.PNG)

---

## Firewall Rule

1. **Firefox3 → inside** : http, telnet 접속  
- http

   ![결과 1]({{ site.baseurl }}/assets/images/fire3-inside-http.PNG)
  
- telnet
  
   ![결과 1]({{ site.baseurl }}/assets/images/fire3-inside-telnet.PNG)
  
2. **Webterm2(firefox5) → dmz** : telnet 접속  
   ![결과 2]({{ site.baseurl }}/assets/images/fire5-dmz-telnet.PNG)

3. **PC1 → Webterm1(firefox4)** : ping 가능  
   ![결과 3]({{ site.baseurl }}/assets/images/pc1-fire4-ping.PNG)

4. **Webterm1(firefox4) → R1** : http, telnet 가능  
- http

  ![결과 4]({{ site.baseurl }}/assets/images/web1(fire4)-r1http3333.PNG)
  
- telnet

  ![결과 4]({{ site.baseurl }}/assets/images/web1(fire4)-r1telnet2222.PNG)
  
5. **Webterm2(firefox5) → PC1** : ping 가능  
   ![결과 5]({{ site.baseurl }}/assets/images/web2(fire5)-pc1-ping-kkk.PNG)

---
## HSRP
1. active

![결과 5]({{ site.baseurl }}/assets/images/HSRP-active.PNG)

2. standby

![결과 5]({{ site.baseurl }}/assets/images/HSRP-standby.PNG)

---

## openVPN

![OpenVPN 성공]({{ site.baseurl }}/assets/images/openvpn.PNG)

---

## Snort / Suricata Rule

1. Win10 → OSSEC : http, ping 탐지  
2. CentOS7 → Win10 : ping 탐지  
3. HIDS → CentOS7 : `/etc/passwd` command injection 공격 탐지  
4. Kali → Win10 : Rand Source Attack DDoS 탐지  
5. Kali → CentOS7 : SYN Flag Scanning 탐지  

---

## SNORT 실행 결과

1. Win10 → OSSEC : http, ping 탐지  

- http

![Snort 결과 1]({{ site.baseurl }}/assets/images/snort(win10-ossec)http.PNG)

-ping

![Snort 결과 1]({{ site.baseurl }}/assets/images/snort(win10-ossec)ping-cmd.PNG)
![Snort 결과 1]({{ site.baseurl }}/assets/images/snort(win10-ossec)ping.PNG)

2. CentOS7 → Win10 : ping 탐지  

![Snort 결과 2]({{ site.baseurl }}/assets/images/rocky-win-ping.PNG)
![Snort 결과 2]({{ site.baseurl }}/assets/images/rocky-win-ping-result.PNG)

3. HIDS → CentOS7 : `/etc/passwd` command injection 공격 탐지

![Snort 결과 3]({{ site.baseurl }}/assets/images/rockinjectcurl.PNG)
![Snort 결과 3]({{ site.baseurl }}/assets/images/rockyinjectiondetc.PNG)

4. Kali → Win10 : Rand Source Attack DDoS 탐지

![Snort 결과 4]({{ site.baseurl }}/assets/images/random-attack.PNG)
![Snort 결과 4]({{ site.baseurl }}/assets/images/kali-winrandattack444444.PNG)

5. Kali → CentOS7 : SYN Flag Scanning 탐지

![Snort 결과 5]({{ site.baseurl }}/assets/images/synflagattack.PNG)
![Snort 결과 5]({{ site.baseurl }}/assets/images/suri-kali-rocky-syn-attack-det.PNG)

---

## Suricata 실행 결과

1. Win10 → OSSEC : http, ping 탐지  

- ping

![Snort 결과 1]({{ site.baseurl }}/assets/images/suriwin-ossec-ping.PNG)
![Snort 결과 1]({{ site.baseurl }}/assets/images/surwin-ossec-pingdetect.PNG)

- http

![Snort 결과 1]({{ site.baseurl }}/assets/images/win-ossechttpdet.PNG)

2. CentOS7 → Win10 : ping 탐지  

![Snort 결과 2]({{ site.baseurl }}/assets/images/surirocky-win-ping.PNG)
![Snort 결과 2]({{ site.baseurl }}/assets/images/surirocky-winping-det.PNG)

3. HIDS → CentOS7 : `/etc/passwd` command injection 공격 탐지

![Snort 결과 3]({{ site.baseurl }}/assets/images/suri-injection-attack.PNG)
![Snort 결과 3]({{ site.baseurl }}/assets/images/suri-injection-detec.PNG)

4. Kali → Win10 : Rand Source Attack DDoS 탐지

![Snort 결과 4]({{ site.baseurl }}/assets/images/surikali-win-randattack2.PNG)
![Snort 결과 4]({{ site.baseurl }}/assets/images/surikali-winrandattack.PNG)

5. Kali → CentOS7 : SYN Flag Scanning 탐지

![Snort 결과 5]({{ site.baseurl }}/assets/images/surikali-rocky-synattack.PNG)
![Snort 결과 5]({{ site.baseurl }}/assets/images/suri-kali-rocky-syn-attack-det.PNG)

---

## OSSEC
**Server**  

![OSSEC Server]({{ site.baseurl }}/assets/images/ossecserver.png)
![OSSEC Server]({{ site.baseurl }}/assets/images/ossecserver2.png)

**Agent**  

![OSSEC Agent]({{ site.baseurl }}/assets/images/ossecagent.png)

**Windows**  

![OSSEC Windows]({{ site.baseurl }}/assets/images/windowossec1.PNG)
![OSSEC Windows]({{ site.baseurl }}/assets/images/windowossec4tail.PNG)
![OSSEC Windows]({{ site.baseurl }}/assets/images/ossecwindowfinal.png)

---

## Zabbix
**Server**  

![Zabbix Server]({{ site.baseurl }}/assets/images/zabbixhome.PNG)

**Agent/windows**  

![Zabbix Agent]({{ site.baseurl }}/assets/images/zabbixwindowre.PNG)

---

*본 페이지의 모든 이미지는 클릭하면 원본 크기로 볼 수 있습니다.*


---

*본 페이지의 모든 이미지는 클릭하면 원본 크기로 볼 수 있습니다.*

---
layout: post
title:  "NETWORK SECURITY PROJECT"
description: personal project
date:   2025-08-11 15:03:36 +0530
categories: GNS3 pfSense Rocky Ubuntu kali OSSEC ZABBIX
---
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Network Security Lab</title>
<style>
    body {
        font-family: Arial, sans-serif;
        line-height: 1.6;
        margin: 20px;
        background-color: #f8f9fa;
    }
    h1, h2, h3 {
        margin-top: 20px;
    }
    .section {
        margin-bottom: 40px;
        padding: 15px;
        background: white;
        border-radius: 8px;
        box-shadow: 0 0 5px rgba(0,0,0,0.1);
    }
    .img-container {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
    }
    .img-container img {
        max-width: 300px;
        cursor: pointer;
        border-radius: 5px;
        transition: transform 0.3s;
    }
    .img-container img:hover {
        transform: scale(1.05);
    }
    .divider {
        border-top: 2px solid #ccc;
        margin: 40px 0;
    }
    .resizable-text {
        font-size: 16px;
    }
    /* 큰 이미지 모달 */
    .modal {
        display: none;
        position: fixed;
        z-index: 999;
        padding-top: 60px;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        overflow: auto;
        background-color: rgba(0,0,0,0.8);
    }
    .modal-content {
        margin: auto;
        display: block;
        max-width: 90%;
    }
    .close {
        position: absolute;
        top: 20px;
        right: 35px;
        color: white;
        font-size: 40px;
        font-weight: bold;
        cursor: pointer;
    }
</style>
</head>
<body>

<h1>Network Security Lab</h1>

<div class="section">
    <h2>포폴로지 (Topology)</h2>
    <div class="img-container">
        <img src="여기에_포폴로지사진_URL" alt="포폴로지" onclick="openModal(this.src)">
    </div>
</div>

<div class="divider"></div>

<div class="section">
    <h2>GNS3</h2>
    <div class="img-container">
        <img src="여기에_GNS3_사진1_URL" alt="GNS3 상세 1" onclick="openModal(this.src)">
        <img src="여기에_GNS3_사진2_URL" alt="GNS3 상세 2" onclick="openModal(this.src)">
    </div>
</div>

<div class="divider"></div>

<div class="section">
    <h2>Firewall Rule</h2>
    <div class="resizable-text">
        <p>1. Firefox3 - inside : http, telnet 접속</p>
        <div class="img-container">
            <img src="사진_URL" onclick="openModal(this.src)">
        </div>
        <p>2. Webterm2 - dmz : telnet 접속</p>
        <div class="img-container">
            <img src="사진_URL" onclick="openModal(this.src)">
        </div>
        <p>3. PC1 -> Webterm1 : ping 가능</p>
        <div class="img-container">
            <img src="사진_URL" onclick="openModal(this.src)">
        </div>
        <p>4. Webterm1 -> R1 : http, telnet 가능</p>
        <div class="img-container">
            <img src="사진_URL" onclick="openModal(this.src)">
        </div>
        <p>5. Webterm2 -> PC1 : Ping 가능</p>
        <div class="img-container">
            <img src="사진_URL" onclick="openModal(this.src)">
        </div>
    </div>
</div>

<div class="divider"></div>

<div class="section">
    <h2>openVPN</h2>
    <div class="img-container">
        <img src="사진_URL" onclick="openModal(this.src)">
    </div>
</div>

<div class="divider"></div>

<div class="section">
    <h2>Snort / Suricata Rule</h2>
    <div class="resizable-text">
        <p>1. Win10 -> OSSEC : http, ping 탐지</p>
        <p>2. CentOS7 -> Win10 : ping 탐지</p>
        <p>3. HIDS -> CentOS7 : /etc/passwd command injection 공격탐지</p>
        <p>4. Kali -> Win10 : Rand Source Attack DDos 공격 탐지</p>
        <p>5. Kali -> CentOS7: SYN Flag Scanning 탐지</p>
    </div>
</div>

<div class="divider"></div>

<div class="section">
    <h2>SNORT</h2>
    <div class="img-container">
        <img src="사진_URL" onclick="openModal(this.src)">
        <!-- 1~5번 각 실행완료 사진 반복 -->
    </div>
</div>

<div class="divider"></div>

<div class="section">
    <h2>Suricata</h2>
    <div class="img-container">
        <img src="사진_URL" onclick="openModal(this.src)">
        <!-- 1~5번 각 실행완료 사진 반복 -->
    </div>
</div>

<div class="divider"></div>

<div class="section">
    <h2>OSSEC</h2>
    <h3>Server</h3>
    <div class="img-container">
        <img src="사진_URL" onclick="openModal(this.src)">
    </div>
    <h3>Agent</h3>
    <div class="img-container">
        <img src="사진_URL" onclick="openModal(this.src)">
    </div>
    <h3>Windows</h3>
    <div class="img-container">
        <img src="사진_URL" onclick="openModal(this.src)">
    </div>
</div>

<div class="divider"></div>

<div class="section">
    <h2>Zabbix</h2>
    <h3>Server</h3>
    <div class="img-container">
        <img src="사진_URL" onclick="openModal(this.src)">
    </div>
    <h3>Agent</h3>
    <div class="img-container">
        <img src="사진_URL" onclick="openModal(this.src)">
    </div>
    <h3>Windows</h3>
    <div class="img-container">
        <img src="사진_URL" onclick="openModal(this.src)">
    </div>
</div>

<!-- 모달 영역 -->
<div id="imgModal" class="modal">
    <span class="close" onclick="closeModal()">&times;</span>
    <img class="modal-content" id="modalImage">
</div>

<script>
function openModal(src) {
    document.getElementById('imgModal').style.display = "block";
    document.getElementById('modalImage').src = src;
}
function closeModal() {
    document.getElementById('imgModal').style.display = "none";
}
</script>

</body>
</html>

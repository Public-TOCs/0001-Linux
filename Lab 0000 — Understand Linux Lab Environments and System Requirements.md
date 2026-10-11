# 🐧 Lab 0000 — Understand Linux Lab Environments and System Requirements

Vyomanant Academy | Linux Administration and Production Troubleshooting

Learn about Linux lab environments, understand hardware and software requirements, and identify the best platform for hands-on Linux administration and DevOps training.

# 🌍 Lab Overview

Before you start learning Linux commands, shell scripting, system administration, or production troubleshooting, you need a reliable Linux lab environment.

A Linux lab environment is a dedicated system where you can safely practice Linux administration without affecting production infrastructure.

In this lab, you will explore different Linux environments, compare their capabilities, check your computer's hardware specifications, and select the environment best suited to your learning needs.

| Lab Information | Details                                       |
| --------------- | --------------------------------------------- |
| 🆔 Lab ID       | 0000                                          |
| 📚 Module       | Module 0 — Linux Lab Setup                    |
| 🎯 Difficulty   | Beginner                                      |
| ⏱️ Duration     | 30–45 Minutes                                 |
| 🐧 Target OS    | Ubuntu Server 26.04 LTS                       |
| 💻 Platforms    | VirtualBox, VMware, WSL2, AWS EC2, Killercoda |
| 🧪 Lab Type     | Environment Planning and System Verification  |
| 💰 Cost         | Free local options; AWS charges may apply     |

Note: This is a foundational preparation lab. You are not required to install Linux yet.

# 🎯 Learning Objectives

By the end of this lab, you will be able to:

- ✅ Explain what a Linux lab environment is.
- ✅ Identify different ways to run Linux.
- ✅ Understand virtualization and virtual machines.
- ✅ Differentiate VirtualBox, VMware, WSL2, AWS EC2, and browser-based labs.
- ✅ Identify minimum and recommended system requirements.
- ✅ Check your computer's CPU, RAM, disk capacity, and virtualization support.
- ✅ Understand common virtual networking modes.
- ✅ Select an appropriate Linux lab environment.
- ✅ Prepare your system for upcoming Linux administration labs.

# 🧰 Prerequisites

You should have:

- 💻 A laptop or desktop computer.
- 🌐 An internet connection.
- 🔐 Administrator access to your computer for future installation activities.
- 🧠 Basic knowledge of using Windows, Linux, or macOS.
- ☁️ An AWS account only if you plan to use AWS EC2.

No previous Linux experience is required.

# 💻 Recommended Hardware Requirements

For a beginner-friendly Ubuntu Server lab environment, use the following practical specifications.

| Component         | Minimum Practical Setup         | Recommended                     |
| ----------------- | ------------------------------- | ------------------------------- |
| CPU               | 2 CPU cores                     | 4 or more cores                 |
| RAM               | 8 GB                            | 16 GB or more                   |
| Available Storage | 30 GB                           | 60–100 GB                       |
| Architecture      | Compatible 64-bit CPU           | x86-64 or supported ARM64       |
| Virtualization    | Supported by CPU and hypervisor | Hardware virtualization enabled |
| Internet          | Broadband                       | Stable broadband                |
| VM Memory         | 2 GB                            | 4 GB                            |
| VM CPU            | 2 vCPUs                         | 2–4 vCPUs                       |

These are recommended training specifications, not Ubuntu's official installation minimums.

Ubuntu Server 26.04 LTS lists 1.5 GB of system memory and 5 GB of storage as baseline installation requirements, but additional resources are preferable for practical labs.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://ubuntu.com\&sz=32)

Ubuntu



💡 Recommendation: For Linux administration and troubleshooting labs, a computer with 16 GB RAM and a 4-core CPU provides a more comfortable experience when running local virtual machines.

# 🏗️ Lab Architecture

Linux can run in multiple environments.

```
                 ┌──────────────────────────┐
                 │    Student Computer      │
                 │ Windows / Linux / macOS  │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │ Select Linux Environment │
                 └────────────┬─────────────┘
                              │
          ┌───────────────────┼───────────────────┐
          │                   │                   │
          ▼                   ▼                   ▼
  ┌──────────────┐    ┌──────────────┐    ┌──────────────┐
  │ VirtualBox / │    │    WSL2      │    │   AWS EC2    │
  │ VMware VM    │    │  (Windows)   │    │   (Cloud)    │
  └──────┬───────┘    └──────┬───────┘    └──────┬───────┘
         │                   │                   │
         └───────────────────┼───────────────────┘
                             │
                             ▼
                 ┌──────────────────────────┐
                 │     Ubuntu Linux         │
                 │   Lab Environment        │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │ Linux Administration     │
                 │ Shell Scripting          │
                 │ Networking & SSH         │
                 │ Production Troubleshoot  │
                 │ DevOps Fundamentals      │
                 └──────────────────────────┘

Alternative: Browser-Based Linux Labs (Killercoda)
```

# 🚀 Step-by-Step Instructions

# 🔹 Step 1 — Understand What a Linux Lab Environment Is

A Linux lab environment is a dedicated computer system where you can safely practice Linux commands and administrative operations.

In this course, you will perform activities such as:

- 🐧 Installing and configuring Linux.
- 👤 Creating users and groups.
- 📁 Managing files and directories.
- 🔐 Configuring Linux file permissions.
- 📦 Installing software packages.
- ⚙️ Managing system services.
- 🌐 Configuring Linux networking.
- 🔑 Connecting to remote servers using SSH.
- 📜 Writing shell scripts.
- 🔍 Troubleshooting Linux issues.

A dedicated lab helps protect your main computer and production systems from accidental changes.

# 🔹 Step 2 — Understand Different Linux Lab Environments

# 🖥️ Option 1 — Virtual Machine (VM)

A virtual machine is a software-defined computer that runs inside another computer.

Virtualization software allows you to run Ubuntu Linux as a guest operating system while continuing to use your existing host operating system.

Common virtualization platforms include:

- Oracle VirtualBox
- VMware Workstation
- VMware Fusion
- Hyper-V

Example architecture:

```
Physical Laptop
│
├── Host Operating System
│   └── Windows 11
│
├── Virtualization Software
│   └── Oracle VirtualBox
│
└── Virtual Machine
    └── Ubuntu Server 26.04 LTS
        ├── Linux Kernel
        ├── Terminal
        ├── System Services
        └── Linux Administration Tools
```

Advantages

- ✅ Full Linux operating system.
- ✅ Suitable for most Linux administration labs.
- ✅ Supports VM snapshots and recovery.
- ✅ Allows experimentation with storage and networking.
- ✅ Does not require a cloud account.

Limitations

- ⚠️ Requires sufficient CPU, RAM, and disk space.
- ⚠️ Requires a compatible hypervisor and CPU architecture.
- ⚠️ Running multiple VMs can slow down the host computer.

Best suited for: Complete Linux administration, networking, storage, and production troubleshooting training.

# 🪟 Option 2 — Windows Subsystem for Linux (WSL2)

WSL2 allows Windows users to run Linux distributions directly within Windows using lightweight virtualization.

It is especially useful for learning Linux commands and DevOps development workflows.

Example architecture:

```
Windows Laptop
│
├── Windows Operating System
│
├── Windows Subsystem for Linux 2
│
└── Ubuntu Linux
    ├── Bash Terminal
    ├── Linux Commands
    ├── Shell Scripts
    ├── Git
    └── Development Tools
```

Advantages

- ✅ Convenient for Windows users.
- ✅ No traditional VM setup required.
- ✅ Supports Linux command-line tools.
- ✅ Useful for Bash scripting and development.
- ✅ Integrates with Windows Terminal and VS Code.

Limitations

- ⚠️ Not identical to a conventional full Linux VM.
- ⚠️ Certain kernel, bootloader, and hardware-level labs are unsuitable.
- ⚠️ Requires supported Windows and virtualization capabilities.

Best suited for: Linux fundamentals, shell scripting, Git, and DevOps development.

Microsoft documents WSL2 installation and supported Windows requirements in its official installation guide.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://learn.microsoft.com\&sz=32)

Microsoft Learn



# ☁️ Option 3 — AWS EC2 Linux Instance

Amazon EC2 allows you to create Linux virtual servers in AWS.

Instead of running Linux on your laptop, you connect to a remotely hosted Linux server.

Example architecture:

```
Local Laptop
│
├── SSH Client
│   ├── Windows Terminal
│   ├── MobaXterm
│   └── VS Code Remote SSH
│
└── Internet
    │
    ▼
AWS Cloud
│
└── Virtual Private Cloud (VPC)
    │
    └── EC2 Instance
        │
        └── Ubuntu Server
            ├── SSH Server
            ├── Linux Services
            ├── Users and Groups
            └── Networking Tools
```

Advantages

- ✅ Experience with real cloud infrastructure.
- ✅ Remote server administration practice.
- ✅ SSH and networking experience.
- ✅ Suitable for cloud and DevOps training.
- ✅ No requirement for a powerful local computer.

Limitations

- ⚠️ AWS charges may apply.
- ⚠️ Requires an internet connection.
- ⚠️ Requires basic cloud networking knowledge.
- ⚠️ Incorrect security configurations may expose services.

Best suited for: Cloud administration, SSH, remote Linux management, and AWS-based DevOps labs.

# 🌐 Option 4 — Browser-Based Linux Environment

Browser-based platforms allow users to access Linux terminals without installing Linux locally.

One example is Killercoda.

Example architecture:

```
Student Laptop
│
└── Web Browser
    │
    ▼
Killercoda Platform
│
└── Temporary Lab Environment
    │
    ├── Linux Terminal
    ├── Linux Commands
    └── Practice Exercises
```

Advantages

- ✅ Minimal local setup.
- ✅ Convenient for quick demonstrations.
- ✅ Useful for basic command practice.
- ✅ Accessible from a browser.

Limitations

- ⚠️ Lab sessions may expire.
- ⚠️ Changes may not persist.
- ⚠️ Internet connectivity is required.
- ⚠️ Some privileged system operations may not be supported.

Best suited for: Quick Linux exercises, demonstrations, and introductory training.

# 🔹 Step 3 — Compare Linux Lab Platforms

| Feature                       | Virtual Machine | WSL2                 | AWS EC2 | Browser Lab        |
| ----------------------------- | --------------- | -------------------- | ------- | ------------------ |
| Full OS installation practice | ✅               | ❌                    | Limited | ❌                  |
| Linux command practice        | ✅               | ✅                    | ✅       | ✅                  |
| Shell scripting               | ✅               | ✅                    | ✅       | ✅                  |
| Networking labs               | ✅               | Partial              | ✅       | Limited            |
| Storage administration        | ✅               | Limited              | ✅       | Limited            |
| SSH practice                  | ✅               | ✅                    | ✅       | Varies             |
| Snapshots/recovery            | ✅               | Different mechanisms | ✅       | Varies             |
| Internet required during use  | No              | No                   | Yes     | Yes                |
| Local installation            | Required        | Required             | No      | No                 |
| Potential cloud charges       | No              | No                   | Yes     | Platform-dependent |

🎯 Recommended lab environment

For Vyomanant Academy's Linux Administration and Production Troubleshooting course:

- Primary: Ubuntu Server running in VirtualBox or VMware.
- Secondary: Ubuntu Server running on AWS EC2.
- Alternative: WSL2 for Windows users.
- Quick practice: Browser-based Linux terminals.

# 🔹 Step 4 — Understand Basic Linux Infrastructure Terminology

Before setting up Linux, understand these important terms.

| Term            | Explanation                                                  |
| --------------- | ------------------------------------------------------------ |
| Host Machine    | Physical computer running the virtualization software        |
| Host OS         | Operating system installed on your physical computer         |
| Guest OS        | Operating system installed inside a virtual machine          |
| Hypervisor      | Technology that creates and manages virtual machines         |
| Virtual Machine | Software-defined computer system                             |
| ISO File        | Installation image used to install an operating system       |
| vCPU            | Virtual processing capacity allocated to a VM                |
| RAM             | Memory used by running applications and the operating system |
| Virtual Disk    | Storage allocated to a VM                                    |
| Snapshot        | Recoverable record of supported VM state                     |
| SSH             | Secure Shell protocol for remote access                      |
| IP Address      | Network address assigned to an interface                     |
| Terminal        | Text-based command execution interface                       |
| Root User       | Privileged Linux administrator account                       |
| sudo            | Mechanism for executing authorized privileged commands       |

# 🔹 Step 5 — Check Your Computer's System Specifications

Before installing Linux, verify that your computer has sufficient resources.

Follow the instructions appropriate for your operating system.

# 🪟 For Windows Users

1\. Open PowerShell

Press:

`Windows + R`

Type:

```
powershell
```

Press Enter.

2\. Check system information

```
systeminfo
```

This command displays information about your Windows operating system and computer hardware.

Look for:

- Processor details.
- Installed physical memory.
- Operating system architecture.
- Virtualization-related information.

3\. Check installed physical RAM

```
Get-CimInstance Win32_ComputerSystem | Select-Object TotalPhysicalMemory
```

The value is returned in bytes.

4\. Check CPU specifications

```
Get-CimInstance Win32_Processor | Select-Object Name,NumberOfCores,VirtualizationFirmwareEnabled
```

This displays your processor name, physical core count, and available firmware virtualization status information.

5\. Check available disk space

```
Get-PSDrive -PSProvider FileSystem
```

Review the available free space on the drive where you intend to store the VM.

6\. Check virtualization in Task Manager

1. Press `Ctrl + Shift + Esc`.
2. Open Performance.
3. Select CPU.
4. Locate Virtualization.
5. Check whether it displays Enabled.

✅ Expected Result

Your computer should ideally have:

- At least 8 GB RAM.
- A compatible 64-bit processor.
- Sufficient free disk space.
- Hardware virtualization available for your selected hypervisor.

# 🐧 For Linux Users

Open the Linux terminal.

1\. Check CPU information

```
lscpu
```

Displays CPU architecture, processor details, and supported CPU features.

2\. Check system memory

```
free -h
```

Displays memory information in a human-readable format.

3\. Check storage devices

```
lsblk
```

Displays disk and partition information.

4\. Check available disk space

```
df -h /
```

Displays used and available filesystem capacity for the root filesystem.

✅ Expected Result

Your Linux computer should have sufficient CPU, memory, and storage resources to run the selected virtual machine.

# 🍎 For macOS Users

Open Terminal.

1\. Check CPU architecture

```
uname -m
```

Common results:

- `arm64` — Apple Silicon architecture.
- `x86_64` — Intel 64-bit architecture.

2\. Check installed RAM

```
sysctl -n hw.memsize
```

Displays physical memory in bytes.

3\. Check available disk space

```
df -h /
```

Displays filesystem usage.

⚠️ Important: Apple Silicon users should select an ARM64-compatible Ubuntu image and virtualization platform. Not every x86-64 virtualization workflow is supported natively.

# 🔹 Step 6 — Understand Hardware Virtualization

Hardware virtualization allows supported processors and hypervisors to run virtual machines efficiently.

Common virtualization technologies include:

| Processor Platform | Virtualization Technology     |
| ------------------ | ----------------------------- |
| Intel x86-64       | Intel VT-x                    |
| AMD x86-64         | AMD-V                         |
| Supported ARM64    | ARM virtualization extensions |

On many computers, the relevant virtualization setting is available in the BIOS or UEFI firmware.

How to check on Windows

1. Open Task Manager.
2. Select Performance → CPU.
3. Find Virtualization.
4. Verify whether it is enabled.

If virtualization is disabled, enabling it may require firmware configuration.

⚠️ Corporate Laptop Warning: If your device is managed by your organization, contact the IT administrator before changing BIOS or UEFI settings.

# 🔹 Step 7 — Understand Virtual Machine Resource Allocation

When creating a virtual machine, you must allocate resources from the host computer.

Suppose your laptop has:

| Host Resource | Available Capacity   |
| ------------- | -------------------- |
| CPU           | 8 logical processors |
| RAM           | 16 GB                |
| Free Storage  | 100 GB               |

You could create an Ubuntu Server VM with:

| VM Resource     | Example Configuration   |
| --------------- | ----------------------- |
| Guest OS        | Ubuntu Server 26.04 LTS |
| vCPU            | 2                       |
| RAM             | 4 GB                    |
| Virtual Disk    | 30 GB                   |
| Network Adapter | NAT                     |

This allocation provides reasonable resources for many introductory Linux labs while leaving capacity for the host operating system.

💡 Best Practice: Avoid assigning all available CPU and memory resources to a virtual machine. Your host operating system also requires resources.

# 🔹 Step 8 — Understand Basic Virtual Machine Networking

Virtual machines need network connectivity for package installation, SSH access, and networking exercises.

The following networking modes are commonly available.

| Network Mode | Description                                                      | Common Use                |
| ------------ | ---------------------------------------------------------------- | ------------------------- |
| NAT          | Guest accesses external networks through translated connectivity | Internet access           |
| Bridged      | Guest connects directly to the external network                  | LAN connectivity          |
| Host-only    | Guest communicates on an isolated host-side network              | Private lab communication |

Recommended beginner configuration: NAT.

NAT generally allows the Ubuntu VM to access the internet for package installation.

However, host-to-guest SSH access may require port forwarding or an additional network adapter, depending on the hypervisor.

# 🔹 Step 9 — Select Your Preferred Linux Lab Environment

Choose the environment based on your available system resources and learning objectives.

| Scenario                                   | Recommended Environment                     |
| ------------------------------------------ | ------------------------------------------- |
| Windows laptop with 16 GB RAM              | VirtualBox / VMware                         |
| Windows laptop focused on shell scripting  | WSL2                                        |
| Linux desktop with adequate resources      | VirtualBox / VMware                         |
| Mac with compatible hypervisor             | Ubuntu ARM64 or x86-64 VM, as appropriate   |
| Low-specification laptop                   | Browser lab or appropriately sized cloud VM |
| Learning AWS administration                | AWS EC2                                     |
| Learning Linux boot and storage management | Full virtual machine                        |
| Quick classroom demonstration              | Browser lab                                 |

🎯 For this course: A full Ubuntu Server virtual machine is the preferred environment because it supports a broad range of Linux administration and troubleshooting exercises.

# 🔹 Step 10 — Understand Lab Safety Best Practices

Before beginning hands-on Linux administration training, follow these practices.

🔐 Security

- Use dedicated lab credentials.
- Avoid using production passwords.
- Restrict remote access where applicable.
- Do not expose unnecessary services to the internet.

💾 Recovery

- Create VM snapshots before risky operations.
- Maintain backups of important lab files.
- Document configuration changes.
- Learn how to restore the environment.

☁️ Cloud Cost Management

- Understand AWS EC2 pricing.
- Configure budgets and billing alerts.
- Stop or terminate unused instances as appropriate.
- Remove unused storage and network resources when no longer needed.

🛡️ Safe Practice

- Never run untrusted scripts blindly.
- Practice destructive operations only in disposable lab environments.
- Avoid modifying production servers during training.
- Use authorized environments for security and networking experiments.

# 🔎 Verification

Complete these checks before proceeding to the next lab.

✅ System Readiness Checklist

- I understand what a Linux lab environment is.
- I can explain the difference between a host OS and guest OS.
- I understand the purpose of a hypervisor.
- I can identify the main Linux lab platforms.
- I have checked my computer's CPU specifications.
- I have checked available RAM.
- I have checked available storage space.
- I have checked virtualization support.
- I understand basic VM networking modes.
- I have selected my preferred Linux lab environment.
- I understand basic security and recovery precautions.

# 🧪 Knowledge Check

Answer the following questions.

Question 1: What is the primary purpose of a hypervisor?

A. To manage Linux users B. To create and run virtual machines C. To install application packages D. To configure SSH access

Question 2: Which environment is generally most appropriate for learning full Linux operating system installation and boot management?

A. WSL2 B. Browser-based terminal C. Full virtual machine D. Git Bash

Question 3: Which virtual networking mode is a convenient starting point for providing outbound internet connectivity to a VM?

A. NAT B. Host-only C. Disconnected D. Internal-only

Question 4: Why should you take VM snapshots before risky Linux experiments?

A. To increase available RAM B. To improve internet speed C. To help restore a previous VM state D. To increase the number of CPU cores

Question 5: What should you consider when using AWS EC2 for Linux labs?

A. Cloud billing and security B. Local monitor resolution only C. Keyboard layout only D. None of the above

# ✅ Knowledge Check Answers

| Question | Correct Answer                          |
| -------- | --------------------------------------- |
| 1        | B — To create and run virtual machines  |
| 2        | C — Full virtual machine                |
| 3        | A — NAT                                 |
| 4        | C — To help restore a previous VM state |
| 5        | A — Cloud billing and security          |

# 🧹 Cleanup

No cleanup is required for this lab.

You have only explored Linux environment options and inspected computer resources.

No software installation or infrastructure provisioning was required.

If you independently created temporary cloud resources while exploring the options, remove unused resources to avoid unnecessary charges.

# 🧠 Key Takeaways

- 🐧 Linux can run on physical machines, virtual machines, WSL2, and cloud instances.
- 🖥️ Virtual machines provide an excellent environment for comprehensive Linux administration training.
- 🪟 WSL2 is useful for learning Linux commands and development workflows on Windows.
- ☁️ AWS EC2 provides practical cloud and remote Linux administration experience.
- 🌐 Browser-based environments are useful for quick experiments.
- ⚙️ CPU, RAM, storage, and virtualization support are important selection criteria.
- 🔐 Security, backups, snapshots, and cloud cost awareness are essential lab practices.
- 🎯 Selecting the right environment helps create a reliable foundation for future Linux labs.

# 📚 Official Documentation

| Resource               | Official Documentation                                                                                                |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Ubuntu Server          | [Ubuntu Server Documentation](https://documentation.ubuntu.com/server/)                                               |
| Ubuntu Server Download | [Ubuntu Server Downloads](https://ubuntu.com/download/server)                                                         |
| Ubuntu Installation    | [Ubuntu Server Installation Guide](https://documentation.ubuntu.com/server/how-to/installation/)                      |
| Oracle VirtualBox      | [VirtualBox User Manual](https://www.virtualbox.org/manual/)                                                          |
| VMware                 | [Broadcom Technical Documentation](https://techdocs.broadcom.com/)                                                    |
| Microsoft WSL2         | [Install WSL](https://learn.microsoft.com/en-us/windows/wsl/install)                                                  |
| AWS EC2                | [Amazon EC2 Documentation](https://docs.aws.amazon.com/ec2/)                                                          |
| AWS Budgets            | [AWS Budgets Documentation](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) |
| Killercoda             | [Killercoda Official Website](https://killercoda.com/)                                                                |

# 🏁 Lab Completion

Congratulations! 🎉

You have completed:

Lab 0000 — Understand Linux Lab Environments and System Requirements

You now understand the available Linux lab environments, their hardware requirements, and how to select an appropriate platform.

Next Lab:

Lab 0001 — Install Ubuntu Server 26.04 LTS Using VirtualBox or VMware

In the next lab, you will:

- Download Ubuntu Server ISO.
- Install and configure virtualization software.
- Create an Ubuntu Server virtual machine.
- Allocate CPU, RAM, and disk resources.
- Configure virtual networking.
- Install Ubuntu Server.
- Create the initial Linux user.
- Verify that Ubuntu boots successfully.
- Prepare the VM for future Linux administration labs.

© Vyomanant Academy | Linux Administration and Production Troubleshooting | Lab 0000

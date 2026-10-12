
# 🐧 Linux Administration, Infrastructure & Production Troubleshooting

**Vyomanant Academy | Master Curriculum v7.1**

**Duration:** 30 Instructor-Led Hours  
**Schedule:** 15 Days × 2 Hours  
**Module 0:** Self-Paced Lab Setup  
**Primary OS:** Ubuntu Server 24.04 LTS  
**Level:** Intermediate, with an accelerated Linux refresher  
**Approach:** Break/Fix Labs, Real-World Scenarios and Root Cause Analysis

---

# 🎯 Course Overview

This course prepares Linux administrators and infrastructure engineers to investigate, troubleshoot and recover Linux-based infrastructure and application services.

Training focuses on practical host troubleshooting, enterprise storage fundamentals, networking diagnostics, resource performance, operational automation and incident recovery.

The course uses realistic, controlled failure scenarios inspired by infrastructure environments found in storage, networking and cloud technology companies.

## Intended Audience

- Linux System Administrators
- Infrastructure Support Engineers
- Site Reliability Engineers (SREs)
- DevOps and DevSecOps Engineers
- Cloud and Platform Engineers
- Storage and Networking Support Engineers
- Application Support Engineers
- Forward Deployed Engineers
- Engineers preparing for roles at F5, Pure Storage, NetApp, VAST Data, HPE and similar organizations

## Prerequisites

Learners should already understand:

- Basic Linux commands and filesystem navigation
- IP addressing, DNS and SSH fundamentals
- Basic operating-system concepts
- How to use a terminal

Foundational Linux concepts are refreshed, not taught from zero.

---

# 🏗️ Module 0 — Linux Lab Setup and Readiness

**Schedule:** Self-Paced | Outside 30 Hours

## Lessons

### Lesson 0.1 — Introduction to Linux Lab Environments
### Lesson 0.2 — Install Ubuntu Server 24.04 LTS Using a Local Hypervisor
### Lesson 0.3 — Configure Ubuntu on Windows WSL2
### Lesson 0.4 — Launch Ubuntu Server on AWS EC2
### Lesson 0.5 — Connect to AWS Ubuntu Using SSH and MobaXterm
### Lesson 0.6 — Access Browser-Based Linux Lab Environments
### Lesson 0.7 — Configure Additional Virtual Disks and Isolated Networking
### Lesson 0.8 — Configure SSH, sudo and vi Editor
### Lesson 0.9 — Prepare VM Snapshots and Recovery Procedures
### Lesson 0.10 — Install Diagnostic Utilities and Validate Readiness


### Recommended Environments

- WSL2 for lightweight Linux and Bash exercises
- Local VM for boot, storage, RAID and rescue
- AWS EC2 for remote Linux and application troubleshooting
- Multiple isolated VMs for NFS, iSCSI and network scenarios
- Pre-recorded diagnostic evidence when specialist hardware is unavailable

### Completion Criteria

Learners can access Linux systems, perform administrative actions, inspect attached storage, communicate between isolated VMs and restore a snapshot.

---

# 🐧 Module 1 — Linux Internals, Processes and systemd

**Schedule:** Day 1 | 2 Hours

## Lessons

### Lesson 1.1 — Linux Architecture, Kernel and User Space
### Lesson 1.2 — Linux Filesystem Hierarchy, /proc and /sys
### Lesson 1.3 — Processes, States, Signals and Resource Limits
### Lesson 1.4 — systemd Services, Dependencies and Targets
### Lesson 1.5 — journald, Service Logs and Failure Investigation

## Technical Coverage

`ps`, `top`, `pgrep`, `kill`, `lsof`, `ulimit`, `systemctl`, `journalctl`, `systemd-analyze`, `/proc`, `/sys`

---

# 🔧 Module 2 — Linux Boot, Recovery and Security Troubleshooting

**Schedule:** Day 2 | 2 Hours

## Lessons

### Lesson 2.1 — BIOS/UEFI, GRUB, Kernel and initramfs
### Lesson 2.2 — Boot Failures, Rescue Mode and Emergency Recovery
### Lesson 2.3 — Users, Permissions, ACLs and sudo Troubleshooting
### Lesson 2.4 — SSH Hardening and Access Recovery
### Lesson 2.5 — AppArmor and SELinux Troubleshooting Fundamentals

## Technical Coverage

`journalctl -b`, `systemctl`, `findmnt`, `lsblk`, `chmod`, `getfacl`, `ssh`, `sshd -t`, `visudo`, `aa-status`

SELinux troubleshooting is introduced using comparative examples; a separate RHEL-compatible lab is optional.

---

# 📊 Module 3 — Linux Performance and Resource Troubleshooting

**Schedule:** Day 3 | 2 Hours

## Lessons

### Lesson 3.1 — CPU Usage, Load Average and Scheduling
### Lesson 3.2 — Memory, Page Cache, Swap and OOM Events
### Lesson 3.3 — I/O Wait, Disk Latency and Blocked Processes
### Lesson 3.4 — Performance Investigation Using vmstat, iostat and strace
### Lesson 3.5 — Introduction to perf, PSI and Resource Limits

## Technical Coverage

`top`, `pidstat`, `free`, `vmstat`, `iostat`, `strace`, `perf`, `dmesg`, `journalctl -k`, `/proc/pressure`

---

# 💽 Module 4 — Linux Filesystems, LVM and RAID

**Schedule:** Day 4 | 2 Hours

## Lessons

### Lesson 4.1 — Linux Disks, Partitions, Mounts and fstab
### Lesson 4.2 — ext4, XFS and Filesystem Diagnostics
### Lesson 4.3 — Disk Space and Inode Exhaustion
### Lesson 4.4 — LVM Administration and Filesystem Expansion
### Lesson 4.5 — Linux Software RAID with mdadm

## Technical Coverage

`lsblk`, `blkid`, `df`, `du`, `findmnt`, `mount`, `pvs`, `vgs`, `lvs`, `lvextend`, `resize2fs`, `xfs_growfs`, `mdadm`

---

# 🗄️ Module 5 — Enterprise NFS and iSCSI Storage Troubleshooting

**Schedule:** Day 5 | 2 Hours

## Lessons

### Lesson 5.1 — NAS, SAN and Enterprise Storage Fundamentals
### Lesson 5.2 — NFS Architecture, Mounts, Exports and Permissions
### Lesson 5.3 — Hung NFS Mounts and Unavailable Storage Servers
### Lesson 5.4 — iSCSI Initiators, Targets, LUNs and Sessions
### Lesson 5.5 — Troubleshooting Network Storage Availability

## Technical Coverage

`exportfs`, `nfsstat`, `rpcinfo`, `mount`, `findmnt`, `ss`, `tcpdump`, `iscsiadm`, `dmesg`

---

# 🧱 Module 6 — NVMe, Multipath and Storage Performance

**Schedule:** Day 6 | 2 Hours

## Lessons

### Lesson 6.1 — NVMe Devices, Controllers and Namespaces
### Lesson 6.2 — NVMe over Fabrics Fundamentals
### Lesson 6.3 — Device Mapper Multipath and Path Redundancy
### Lesson 6.4 — Storage Latency, IOPS and Throughput
### Lesson 6.5 — Controlled Storage Benchmarking Using fio

## Technical Coverage

`nvme`, `lsblk`, `multipath`, `multipathd`, `udevadm`, `fio`, `iostat`, `dmesg`

---

# 🌐 Module 7 — Linux Networking and TCP Troubleshooting

**Schedule:** Day 7 | 2 Hours

## Lessons

### Lesson 7.1 — Linux Interfaces, IP Addresses and Routing
### Lesson 7.2 — DNS Resolution and Resolver Diagnostics
### Lesson 7.3 — TCP Connections, Sockets and Connection States
### Lesson 7.4 — Linux Firewalls with nftables and iptables Compatibility
### Lesson 7.5 — Packet Capture and Analysis Using tcpdump

## Technical Coverage

`ip`, `netplan`, `ss`, `dig`, `resolvectl`, `getent`, `nft`, `iptables`, `tcpdump`, `curl`

---

# 🔌 Module 8 — Advanced Networking, MTU, Load Balancing and TLS

**Schedule:** Day 8 | 2 Hours

## Lessons

### Lesson 8.1 — TCP Retransmissions, Resets and Connection Timeouts
### Lesson 8.2 — MTU, MSS and Path MTU Discovery
### Lesson 8.3 — Nginx and HAProxy Load Balancing Fundamentals
### Lesson 8.4 — HTTP 502/503, Backend Health Checks and TLS Failures
### Lesson 8.5 — Network sysctl Parameters and Safe Tuning

## Technical Coverage

`ss -ti`, `tcpdump`, `tracepath`, `ip`, `sysctl`, `curl`, `nginx -t`, `haproxy -c`, `openssl s_client`

---

# 🧩 Module 9 — Linux Isolation, GPU and RDMA Fundamentals

**Schedule:** Day 9 | 2 Hours

## Lessons

### Lesson 9.1 — Linux Namespaces and Process Isolation
### Lesson 9.2 — cgroups v2 and Resource Accounting
### Lesson 9.3 — CPU Throttling and Memory Limit Failures
### Lesson 9.4 — GPU Servers and NVIDIA Diagnostic Fundamentals
### Lesson 9.5 — RDMA, RoCE and InfiniBand Fundamentals

## Technical Coverage

`lsns`, `nsenter`, `unshare`, `systemd-cgls`, `systemd-cgtop`, `/sys/fs/cgroup`, `nvidia-smi`, `rdma`, `ibstat`

---

# 🤖 Module 10 — Bash Automation, Ansible and Prometheus

**Schedule:** Day 10 | 2 Hours

## Lessons

### Lesson 10.1 — Bash Scripting for Linux Health Checks
### Lesson 10.2 — Script Error Handling, Logging and Scheduling
### Lesson 10.3 — Ansible Inventory, SSH and Playbook Troubleshooting
### Lesson 10.4 — Prometheus and Node Exporter Fundamentals
### Lesson 10.5 — NTP, Time Synchronization and Monitoring Diagnostics

## Technical Coverage

Bash, `shellcheck`, `cron`, `systemctl list-timers`, `ansible`, `ansible-playbook`, Prometheus, Node Exporter, `timedatectl`, `chronyc`

---

# 🖥️ Module 11 — Linux Application Deployment and Troubleshooting

**Schedule:** Day 11 | 2 Hours

## Lessons

### Lesson 11.1 — Linux Application Deployment Architecture
### Lesson 11.2 — Install and Configure a Linux Web Application
### Lesson 11.3 — Nginx, Application Services and PostgreSQL Fundamentals
### Lesson 11.4 — File Permissions, Environment Variables and Dependencies
### Lesson 11.5 — Troubleshoot Application Startup and HTTP Failures

## Technical Coverage

`apt`, `systemctl`, `journalctl`, `ss`, `curl`, `nginx -t`, PostgreSQL service inspection, application logs

---

# 🚨 Module 12 — Production Incident Investigation and RCA

**Schedule:** Day 12 | 2 Hours

## Lessons

### Lesson 12.1 — Incident Severity and Initial Triage
### Lesson 12.2 — Structured Troubleshooting and Evidence Collection
### Lesson 12.3 — Correlating Linux Logs, Metrics and Infrastructure Changes
### Lesson 12.4 — Root Cause Validation and Safe Remediation
### Lesson 12.5 — Recovery Verification, RCA and Handover

## Technical Coverage

`journalctl`, `dmesg`, `ss`, `tcpdump`, `iostat`, `vmstat`, `strace`, change records, incident timelines

---

# 🏆 Module 13 — Real-World Project 1: Enterprise Storage Recovery

**Schedule:** Day 13 | 2 Hours

## Project

**Enterprise Storage Failure and PostgreSQL Application Recovery**

## Architecture

Client → Nginx → Application API → PostgreSQL → Dedicated Storage

The storage may use an LVM-backed virtual disk or isolated network storage.

## Lessons / Project Phases

### Phase 13.1 — Review Application and Storage Architecture
### Phase 13.2 — Validate Installed Application and Database Services
### Phase 13.3 — Investigate Injected Storage Failure
### Phase 13.4 — Restore Application and Database Functionality
### Phase 13.5 — Verify Recovery and Prepare RCA

## Fault Scenarios

- Disk space exhaustion
- Filesystem permission failure
- Inode exhaustion
- Unavailable NFS/iSCSI storage
- Storage latency

The instructor selects one principal incident, potentially with a related secondary fault, for the live assessment.

---

# 🌐 Module 14 — Real-World Project 2: Networking Recovery

**Schedule:** Day 14 | 2 Hours

## Project

**Production Load Balancer and Application Connectivity Recovery**

## Architecture

Client → Nginx/HAProxy → Backend Application A / Backend Application B

Host monitoring is available using Node Exporter and Prometheus.

## Lessons / Project Phases

### Phase 14.1 — Review Network and Application Architecture
### Phase 14.2 — Validate Backend and Load Balancer Services
### Phase 14.3 — Diagnose Injected Network or TLS Failure
### Phase 14.4 — Restore Application Connectivity
### Phase 14.5 — Validate Service and Prepare RCA

## Fault Scenarios

- Failed backend service
- DNS resolution failure
- Firewall blocking connectivity
- Incorrect routing or backend port
- TLS trust or certificate misconfiguration
- Controlled MTU mismatch

The instructor selects one principal incident, potentially with a related secondary fault, for the live assessment.

---

# 🧠 Module 15 — Final Independent Production Incident Challenge

**Schedule:** Day 15 | 2 Hours

## Assessment

**Unknown Linux Infrastructure and Application Failure**

The learner receives a disposable Linux environment with one or more injected problems.

No diagnostic hints or predefined commands are provided.

## Assessment Stages

### Stage 15.1 — Assess the Incident and Collect Initial Evidence
### Stage 15.2 — Form and Test Root-Cause Hypotheses
### Stage 15.3 — Investigate Service and Infrastructure Dependencies
### Stage 15.4 — Apply Safe Recovery Actions
### Stage 15.5 — Validate Recovery and Submit Incident RCA

## Potential Failure Categories

- Failed systemd service
- Incorrect permissions
- CPU or memory pressure
- OOM events
- Disk or inode exhaustion
- Failed filesystem mount
- NFS or storage access failure
- DNS or routing failure
- Firewall issue
- Backend application failure
- TLS or reverse proxy issue
- Multiple related infrastructure failures

---

# 📅 Final 15-Day Training Schedule

| Day | Module | Focus | Hours |
|---|---|---|---:|
| 1 | 1 | Linux Internals, Processes and systemd | 2 |
| 2 | 2 | Boot Recovery and Security | 2 |
| 3 | 3 | Linux Performance and Resource Diagnosis | 2 |
| 4 | 4 | Filesystems, LVM and RAID | 2 |
| 5 | 5 | NFS and iSCSI Troubleshooting | 2 |
| 6 | 6 | NVMe, Multipath and fio | 2 |
| 7 | 7 | Linux Networking, DNS, TCP and Firewalls | 2 |
| 8 | 8 | MTU, Load Balancing, TLS and sysctl | 2 |
| 9 | 9 | Namespaces, cgroups, GPU and RDMA | 2 |
| 10 | 10 | Bash, Ansible, Prometheus and NTP | 2 |
| 11 | 11 | Application Deployment and Debugging | 2 |
| 12 | 12 | Production Incident Investigation and RCA | 2 |
| 13 | 13 | Project 1 — Enterprise Storage Recovery | 2 |
| 14 | 14 | Project 2 — Networking Recovery | 2 |
| 15 | 15 | Independent Production Incident Challenge | 2 |
| | | **Total** | **30** |

---

# ⏱️ Instructor-Led Session Structure

## Standard Technical Days (1–12)

| Activity | Time |
|---|---:|
| Essential concepts | 15 minutes |
| Instructor demonstration | 20 minutes |
| Guided break/fix investigation | 45 minutes |
| Independent investigation | 30 minutes |
| Verification and RCA discussion | 10 minutes |
| **Total** | **120 minutes** |

## Project Days (13–14)

| Activity | Time |
|---|---:|
| Architecture and scenario briefing | 10 minutes |
| Verify prepared environment | 10 minutes |
| Fault investigation | 45 minutes |
| Recovery and validation | 40 minutes |
| RCA and handover | 15 minutes |
| **Total** | **120 minutes** |

## Final Assessment (Day 15)

| Activity | Time |
|---|---:|
| Incident briefing and safety rules | 5 minutes |
| Independent investigation | 65 minutes |
| Remediation and validation | 30 minutes |
| RCA and handover | 20 minutes |
| **Total** | **120 minutes** |

---

# 📚 Pre-Class and Self-Paced Requirements

The following must be completed outside the 30 instructor-led hours:

- Module 0 environment setup
- Basic Linux command refresher
- Essential networking prerequisites
- Installation of approved lab utilities
- Multi-VM preparation and snapshots
- Additional storage device configuration
- PostgreSQL and web application baseline deployment
- Load balancer and backend baseline preparation
- Optional advanced lab investigations

Recommended self-paced workload: approximately 10–15 hours, depending on prior experience.

This is an estimate, not a fixed completion guarantee.

---

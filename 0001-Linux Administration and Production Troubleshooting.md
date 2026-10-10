# Linux Administration and Production Troubleshooting

- **Vyomanant Academy | Linux-Only Master Curriculum**
- **Course Duration:** 30 instructor-led hours | 15 days × 2 hours per day  
- **Module 0:** Self-paced lab setup; not counted toward 30 hours

---

## Course Overview

This course builds practical Linux server administration, troubleshooting, security, performance and recovery skills for working professionals. It starts with a focused Linux refresher, progresses through essential administration and concludes with realistic, evidence-based production incident investigations.

The course teaches **Linux operating-system administration**, not complete DevOps, SRE, Platform Engineering or Forward Deployed Engineering job responsibilities.

### Who Should Attend?

- Linux System Administrators and Infrastructure Support Engineers
- DevOps, DevSecOps, Cloud and Platform Engineers who support Linux servers
- Site Reliability Engineers (SREs) investigating Linux host issues
- Application Support Engineers and Forward Deployed Engineers working with Linux environments

### Prerequisites

- Basic familiarity with operating systems and the command line
- Basic IP networking and DNS concepts
- Ability to use a terminal; Module 0 prepares the lab environment

### Learning Outcomes

After completing this course, learners should be able to:

1. Inspect a Linux server and collect system health information.
2. Configure and troubleshoot Linux users, permissions, sudo and SSH.
3. Manage systemd services, processes and scheduled jobs.
4. Troubleshoot disk, filesystem, mounts, LVM and common NFS problems.
5. Diagnose DNS, routing, sockets, firewall and TLS-related connectivity failures.
6. Investigate CPU, memory, swap, disk I/O and process resource limitations.
7. Apply Linux updates and security changes using safe rollback practices.
8. Analyze logs, correlate evidence and write a root cause analysis (RCA).
9. Build and validate basic Bash scripts for Linux administration.
10. Investigate boot failures and verify Linux service and backup recovery.
11. Resolve and document a simulated multi-layer Linux production incident.

---

# Complete Course Curriculum

## Module 0 — Course Orientation and Linux Lab Setup

**Schedule:** Self-paced, before Day 1 (outside 30 hours)

### Lessons

**Lesson 0.1 — Course Introduction and Learning Objectives**

**Lesson 0.2 — Course Schedule, Learning Path and Assessments**

**Lesson 0.3 — System Requirements and Linux Lab Setup**

**Lesson 0.4 — SSH Access, Virtual Machines and Lab Snapshots**

**Lesson 0.5 — Learning Materials, Assignments and Lab Guidelines**

**Lesson 0.6 — Linux Lab Readiness Check**

### Lab Readiness Check

Prove SSH, sudo, isolated lab networking, snapshot/restore and access to a second test VM or service.

---

## Module 1 — Linux Basics, Shell Commands and Server Health

**Schedule:** Day 1 | 2 hours

### Lessons

**Lesson 1.1 — Linux Architecture: Kernel, Shell and Distributions**

**Lesson 1.2 — Linux Filesystem Hierarchy, Files and Directories**

**Lesson 1.3 — Essential Linux Commands, Pipes and Text Processing**

**Lesson 1.4 — Check Linux System Information and Learn Basic Bash Commands**

**Lesson 1.5 — Hands-On Lab: Investigate an Unfamiliar Linux Server**

### Key Technical Coverage

`pwd`, `ls`, `stat`, `find`, `grep`, `sed`, `awk`, `uname`, `hostnamectl`, `uptime`, `free`, `ps`, `ls /proc`, `ls /sys`.

### Practical Outcome and Evidence

Server inventory, running services, filesystem layout, initial health metrics and sources used.

---

## Module 2 — Linux Users, Groups, Permissions and SSH

**Schedule:** Day 2 | 2 hours

### Lessons

**Lesson 2.1 — Manage Linux Users, Groups and Password Policies**

**Lesson 2.2 — File Permissions, Ownership, umask and ACLs**

**Lesson 2.3 — SSH Configuration, Key Authentication and sudo Access**

**Lesson 2.4 — Secure File Transfers using SCP, SFTP, Rsync and Tar**

**Lesson 2.5 — Hands-On Lab: Troubleshoot SSH and File Access Issues**

### Key Technical Coverage

`id`, `useradd`, `usermod`, `passwd`, `chmod`, `chown`, `getfacl`, `setfacl`, `sudo`, `visudo`, `ssh`, `sftp`, `scp`, `rsync`, `tar`.

### Practical Outcome and Evidence

Least-privilege access restored; SSH error identified; transfer validated. Verify `sshd` configuration before reload and retain a working recovery session.

---

## Module 3 — Linux Processes, systemd Services and Job Scheduling

**Schedule:** Day 3 | 2 hours

### Lessons

**Lesson 3.1 — Linux Processes, Signals and Process Management**

**Lesson 3.2 — Manage Linux Services using systemctl**

**Lesson 3.3 — Troubleshoot systemd Services and Logs using journalctl**

**Lesson 3.4 — Schedule Automated Jobs using cron and systemd Timers**

**Lesson 3.5 — Hands-On Lab: Fix a Linux Service That Fails After Reboot**

### Key Technical Coverage

`ps`, `top`, `pgrep`, `kill`, `nice`, `lsof`, `systemctl`, `journalctl`, `systemd-analyze`, `crontab`, `systemctl list-timers`.

**Knowledge Check:** Processes, systemd and job scheduling.  

### Practical Outcome and Evidence

Corrected unit/dependency, successful restart and reboot verification.

---

## Module 4 — Linux Storage, Filesystems, Mounts and LVM

**Schedule:** Day 4 | 2 hours

### Lessons

**Lesson 4.1 — Linux Disks, Partitions and Filesystems**

**Lesson 4.2 — Mounting, Unmounting and Persistent Mounts using /etc/fstab**

**Lesson 4.3 — Logical Volume Management (LVM) and Filesystem Expansion**

**Lesson 4.4 — Troubleshoot Disk Space, Inodes and NFS Mount Issues**

**Lesson 4.5 — Hands-On Lab: Recover an Application Affected by Storage Failure**

### Key Technical Coverage

`lsblk`, `blkid`, `df -h`, `df -i`, `du`, `findmnt`, `mount`, `umount`, `pvdisplay`, `vgdisplay`, `lvdisplay`, `lvextend`.

**Safety and Production Practice:** Distinguish ext4/XFS growth procedures; do not imply XFS can be shrunk; test persistent mount configuration before reboot.  

### Practical Outcome and Evidence

Cause and remedy, mount verification, successful application write and rollback note.

---

## Module 5 — Linux Networking, DNS, Routing and Firewalls

**Schedule:** Day 5 | 2 hours

### Lessons

**Lesson 5.1 — Linux IP Addresses, Interfaces and Routing**

**Lesson 5.2 — Troubleshoot DNS and Hostname Resolution**

**Lesson 5.3 — Inspect Network Ports, Sockets and Connections**

**Lesson 5.4 — Linux Firewall Configuration and Network Traffic Analysis**

**Lesson 5.5 — Hands-On Lab: Fix a Linux Application Connectivity Issue**

### Key Technical Coverage

`ip`, `nmcli`, `dig`, `resolvectl` where available, `getent hosts`, `ss`, `curl`, `firewall-cmd`, `nft`, `tcpdump`, `openssl s_client`.

### Practical Outcome and Evidence

Demonstrate whether the fault is resolver, route, listener, firewall or certificate/trust configuration; verify restored connectivity.

---

## Module 6 — Linux Performance Troubleshooting: CPU, Memory and Disk I/O

**Schedule:** Day 6 | 2 hours

### Lessons

**Lesson 6.1 — Linux System Performance Metrics and Load Average**

**Lesson 6.2 — Troubleshoot High CPU Usage and Process Bottlenecks**

**Lesson 6.3 — Investigate Memory, Swap and Out-of-Memory (OOM) Events**

**Lesson 6.4 — Analyze Disk I/O, Open Files and Resource Limits**

**Lesson 6.5 — Hands-On Lab: Troubleshoot a Slow Linux Application**

### Key Technical Coverage

`top`, `ps`, `pidstat`, `free`, `vmstat`, `iostat`, `lsof`, `ulimit`, `sysctl`, `dmesg`, `journalctl -k`; interpret PSI/cgroup files where supported.

**Safety and Production Practice:** Diagnose first; modify kernel settings only in disposable labs with rollback.  

### Practical Outcome and Evidence

Identify actual bottleneck and demonstrate before/after measurements.

---

## Module 7 — Linux Package Management, Patching and Updates

**Schedule:** Day 7 | 2 hours

### Lessons

**Lesson 7.1 — Manage Linux Packages and Repositories using DNF and APT**

**Lesson 7.2 — RPM, DEB Packages, Versions and Dependencies**

**Lesson 7.3 — Linux Security Updates, Kernel Patching and Maintenance Planning**

**Lesson 7.4 — Configuration Backups, Change Validation and Rollback Planning**

**Lesson 7.5 — Hands-On Lab: Recover a Linux Service After a Failed Update**

### Key Technical Coverage

`dnf`, `rpm`, `apt`, `dpkg`, version comparison, package history where available, configuration diff and backup verification.

**Knowledge Check:** Packages, patching and safe changes.  

### Practical Outcome and Evidence

Package/configuration change identified, service restored and recovery plan recorded.

---

## Module 8 — Linux Security, SSH Hardening, sudo and SELinux

**Schedule:** Day 8 | 2 hours

### Lessons

**Lesson 8.1 — Linux Access Controls and Least-Privilege Security**

**Lesson 8.2 — SSH Hardening, sudo Policies and Secure Administration**

**Lesson 8.3 — SELinux Contexts, Policies and Access Denial Troubleshooting**

**Lesson 8.4 — Firewall Security, Linux Audit Logs and AppArmor Basics**

**Lesson 8.5 — Hands-On Lab: Restore an Application Blocked by Security Policies**

### Key Technical Coverage

`sshd -t`, `visudo -c`, `getenforce`, `sestatus`, `ls -Z`, `restorecon`, audit log inspection; AppArmor coverage only on applicable distributions.

**Safety and Production Practice:** Do not disable SELinux, AppArmor or firewalls as the default solution.  

### Practical Outcome and Evidence

Policy cause isolated, permitted remediation applied, security control left enabled.

---

## Module 9 — Linux Logs, Monitoring and Finding the Root Cause

**Schedule:** Day 9 | 2 hours

### Lessons

**Lesson 9.1 — Linux System Logs and journalctl Troubleshooting**

**Lesson 9.2 — Log Rotation, Journal Management and Disk Usage**

**Lesson 9.3 — Linux Time Synchronization and Event Correlation**

**Lesson 9.4 — Root Cause Analysis (RCA) using Logs, Metrics and Change History**

**Lesson 9.5 — Hands-On Lab: Investigate an Intermittent Linux Application Failure**

### Key Technical Coverage

`journalctl`, `logger`, `logrotate`, `timedatectl`, `chronyc` where installed, basic host-metric collection and event timelines.

**Course Scope Note:** Host/service monitoring only; advanced SRE SLI/SLO/error-budget engineering is excluded.

**Knowledge Check:** Logs, monitoring and RCA.  

### Practical Outcome and Evidence

Timestamped evidence, probable root cause, alternatives considered and verification steps.

---

## Module 10 — Linux Web Servers and Application Troubleshooting

**Schedule:** Day 10 | 2 hours

### Lessons

**Lesson 10.1 — Nginx, Apache, Reverse Proxies and Backend Architecture**

**Lesson 10.2 — Manage Web Servers, Application Services and Environment Configuration**

**Lesson 10.3 — Troubleshoot HTTP 502, 503 and Application Connectivity Errors**

**Lesson 10.4 — Diagnose TLS Certificates, File Permissions and Application Logs**

**Lesson 10.5 — Hands-On Lab: Restore a Failed Linux Web Application**

### Key Technical Coverage

`systemctl`, `journalctl`, `ss`, `curl`, `openssl`, web-server configuration validation, file ownership and host trust checks.

**Course Scope Note:** No customer-specific integration, CI/CD or deployment platform instruction.

### Practical Outcome and Evidence

End-to-end request restored; fault located at web server, backend service, filesystem, TLS or networking layer.

---

## Module 11 — Bash Scripting and Linux Automation

**Schedule:** Day 11 | 2 hours

### Lessons

**Lesson 11.1 — Bash Shell, Variables, Exit Codes and Safe Script Execution**

**Lesson 11.2 — Bash Conditions, Loops, Functions and Script Arguments**

**Lesson 11.3 — Input Validation, Error Handling and Log Processing**

**Lesson 11.4 — Automate Linux Health Checks using Bash and Job Scheduling**

**Lesson 11.5 — Hands-On Lab: Build and Troubleshoot a Linux Health-Check Script**

### Key Technical Coverage

Bash, `shellcheck` if available, `set -o pipefail`, traps, logging, cron, timers and nonzero exit codes.

**Course Scope Note:** No Ansible, Terraform or CI/CD pipelines.

**Knowledge Check:** Bash and Linux automation.  

### Practical Outcome and Evidence

Script, sample output, failure case, validation procedure and job schedule.

---

## Module 12 — Linux Boot, Rescue and Server Recovery

**Schedule:** Day 12 | 2 hours

### Lessons

**Lesson 12.1 — Linux Boot Process: BIOS/UEFI, GRUB, Kernel and initramfs**

**Lesson 12.2 — Diagnose Linux Boot Failures and systemd Targets**

**Lesson 12.3 — Linux Rescue Mode and Emergency Recovery**

**Lesson 12.4 — Recover Failed Mounts, Restore Backups and Use VM Snapshots**

**Lesson 12.5 — Hands-On Lab: Repair a Linux Server That Fails to Boot**

### Key Technical Coverage

systemd boot targets, `journalctl -b`, relevant bootloader/recovery tooling for the pinned distribution, backup restore verification.

### Practical Outcome and Evidence

Root cause, repair record, successful reboot, service checks and restore verification. Introduce RPO/RTO only as recovery-planning vocabulary.

---

## Module 13 — Linux Server Operations and Incident Management

**Schedule:** Day 13 | 2 hours

### Lessons

**Lesson 13.1 — Linux Health Monitoring, Alert Triage and Incident Prioritization**

**Lesson 13.2 — Backup Verification, Restore Testing and Recovery Readiness**

**Lesson 13.3 — Production Change Management, Rollback and Service Restoration**

**Lesson 13.4 — Incident Communication, Runbooks, RCA and Handover Documentation**

**Lesson 13.5 — Hands-On Lab: Manage a Linux Production Incident from Alert to Closure**

### Key Technical Coverage

Host-side alert triage, approved break-glass/console recovery pathways, runbooks, change logs, evidence-based closure.

**Course Scope Note:** No AWS services, SRE reliability-program management or customer-specific integration.

**Knowledge Check:** Linux operations and incident handling.  

### Practical Outcome and Evidence

Alert assessment, safe action sequence, service verification and concise incident handover.

---

## Module 14 — Advanced Linux Troubleshooting

**Schedule:** Day 14 | 2 hours

### Lessons

**Lesson 14.1 — Structured Linux Troubleshooting Methodology**

**Lesson 14.2 — Trace Linux Service, Network, Storage and Security Dependencies**

**Lesson 14.3 — Advanced Diagnostics using Logs, tcpdump, lsof and strace**

**Lesson 14.4 — Root Cause Validation, Permanent Fixes and Recovery Verification**

**Lesson 14.5 — Independent Lab: Troubleshoot an Unknown Linux Production Issue**

**Independent Assignment:** Submit a Linux troubleshooting report with symptom, timeline, command outputs, hypotheses, root cause, fix, rollback and evidence of recovery.

### Practical Outcome and Evidence

Independent investigation; no prescribed command list; safe recovery and defensible RCA.

---

## Module 15 — Final Capstone: Linux Production Incident Recovery

**Schedule:** Day 15 | 2 hours

### Lessons

**Lesson 15.1 — Production Incident Scenario, Requirements and Safety Rules**

**Lesson 15.2 — Investigate Linux Services, Logs, Storage and Network Connectivity**

**Lesson 15.3 — Apply Safe Remediation and Validate Application Recovery**

**Lesson 15.4 — Prepare Root Cause Analysis, Rollback Notes and Operations Handover**

**Lesson 15.5 — Final Practical Assessment: Demonstrate Linux Incident Recovery**

### Capstone Scenario

A disposable Linux-hosted web or application service is unavailable following a routine host configuration or package change. The learner identifies one or more Linux-level causes (for example systemd configuration, file permissions, resolver/firewall, mount, disk pressure or TLS trust), restores the application and proves successful recovery.

### Required Capstone Deliverables

Incident timeline, diagnostic outputs, hypotheses, root cause, change record, rollback plan, service validation, prevention recommendations and handover note.

---

## Course Scope and Boundaries

### Included in This Course

Linux OS and command line; accounts and access; processes and systemd; storage; host networking; package management; patching; SSH, sudo, SELinux/AppArmor; Linux auditing; logging; host monitoring; CPU/memory/I/O diagnostics; Bash automation; boot recovery; Linux-hosted web and service troubleshooting; Linux incident response.

### Outside This Course

- **Docker / Kubernetes:** no images, containers, orchestration, Kubernetes nodes or workloads administration.
- **Terraform / infrastructure as code:** no infrastructure provisioning modules.
- **CI/CD:** no pipeline design, runners or release engineering workflows.
- **Advanced SRE:** no SLO design, error budgets, distributed tracing or reliability-program management; only host health and incident fundamentals.
- **Customer integration:** no customer-specific APIs, integrations or deployment architecture; only generic Linux service and environment diagnostics.
- **Ansible / configuration management platform training:** excluded; Bash and native Linux scheduling remain in scope.
- **Cloud-platform administration:** no AWS architecture, IAM, EC2 administration or cloud service troubleshooting. The Linux guest OS may be hosted in a VM or cloud instance without making cloud tooling part of the syllabus.

Linux-native cgroups, `/proc`, `/sys`, resource controls and `sysctl` are included as **OS concepts and diagnostics**, without teaching container platforms.


## Tutor LMS Implementation Structure

- Create **16 Topics**: Module 0 through Module 15.
- Create **81 Lessons**: 6 self-paced orientation lessons and 5 segments for each of 15 live modules.
- Five lesson segments form **one** 2-hour class; they are not separate 2-hour sessions.
- Add five formative quizzes (Modules 3, 7, 9, 11, 13), one independent incident report (Module 14) and one final capstone assessment (Module 15).
- Configure quizzes/assignments in accordance with the capabilities and licensing of the actual Tutor LMS installation. This Markdown file is a **planning source**, not a verified LMS import format.


## Training Delivery Plan

### Daily 2-Hour Session Structure

| Activity | Minutes |
|---|---:|
| Essential terminology and concepts | 15 |
| Instructor demonstration | 20 |
| Guided Linux break/fix lab | 45 |
| Independent investigation | 30 |
| Verification, RCA and feedback | 10 |
| **Total** | **120** |

For Days 14–15, combine guided and independent lab blocks for longer investigations. The five LMS lessons are organizational learning segments, not equal-length 24-minute lectures. Quizzes and report preparation can include self-paced work outside live delivery.

## Practical Lab Requirements and Safety

- **Baseline:** one primary VM per learner plus a second test VM or isolated Linux-hosted application for SSH/network scenarios.
- **Supported release:** choose and freeze a currently supported RHEL-compatible release and use Ubuntu comparisons only where needed.
- **Resets:** instructor-created faults, snapshots, known-good images and a tested recovery path.
- **Data and access:** disposable test accounts, non-production credentials, no exposed training services on public networks.
- **Safe changes:** snapshot first; validate sshd, sudoers, systemd and fstab changes before reboot/reload; avoid reckless deletion or firewall changes.
- **Distribution differences:** document differences in DNF/APT, firewalld availability, SELinux/AppArmor, resolver configuration, boot tooling and filesystem behavior.
- **Tool availability:** preinstall or approve `sysstat`, `lsof`, `tcpdump`, `strace`, `dig` and relevant audit utilities as appropriate.
- **After lab:** restore snapshots, remove test access and verify clean state.

## Assessments and Evaluation

| Evaluation | Weight |
|---|---:|
| Daily lab evidence and verification | 30% |
| Independent troubleshooting investigations | 25% |
| Bash administration automation assignment | 15% |
| Final Linux incident recovery capstone | 30% |
| **Total** | **100%** |

**Suggested passing standard:** 70% overall, successful final service recovery and no critical unsafe actions. Formative quizzes can be tracked separately or incorporated into daily learning evidence; avoid double-counting grades.

**Assessment rubric dimensions:** diagnostic method, evidence quality, safety/least privilege, correctness of fix, post-fix validation, RCA clarity and handover quality.

## Course Approval and Release Checklist

- [ ] Academic team signs off on the Linux-only scope and all 16 topics.
- [ ] Instructor validates the curriculum against the chosen Linux release.
- [ ] Every lab is tested from a clean VM and can be reliably reset.
- [ ] Check that 30 instructor-led hours are feasible without claiming advanced mastery of every listed tool.
- [ ] Tutor LMS lesson, quiz and assignment availability is confirmed.
- [ ] Grading, pass criteria and capstone evidence templates are finalized.
- [ ] Lab access, security isolation, snapshots and cleanup are documented.
- [ ] Learner-facing copy accurately describes Linux-only outcomes.

## Recommended Official Technical References

- [Red Hat Enterprise Linux documentation](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/)
- [Rocky Linux documentation](https://docs.rockylinux.org/)
- [Ubuntu Server documentation](https://documentation.ubuntu.com/server/)
- [systemd manuals](https://www.freedesktop.org/software/systemd/man/latest/)
- [GNU Bash reference manual](https://www.gnu.org/software/bash/manual/)
- [Linux kernel documentation](https://docs.kernel.org/)

**Scope statement for website:** *A practical, Linux-only course covering server administration, secure operations, Bash automation, performance diagnostics, Linux service troubleshooting and recovery. Docker, Kubernetes, Terraform, CI/CD, advanced SRE and customer integration are offered separately.*

---

**Vyomanant Academy — Linux Administration and Production Troubleshooting | Version 6.2**  
**Curriculum classification:** Linux-only master syllabus  
**Release status:** Ready for academic review and lab validation prior to publication

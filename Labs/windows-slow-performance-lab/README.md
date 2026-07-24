# Diagnose and Resolve Slow Performance Issues (CompTIA A+ 1202)

Hands-on Windows 11 lab diagnosing and resolving a slow-performing system using Task Manager, Resource Monitor, and Disk Cleanup.

## Objective

Systematically identify what's consuming CPU, memory, disk, and network resources on a Windows endpoint, then apply targeted fixes — ending unnecessary processes, disabling non-essential startup programs, and reclaiming disk space.

## Tools

Task Manager, Resource Monitor, Disk Cleanup

## Process

**1. Baseline resource usage.** Opened Task Manager's Performance tab and reviewed CPU, memory, disk, and network utilization to establish a baseline before making changes.

| CPU | Memory |
|---|---|
| <img width="975" height="796" alt="image" src="https://github.com/user-attachments/assets/aa0b8236-e699-46fb-9e0c-1759a86e8ce6" />
 | <img width="975" height="791" alt="image" src="https://github.com/user-attachments/assets/ddce42c5-41e8-4444-ad0f-a5dffe3c019d" />
 |

| Disk | Network |
|---|---|
| <img width="975" height="793" alt="image" src="https://github.com/user-attachments/assets/055b7c0f-63ac-4055-aa9b-e0cfc44296f4" />
 | <img width="975" height="757" alt="image" src="https://github.com/user-attachments/assets/86dcf8ff-2e6a-459b-843d-2abf29055c1e" />
 |

**2. Identify resource-heavy processes.** Switched to the Processes tab and sorted by CPU and Memory to surface the biggest consumers — Antimalware Service Executable (185.5 MB) and a background Resume process group (104.9 MB) stood out.

<img width="975" height="1158" alt="image" src="https://github.com/user-attachments/assets/18d908e0-d60a-4f1c-8b88-d5c515783c15" />


Right-clicked the problematic process group and ended the task where safe to do so.

<img width="975" height="574" alt="image" src="https://github.com/user-attachments/assets/863a81d7-574a-4459-b52d-b2195e2a5efe" />


**3. Trim startup load.** Opened Task Manager's Startup apps view and disabled non-essential programs (Microsoft 365 Copilot) so they stop competing for resources at boot.

<img width="975" height="896" alt="image" src="https://github.com/user-attachments/assets/a1ffa3cf-414a-47e5-9eb2-6478777aad62" />

<img width="975" height="573" alt="image" src="https://github.com/user-attachments/assets/3c244335-885c-4a6b-9c0d-d7f9b73592ad" />


**4. Check disk activity.** Opened Resource Monitor's Disk tab to check for processes generating high read/write activity and confirm disk I/O wasn't the bottleneck.

<img width="975" height="878" alt="image" src="https://github.com/user-attachments/assets/f566233e-3dac-4baa-935a-cee29c19e1b4" />


**5. Reclaim disk space.** Ran Disk Cleanup on the C: drive and selected reclaimable file categories (temporary internet files, downloaded program files) to free up space.

<img width="673" height="758" alt="image" src="https://github.com/user-attachments/assets/0f9202a6-59fd-459f-b763-490306ca2177" />


## Outcome

Walked a slow endpoint through a full performance triage: baseline the four core resources, isolate the specific processes and startup programs driving the load, confirm disk I/O wasn't a contributing factor, and reclaim disk space — a repeatable sequence for any "my computer is slow" ticket.

## Skills Demonstrated

Windows performance monitoring, resource bottleneck analysis, process management, startup optimization, disk space management, systematic troubleshooting methodology.


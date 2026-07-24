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
| ![Task Manager CPU](images/01-task-manager-cpu.png) | ![Task Manager Memory](images/02-task-manager-memory.png) |

| Disk | Network |
|---|---|
| ![Task Manager Disk](images/03-task-manager-disk.png) | ![Task Manager Network](images/04-task-manager-network.png) |

**2. Identify resource-heavy processes.** Switched to the Processes tab and sorted by CPU and Memory to surface the biggest consumers — Antimalware Service Executable (185.5 MB) and a background Resume process group (104.9 MB) stood out.

![Processes sorted by memory](images/05-processes-sorted-by-memory.png)

Right-clicked the problematic process group and ended the task where safe to do so.

![Ending a resource-heavy process](images/06-end-task-resource-heavy-process.png)

**3. Trim startup load.** Opened Task Manager's Startup apps view and disabled non-essential programs (Microsoft 365 Copilot) so they stop competing for resources at boot.

![Disabling a startup app](images/07-startup-apps-disable.png)
![Startup app confirmed disabled](images/08-startup-app-disabled-confirmed.png)

**4. Check disk activity.** Opened Resource Monitor's Disk tab to check for processes generating high read/write activity and confirm disk I/O wasn't the bottleneck.

![Resource Monitor Disk tab](images/09-resource-monitor-disk-tab.png)

**5. Reclaim disk space.** Ran Disk Cleanup on the C: drive and selected reclaimable file categories (temporary internet files, downloaded program files) to free up space.

![Disk Cleanup](images/10-disk-cleanup.png)

## Outcome

Walked a slow endpoint through a full performance triage: baseline the four core resources, isolate the specific processes and startup programs driving the load, confirm disk I/O wasn't a contributing factor, and reclaim disk space — a repeatable sequence for any "my computer is slow" ticket.

## Skills Demonstrated

Windows performance monitoring, resource bottleneck analysis, process management, startup optimization, disk space management, systematic troubleshooting methodology.


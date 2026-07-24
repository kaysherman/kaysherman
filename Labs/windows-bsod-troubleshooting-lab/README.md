# Troubleshoot Blue Screen of Death Errors (CompTIA A+ 1202)

Hands-on Windows 11 lab diagnosing Blue Screen of Death (BSOD) crashes using Event Viewer and Reliability Monitor.

## Objective

Systematically trace a system crash back to its root cause using Windows' built-in diagnostic tools, rather than guessing at hardware or driver issues.

## Tools

Event Viewer, Reliability Monitor

## Process

**1. Filter the System log for crash events.** Opened Event Viewer, navigated to Windows Logs > System, and filtered the current log to Critical and Error level events from the `BugCheck` and `Kernel-Power` sources — the two event sources most associated with unexpected shutdowns and crash dumps.

<img width="975" height="753" alt="image" src="https://github.com/user-attachments/assets/c0081fb4-f5f8-4813-9cb8-6c036ae2798b" />


**2. Cross-check the Application log.** Reviewed Windows Logs > Application for related application-level errors that might have contributed to or coincided with the crash, rather than treating the System log in isolation.

<img width="975" height="734" alt="image" src="https://github.com/user-attachments/assets/9e990fe2-9b20-4dd1-bde3-c6bd5c614ad4" />


**3. Review system stability history.** Opened Reliability Monitor (`perfmon /rel`) to view the stability index over time and correlate any dips against application failures, Windows failures, or recent updates — giving a timeline view that Event Viewer alone doesn't provide.

<img width="975" height="539" alt="image" src="https://github.com/user-attachments/assets/c294ac2c-6a7f-4074-ba39-4cb1d539c57b" />


## Outcome

Built a two-tool workflow for BSOD triage: Event Viewer to pinpoint the specific crash event and its source, Reliability Monitor to see whether it's an isolated incident or part of a stability trend — the information needed to distinguish a one-off driver hiccup from a recurring hardware problem.

## Skills Demonstrated

Event Viewer log analysis, Reliability Monitor, BSOD root-cause investigation, Windows diagnostic tooling, systematic troubleshooting methodology.


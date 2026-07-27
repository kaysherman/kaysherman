# ServiceNow Ticketing Lab — Top 5 Service Desk Scenarios

Hands-on incident ticketing practice in a ServiceNow Personal Developer Instance, covering four of the most common service desk ticket types end-to-end: intake, triage, troubleshooting, and resolution (or escalation).

## Objective

Practice real ITSM ticket workflows rather than just documentation theory — creating, categorizing, triaging by impact/urgency, working, and closing incidents the way a Tier 1 service desk analyst would in ServiceNow, including knowing when to escalate rather than force a resolution.

## Tools

ServiceNow (Incident Management module)

## Tickets Worked

### 1. Password Reset / Account Lockout

The most common service desk ticket industry-wide. Logged the caller's report, set Impact/Urgency to 3 - Low (single user, non-critical), and assigned to Help Desk.

<img width="975" height="456" alt="image" src="https://github.com/user-attachments/assets/16dc4397-6d6e-44ea-83b3-ea8459b5058b" />


Documented the fix directly in Work notes — verified identity, confirmed the account was locked in Active Directory, unlocked it, and forced a password reset at next logon — then resolved with a clear resolution note.

<img width="975" height="407" alt="image" src="https://github.com/user-attachments/assets/750794af-2feb-4e34-b321-f37675a9c084" />


### 2. Software Installation Request

A request-type ticket rather than a break/fix incident — useful for showing that not every ticket is an outage. Followed a manager-approval workflow before installing anything.

<img width="975" height="418" alt="image" src="https://github.com/user-attachments/assets/e61d63e3-2b1b-45f6-bcf5-ba1d9f09c6b1" />


Work notes trace the full approval chain: confirmed manager approval, verified license availability against the volume licensing agreement, remotely installed Microsoft Visio, and verified functionality before resolving.

<img width="975" height="527" alt="image" src="https://github.com/user-attachments/assets/9146cff6-b670-40a3-9252-f09f84c84b6f" />


### 3. Outlook / Email Not Working

Multiple possible causes (profile corruption, Exchange connectivity, mailbox quota, offline mode, network) meant this ticket needed systematic elimination rather than a single fix. Set Impact/Urgency to 2 - Medium, since email being down is more disruptive than a single-feature issue.

<img width="975" height="481" alt="image" src="https://github.com/user-attachments/assets/a07aa55b-d39b-44aa-ab87-3394c7c9f5e8" />


Tested Outlook Web Access first to isolate the problem to the client vs. the server — OWA worked, which immediately ruled out Exchange connectivity and mailbox quota as causes and pointed to a local Outlook profile issue. Recreated the profile, which resolved it.

<img width="975" height="498" alt="image" src="https://github.com/user-attachments/assets/2b4c573f-a1d8-4230-bf7a-40cc7f2da828" />


### 4. VPN / Remote Access Issue

Escalation, not self-resolution. Set Impact to 2 - Medium and Urgency to 1 - High, since a remote employee with no VPN access is fully blocked from working — higher priority than the other three tickets.

<img width="975" height="492" alt="image" src="https://github.com/user-attachments/assets/5824036b-c99f-4718-ad5b-1030cb55a37b" />


Ran through the full standard troubleshooting sequence — connectivity, credentials, MFA, client version, service restart — and ruled out every one of them. Rather than continuing to guess, escalated to the Network Operations team with a clear note on what had already been tried and why the remaining cause (VPN gateway) was outside Service Desk scope.

<img width="975" height="488" alt="image" src="https://github.com/user-attachments/assets/d8184a46-f5bb-48e8-a75c-248f7c1461fa" />


## Outcome

Four tickets, four different resolution paths: a routine fix, an approval-driven request, root-cause elimination across multiple possible causes, and an appropriately escalated issue rather than a forced resolution. Priority judgment scaled correctly across all four (Low → Low → Medium → High) based on actual business impact, not a flat default.

## Skills Demonstrated

ServiceNow Incident Management, ticket triage (Impact/Urgency/Priority), systematic troubleshooting and root-cause elimination, software license and approval workflows, VPN/MFA troubleshooting, escalation judgment, service desk documentation discipline.


# Active Directory Basics — Identity & Access Lab

Hands-on domain administration lab (TryHackMe) covering AD structure, user/group management, and Group Policy enforcement in a simulated Windows domain.

## Objective

Understand how Active Directory manages identities, authentication, and access across an enterprise network, using a lab environment with a domain controller, file server, database server, workstation, and desktop endpoint.

## Tools

Active Directory Users and Computers (ADUC), PowerShell, Group Policy Management

## Process

**1. Domain exploration.** Navigated ADUC, reviewed domain structure, organizational units (OUs), users, and groups, and examined group membership and privilege levels.

<img width="975" height="696" alt="image" src="https://github.com/user-attachments/assets/1d52d52f-d320-4fb1-b554-4689cd67fa0e" />


**2. User and group administration.** Reset a domain user's password and forced a password change at next logon via PowerShell:

```powershell
Set-ADUser -ChangePasswordAtLogon $true -Identity sophie -Verbose
```

<img width="975" height="319" alt="image" src="https://github.com/user-attachments/assets/3c10b42c-f810-4779-b6c2-5e37be2682e6" />


**3. Authentication validation.** Logged into the user's workstation with the domain-format credentials (`THM\sophie`) and confirmed successful authentication, correct profile creation, and proper permission application by retrieving the assigned flag file.

<img width="975" height="419" alt="image" src="https://github.com/user-attachments/assets/c0230bd5-6db4-4894-8bbe-ebe939e75e1a" />

**4. Group Policy configuration.** Created a new GPO to restrict Control Panel access and system setting changes for standard users, then linked it to the Management, Marketing, and Sales OUs. Verified the GPO appeared under each linked OU, confirmed correct inheritance order, and checked for conflicting policies.

<img width="742" height="794" alt="image" src="https://github.com/user-attachments/assets/a4baaa9b-9575-4404-92a1-9ee154d5c90a" />


## Outcome

Completed a full identity lifecycle loop — create/modify a credential, validate it end-to-end via login, then enforce policy-based restrictions across three separate OUs with no inheritance conflicts.

## Skills Demonstrated

Kerberos vs. NTLM authentication, Group Policy Objects (GPOs), identity lifecycle management, least-privilege access, domain resource access control, PowerShell for AD administration.


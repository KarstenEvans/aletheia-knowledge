---
aletheia_schema: knowledge-v0.2
title: Aletheia Secret Windows
domain: computing
collection: secret-windows
status: curated
language: en-GB
version: 0.8
created: 2026-09-23
last_reviewed: 2026-09-23
resource_url: https://karstenevans.github.io/aletheia-knowledge/resources/aletheia-secret-windows-rsc.htm
resource_status: live
resource_mirror_planned: https://swindon.org.uk/resources/aletheia-secret-windows-rsc.htm
---

# Aletheia Secret Windows Knowledge Library

Purpose: a practical, source-traced Windows knowledge library covering overlooked shortcuts, safe command-line tools, PowerShell, troubleshooting, networking, recovery, privacy, performance, Windows Server administration and version-specific traps.

"Secret Windows" means useful things that are easy to miss. It does not mean bypassing licensing, defeating security controls, hiding malicious activity, or applying mysterious registry scripts found in the darker cupboards of the internet.

## Portable knowledge design

Aletheia Knowledge is vendor-neutral Markdown first.

Core rules:
- Markdown is the canonical knowledge format.
- Each card states which Windows versions it applies to.
- Discovery books and cheat sheets are topic maps, not verification.
- Prefer Microsoft primary documentation for Windows behaviour and lifecycle facts.
- Commands that can remove data, stop services, alter policy or change boot/storage state carry an explicit risk label.
- A safe GUI method is preferred where it is clearer than a command.
- Do not recommend a "debloat" action merely because Windows allows it.
- Preserve reversibility: uninstall or disable before deleting; export settings before registry edits; make a backup before recovery work.
- Do not publish one-line "debloat everything" scripts as trusted knowledge.
- Cloud services, AI search and browser integrations are optional abilities, not foundation bricks.

## Resource backlink rule

Planned resource page:

https://swindon.org.uk/resources/aletheia-secret-windows-rsc.htm

Until RESOURCE_STATUS becomes LIVE, apps should not render this as a public "More / resources" link.

When live, the resource page may contain books, utilities and clearly disclosed affiliate links. Commercial links must never influence evidence status, risk labels or wording in this knowledge file.

## Knowledge rule

DISCOVERY SOURCE -> TOPIC -> CURRENT VERSION CHECK -> PRIMARY DOCUMENTATION -> SAFETY CHECK -> KNOWLEDGE CARD

## Card fields

STATUS:
- VERIFIED
- VERIFIED_WITH_CONTEXT
- LEGACY
- REMOVED
- PROVISIONAL
- REJECTED
- METHOD

EVIDENCE:
- STRONG: primary Microsoft/Google/Cloudflare documentation or lifecycle page.
- GOOD: established behaviour supported by current documentation.
- CONTEXT: useful interpretation or operating practice built around verified facts.
- CHECK: needs a version-specific recheck before automation.

RISK:
- LOW: read-only or easily reversible.
- MEDIUM: changes configuration or installed software.
- HIGH: can interrupt services, networking, recovery, boot or access.
- DESTRUCTIVE: can delete data or make recovery difficult.

LIFECYCLE:
- CURRENT
- SUPPORTED-LEGACY
- UNSUPPORTED
- REMOVED
- MIXED

## Discovery-source registry

The following copyrighted items supplied for this research are used only as topic discovery/provenance. Their prose is not copied and their claims are not accepted without independent checking.

1. Windows Command
   https://www.scribd.com/document/390140294/Windows-Command
2. Command
   https://www.scribd.com/document/704616117/Command
3. Cmd
   https://www.scribd.com/document/969764088/Cmd
4. A-to-Z List of Windows CMD Commands
   https://www.scribd.com/document/856922711/A-to-Z-List-of-Windows-CMD-Commands
5. Windows CMD Command Syntax / SS64-style compilation
   https://www.scribd.com/document/441026377/Windows-CMD-Command-Syntax-SS64-Com-1
6. Windows CMD Commands
   https://www.scribd.com/document/871803772/Windows-CMD-Commands
7. Windows System Administrator Interview Questions
   https://www.scribd.com/doc/176163468/Windows-System-Administrator-Interview-Q
8. PowerShell / Linux Command Cheat Sheet
   https://www.scribd.com/document/878894813/PowerShell-Linux-Command-CheatSheet
9. Windows Server Administration
   https://www.scribd.com/document/897021152/Windows-Server-Administration
10. MCSE Notes
    https://www.scribd.com/document/226091615/MCSE-Notes-Djvu
11. Windows / computing "Dummies" source
    https://www.scribd.com/document/455251608/dummies
12. Help Your Kids With Computer Coding, 2nd Edition, DK
    https://www.scribd.com/document/426426943/Help-Your-Kids-With-Computer-Coding-2nd-Edition-DK
13. The Complete Windows 11 Manual, 2nd Edition, 2022
    https://www.scribd.com/document/658632770/The-Complete-Windows-11-Manual-2nd-Edition-2022
14. Windows 11 Cheat Sheet
    https://www.scribd.com/document/516811615/Windows-11-Cheat-Sheet
15. Chrome What's New archive
    https://www.google.com/chrome/whats-new/archive/

16. XDA Developers, "Your Windows PC has a built-in maintenance tool that outperforms every paid optimizer on the market" (19 September 2026). Discovery source only; the comparative headline is not supported by published head-to-head measurements in the article.
    https://www.xda-developers.com/windows-pc-has-built-in-optimization-tool-hidden-plain-sight-beats-every-paid-alternative/

Several Scribd pages expose only previews or challenge pages. Those sources remain useful as provenance/topic maps, but cards below rely on independently checked documentation.

## ASCII INDEX

ID             | SECTION       | KEY
---------------+---------------+--------------------------------------------------------
SW-LIFE-001    | LIFECYCLE     | Windows 10 ended normal support in 2025
SW-LIFE-002    | LIFECYCLE     | Consumer Windows 10 ESU now runs to 2027
SW-LIFE-003    | LIFECYCLE     | Windows 11 support belongs to a version, not just "11"
SW-LIFE-004    | LIFECYCLE     | Windows 7 is unsupported
SW-LIFE-005    | SERVER        | Server 2022 is moving from mainstream to extended support
SW-LIFE-006    | SERVER        | Server 2025 is the current LTSC generation
SW-UI-001      | BASICS        | Win+X opens the Quick Link menu
SW-UI-002      | BASICS        | Win+V opens clipboard history
SW-UI-003      | BASICS        | Win+Shift+S captures a screen region
SW-UI-004      | BASICS        | Win+Tab and virtual desktops separate workspaces
SW-UI-005      | BASICS        | Win+Z exposes Windows 11 snap layouts
SW-UI-006      | BASICS        | Task Manager shows startup impact
SW-UI-007      | BASICS        | Windows Terminal is a host, not a replacement shell
SW-CMD-001     | CMD           | Ask the command itself for help
SW-CMD-002     | CMD           | Quote paths containing spaces
SW-CMD-003     | CMD           | Pipes and redirection connect small tools
SW-CMD-004     | CMD           | where finds executables and matching files
SW-CMD-005     | CMD           | findstr searches text
SW-CMD-006     | FILES         | robocopy is resilient, but /MIR deletes extras
SW-CMD-007     | PROCESSES     | tasklist inventories running processes
SW-CMD-008     | PROCESSES     | taskkill can terminate by PID or name
SW-CMD-009     | TASKS         | schtasks manages scheduled tasks
SW-NET-001     | NETWORK       | ipconfig /all is a first network snapshot
SW-NET-002     | NETWORK       | flush DNS without pretending it fixes everything
SW-NET-003     | NETWORK       | DHCP release/renew is not the same as assigning an IP
SW-NET-004     | NETWORK       | ping tests ICMP reachability, not whole-service health
SW-NET-005     | NETWORK       | tracert shows route behaviour, with caveats
SW-NET-006     | NETWORK       | pathping adds hop loss/latency sampling
SW-NET-007     | NETWORK       | netstat -ano links connections to PIDs
SW-NET-008     | NETWORK       | Test-NetConnection checks ports
SW-NET-009     | NETWORK       | Resolve-DnsName is a modern DNS diagnostic
SW-REP-001     | REPAIR        | Run DISM before SFC for component corruption
SW-REP-002     | REPAIR        | chkdsk without switches is read-only
SW-REP-003     | REPAIR        | prefer /scan before heavier chkdsk repairs
SW-REP-004     | RECOVERY      | System Restore is not a personal-file backup
SW-REP-005     | RECOVERY      | Reset, repair reinstall and clean install differ
SW-REP-006     | RECOVERY      | know the BitLocker recovery key before major recovery
SW-PWR-001     | POWER         | powercfg /batteryreport exposes battery history
SW-PWR-002     | POWER         | powercfg /energy diagnoses power inefficiency
SW-PWR-003     | POWER         | sleep reports can explain modern standby behaviour
SW-PKG-001     | WINGET        | search, then install by exact package ID
SW-PKG-002     | WINGET        | preview upgrades before winget upgrade --all
SW-PKG-003     | WINGET        | export/import can rebuild much of an app set
SW-PS-001      | POWERSHELL    | PowerShell pipes objects rather than display text
SW-PS-002      | POWERSHELL    | Get-Help, Get-Command and Get-Member are discovery tools
SW-PS-003      | POWERSHELL    | Get-CimInstance replaces most WMIC usage
SW-PS-004      | POWERSHELL    | execution policy is not a security boundary
SW-PS-005      | POWERSHELL    | Get-FileHash verifies downloaded file content
SW-PS-006      | POWERSHELL    | Get-WinEvent turns Event Viewer into queryable data
SW-LEG-001     | LEGACY        | WMIC is removed from Windows 11 24H2 and later
SW-LEG-002     | LEGACY        | PowerShell 2.0 is removed from modern Windows
SW-DEV-001     | DEV           | WSL is installed with wsl --install on supported systems
SW-DEV-002     | DEV           | OpenSSH is built into modern Windows as an optional feature
SW-OPT-001     | DEBLOAT       | safe debloat starts with uninstall and startup control
SW-OPT-002     | DEBLOAT       | Storage Sense is safer than mystery cleanup scripts
SW-OPT-003     | DEBLOAT       | do not mass-disable Windows services
SW-OPT-004     | DEBLOAT       | do not blindly remove AppX packages for every user
SW-OPT-005     | DEBLOAT       | registry tweaks need rollback and version evidence
SW-OPT-006     | PRIVACY       | configure diagnostic data through supported controls
SW-SEC-001     | SECURITY      | keep Defender and Firewall unless a managed replacement exists
SW-SEC-002     | SECURITY      | least privilege beats permanent administrator use
SW-SEC-003     | BACKUP        | Windows Backup is not the same thing as a full disk image
SW-ADM-001     | SERVER        | Active Directory is multi-master
SW-ADM-002     | SERVER        | FSMO roles handle operations that need one owner
SW-ADM-003     | SERVER        | DNS is foundational to Active Directory
SW-ADM-004     | SERVER        | gpupdate changes processing; gpresult explains results
SW-ADM-005     | SERVER        | RSAT lets a client manage server roles remotely
SW-ADM-006     | SERVER        | Windows Admin Center has no extra licence cost
SW-ADM-007     | SERVER        | remote management often beats routine RDP
SW-CHR-001     | CHROME        | Chrome vertical tabs are now built in
SW-CHR-002     | CHROME        | Chrome can sign and annotate PDFs
SW-CHR-003     | CHROME        | Chrome split view puts two pages in one tab
SW-WEB-001     | WEB ADMIN     | Search Console Domain property should be swindon.org.uk
SW-WEB-002     | WEB ADMIN     | submit sitemap.xml and expose it in robots.txt
SW-WEB-003     | WEB ADMIN     | URL Inspection is the correct single-page diagnostic
SW-WEB-004     | WEB ADMIN     | canonical signals should agree on one HTTPS URL
SW-WEB-005     | WEB ADMIN     | Cloudflare must not accidentally obstruct legitimate crawlers
SW-LIFE-007    | SERVER        | Server 2012/R2 ESU ends in October 2026
SW-LIFE-008    | SERVER        | Server 2016 extended support ends in January 2027
SW-LIFE-009    | SERVER        | Server 2019 extended support ends in January 2029
SW-CMD-010     | INVENTORY     | systeminfo captures OS and hardware configuration
SW-CMD-011     | IDENTITY      | whoami shows the current security token
SW-CMD-012     | DRIVERS       | driverquery inventories installed drivers
SW-CMD-013     | CLIPBOARD     | clip sends command output to the clipboard
SW-CMD-014     | CREDENTIALS   | cmdkey inventories and manages stored credentials
SW-FS-001      | PERMISSIONS   | icacls reads and changes NTFS permissions
SW-FS-002      | PERMISSIONS   | takeown recovers ownership but changes security state
SW-SVC-001     | SERVICES      | sc query inspects service and driver state
SW-EVT-001     | EVENTS        | wevtutil queries and exports event logs
SW-CFG-001     | REGISTRY      | reg query reads registry state without changing it
SW-SYS-001     | POWER         | shutdown schedules restart/shutdown and /a can abort
SW-ID-001      | ACCOUNTS      | net user lists or administers user accounts
SW-UPD-001     | WINDOWS UPDATE| ESU does not remove all supported update control
SW-UPD-002     | WINDOWS UPDATE| Controlled Update mode is safer than killing Windows Update
SW-UPD-003     | DRIVERS       | Windows Update drivers can be excluded on supported editions
SW-UPD-004     | DRIVERS       | roll back a driver after a bad Windows Update
SW-DRV-001     | DRIVERS       | export existing third-party drivers before changing them
SW-DRV-002     | DRIVERS       | AI may find driver candidates but must not choose blindly
SW-UPD-005     | RECOVERY      | use an update-recovery ladder before Reset this PC
SW-REG-001     | REGISTRY      | Windows stopped automatic RegBack in Windows 10 1803
SW-REG-002     | REGISTRY      | save touched registry keys before applying a profile
SW-BACK-001    | BACKUP        | build a recovery pack before debloat or update changes
SW-UPD-006     | WINDOWS UPDATE| ESU changes the security window, not every update-control rule
SW-REG-003     | REGISTRY      | downloadable RegBack enable and undo files
SW-OPT-007     | UPGRADE       | replacing an HDD with an SSD can transform an old PC
SW-OPT-008     | UPGRADE       | 8 GB RAM is a strong practical target for light Windows use
SW-OPT-009     | UPGRADE       | research the exact machine before buying RAM or SSD
SW-OPT-010     | UPGRADE       | an optical-bay caddy can reuse the old HDD
SW-OPT-011     | DEBLOAT       | Task Scheduler orchestrates maintenance; it does not optimise by itself
SW-OPT-012     | MAINTENANCE   | Windows can pause maintenance when you return to the PC
SW-OPT-013     | STORAGE       | Disk Cleanup can save named cleanup presets
SW-OPT-014     | DEBLOAT       | A hidden startup workload may be a scheduled task
SW-OPT-015     | BROWSER       | A browser cache is useful; routine purging can backfire
SW-AI-012      | AI            | Free Custom Instructions have a 1,500-character limit
SW-AI-013      | AI            | Audit memory sources before correcting or deleting
SW-AI-014      | AI            | Free Projects: five files, project-specific rules and safe sharing
SW-AI-015      | AI            | Live, Standard and Advanced Voice are different experiences
SW-AI-016      | AI            | Web search, chat search and search-query privacy are different
SW-AI-017      | AI            | Free allows existing GPTs, Library and Think, not GPT creation
SW-AI-018      | AI            | Privacy controls: training, Temporary Chat and deletion differ

---

# CARD LIBRARY

## SW-LIFE-001 | Windows 10 ended normal support in 2025

STATUS: VERIFIED
APPLIES_TO: Windows 10 22H2 Home, Pro, Enterprise and Education, with LTSC/LTSB exceptions handled separately
LIFECYCLE: UNSUPPORTED / ESU-ELIGIBLE IN SOME EDITIONS
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Normal Windows 10 support ended on 14 October 2025. A Windows 10 PC does not stop working on that date, but ordinary free security servicing ended for the final mainstream release, version 22H2. Long-term servicing editions have their own lifecycle dates.

### Aletheia check
Never say simply "Windows 10 is supported" or "unsupported" without checking edition and ESU status. A device can be beyond normal support yet still receive Extended Security Updates.

### Sources
- https://learn.microsoft.com/en-gb/lifecycle/announcements/windows-10-end-of-support
- https://learn.microsoft.com/en-us/windows/release-health/release-information

---

## SW-LIFE-002 | Consumer Windows 10 ESU now runs to 2027

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: eligible consumer Windows 10 22H2 Home, Pro, Pro Education and Workstations
LIFECYCLE: ESU
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Microsoft's current consumer ESU page says eligible Windows 10 22H2 devices can enrol in Extended Security Updates until 12 October 2027, and already-enrolled devices continue automatically to that date. ESU supplies critical and important security updates, not feature improvements or normal product support.

### Source-drift warning
Older 2025 and early-2026 material stated an October 2026 end date. The live Microsoft consumer page now supersedes that wording. This is exactly why lifecycle facts need a LAST_CHECKED field.

### Sources
- https://www.microsoft.com/windows/extended-security-updates
- https://support.microsoft.com/en-us/windows/deployment/updates-lifecycle/windows-10-support-has-ended-on-october-14-2025

---

## SW-LIFE-003 | Windows 11 support belongs to a version, not just "11"

STATUS: VERIFIED
APPLIES_TO: Windows 11
LIFECYCLE: CURRENT / VERSION-SPECIFIC
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows 11 has an annual feature-update cadence and each release has its own servicing window. As checked on 23 September 2026, Microsoft lists 24H2, 25H2 and 26H1 as current release families, with different end-of-update dates by edition.

### Useful current detail
Microsoft says 26H1 is scoped to new devices introduced in early 2026 and is not offered as an in-place feature update from 24H2 or 25H2 on existing PCs.

### Rule
Before giving a Windows 11 tweak, ask or detect the version with winver, Settings > System > About, or an equivalent supported method.

### Source
- https://learn.microsoft.com/en-us/windows/release-health/windows11-release-information

---

## SW-LIFE-004 | Windows 7 is unsupported

STATUS: VERIFIED
APPLIES_TO: Windows 7
LIFECYCLE: UNSUPPORTED
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Windows 7 normal support ended in January 2020 and its final Extended Security Updates ended in January 2023. It may still exist on isolated specialist equipment, but it should not be treated as a normally supported internet-connected desktop.

### Practical rule
For legacy machines, prioritise isolation, minimum services, restricted network access, current application compatibility where possible, and a replacement plan. Do not make an unsupported OS appear "safe" merely by disabling telemetry or installing a third-party antivirus.

### Source
- https://learn.microsoft.com/en-us/lifecycle/products/windows-7

---

## SW-LIFE-005 | Server 2022 is moving from mainstream to extended support

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows Server 2022
LIFECYCLE: SUPPORTED-LEGACY
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows Server 2022 remains supported, but it is reaching the boundary between mainstream and extended support in October 2026. Extended support then continues into 2031.

### Aletheia check
Microsoft pages have shown a one-day difference around the mainstream-support boundary depending on lifecycle/release-health presentation. For an operational deadline, check the live lifecycle page rather than hard-coding a date into automation.

### Source
- https://learn.microsoft.com/en-us/lifecycle/products/windows-server-2022

---

## SW-LIFE-006 | Server 2025 is the current LTSC generation

STATUS: VERIFIED
APPLIES_TO: Windows Server
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows Server 2025 is Microsoft's current Long-Term Servicing Channel Windows Server generation. Its lifecycle starts in 2024 and extends mainstream support into 2029 and extended support into 2034.

### Why useful
Old MCSE and Server 2000/2003 notes can still teach concepts, but current administration guidance should be anchored to Server 2016, 2019, 2022 and 2025, with legacy notes clearly labelled.

### Source
- https://learn.microsoft.com/en-us/lifecycle/products/windows-server-2025

---

## SW-UI-001 | Win+X opens the Quick Link menu

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows key + X opens the Quick Link menu, the same menu available by right-clicking Start. It gives fast access to system tools without memorising Control Panel paths.

### Why it belongs in Secret Windows
It is one of the quickest routes to Task Manager, Terminal/PowerShell, Settings and other administrative surfaces, and it survives UI rearrangements better than many click-by-click instructions.

### Source
- https://support.microsoft.com/en-us/windows/keyboard-shortcuts-in-windows-dcc61a57-8ff0-cffe-9796-cb9706c75eec

---

## SW-UI-002 | Win+V opens clipboard history

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows key + V opens clipboard history. The feature is not necessarily enabled by default, and Windows can prompt to enable it.

### Privacy note
Clipboard history may contain passwords, personal data or copied work material. Treat it as a convenience store, not a secret vault. Clear sensitive entries and be deliberate about any cross-device clipboard-synchronisation feature.

### Source
- https://support.microsoft.com/en-us/windows/keyboard-shortcuts-in-windows-dcc61a57-8ff0-cffe-9796-cb9706c75eec

---

## SW-UI-003 | Win+Shift+S captures a screen region

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows key + Shift + S starts a screen-region capture into the clipboard through Snipping Tool behaviour. It is usually faster than taking a full-screen screenshot and cropping afterwards.

### Useful twist
Current Windows also supports additional Snipping Tool capabilities on newer releases, including screen recording shortcuts. Version-specific features should be checked before documenting them as universal.

### Source
- https://support.microsoft.com/en-us/windows/keyboard-shortcuts-in-windows-dcc61a57-8ff0-cffe-9796-cb9706c75eec

---

## SW-UI-004 | Win+Tab and virtual desktops separate workspaces

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows key + Tab opens Task View. Virtual desktops let one PC hold separate workspaces, for example work, research and personal browsing, without closing applications.

### Useful shortcuts
- Win+Ctrl+D: create a virtual desktop.
- Win+Ctrl+Left/Right: move between desktops.
- Win+Ctrl+F4: close the current desktop.

Closing a desktop does not normally close its applications; Windows moves them to another desktop.

### Source
- https://support.microsoft.com/en-us/windows/keyboard-shortcuts-in-windows-dcc61a57-8ff0-cffe-9796-cb9706c75eec

---

## SW-UI-005 | Win+Z exposes Windows 11 snap layouts

STATUS: VERIFIED
APPLIES_TO: Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
On Windows 11, Windows key + Z opens Snap Layouts so windows can be arranged into predefined screen zones.

### Version trap
Older Windows shortcut lists may describe Win+Z differently. Shortcut meaning can change by Windows generation, so a cheat sheet without an APPLIES_TO field is a future fossil waiting politely on the shelf.

### Source
- https://support.microsoft.com/en-us/windows/keyboard-shortcuts-in-windows-dcc61a57-8ff0-cffe-9796-cb9706c75eec

---

## SW-UI-006 | Task Manager shows startup impact

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Task Manager's Startup apps view shows which registered programs launch at sign-in and estimates their startup impact. Settings > Apps > Startup provides another supported interface.

### Safe optimisation
Disable a non-essential startup app before uninstalling or deleting anything. If the machine improves and nothing useful disappears, the change is easily reversible.

### Source
- https://support.microsoft.com/en-US/Windows/Experience/Startup-Boot/configure-startup-applications-in-windows

---

## SW-UI-007 | Windows Terminal is a host, not a replacement shell

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10 22H2 with suitable updates, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows Terminal is a modern terminal application that can host Command Prompt, Windows PowerShell, PowerShell 7, WSL distributions and other command-line profiles. The shell and the terminal are different layers.

### Why it matters
A command that works in cmd.exe may use different quoting, operators or variables in PowerShell. "Open Terminal" does not by itself tell you which shell is running.

### Sources
- https://learn.microsoft.com/en-us/windows/terminal/
- https://learn.microsoft.com/en-us/windows/terminal/customize-settings/startup

---

## SW-CMD-001 | Ask the command itself for help

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Before copying an old command-line example, ask the installed command for help. In Command Prompt, HELP lists commands and HELP command gives details for many built-ins. Many executables also support command /?.

Example:

    help robocopy
    ipconfig /?
    schtasks /?

### Why useful
The local help reflects what is actually installed, while a decade-old cheat sheet may quietly describe a retired switch.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/help

---

## SW-CMD-002 | Quote paths containing spaces

STATUS: VERIFIED
APPLIES_TO: Windows command line
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
A path containing spaces should normally be quoted so the shell treats it as one argument.

Example:

    cd /d "C:\Program Files"
    robocopy "C:\My Files" "D:\Backup Files" /E

### Shell warning
Command Prompt and PowerShell have different parsing rules. Do not assume an escape sequence or variable expression copied for one shell behaves identically in the other.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/cmd

---

## SW-CMD-003 | Pipes and redirection connect small tools

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Command Prompt, with different semantics in PowerShell
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Command Prompt can send output into another command with |, replace a file with >, append with >>, and redirect error output using stream notation. This makes small commands composable.

Examples:

    tasklist | findstr /i chrome
    ipconfig /all > "%USERPROFILE%\Desktop\network.txt"

### PowerShell distinction
PowerShell pipelines normally pass objects rather than merely formatted text. That difference is one of the biggest reasons to prefer PowerShell for structured administration.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/cmd

---

## SW-CMD-004 | where finds executables and matching files

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
WHERE searches locations for files matching a pattern and is especially useful for finding which executable will run from PATH.

Examples:

    where powershell
    where winget
    where /r C:\Tools *.exe

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/where

---

## SW-CMD-005 | findstr searches text

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
FINDSTR searches text files using literal or regular-expression matching and can recurse through folders. In PowerShell, Select-String is the more natural object-aware counterpart.

Examples:

    findstr /i "error failed" app.log
    findstr /s /n /i "ProjectWise" *.txt

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/findstr

---

## SW-CMD-006 | robocopy is resilient, but /MIR deletes extras

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: HIGH WITH /MIR, /PURGE, /MOV OR /MOVE
LAST_CHECKED: 2026-09-23

### Summary
ROBOCOPY is a robust file-copy tool with restartable copying, multithreading, filtering and logging. It is excellent for large trees and unreliable links.

### Safe pattern
Test dangerous jobs with /L first. /L lists what would happen without copying, deleting or timestamping.

Example dry run:

    robocopy "C:\Source" "D:\Backup" /E /L

### Danger
/MIR equals /E plus /PURGE. Files present only in the destination can be deleted. /MOVE and /MOV delete source items after copying. Never paste those switches into an unfamiliar path.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/robocopy

---

## SW-CMD-007 | tasklist inventories running processes

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
TASKLIST displays running processes and can include service or verbose information. It is useful when Task Manager is inconvenient or output needs to be filtered or saved.

Examples:

    tasklist
    tasklist /svc
    tasklist /fi "IMAGENAME eq chrome.exe"

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/tasklist

---

## SW-CMD-008 | taskkill can terminate by PID or name

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
TASKKILL can end a process by process ID or image name. /F forces termination and /T includes child processes.

### Rule
First identify the process. Prefer the application's own exit route. Forced termination can lose unsaved work or interrupt a service in the middle of writing data.

Example:

    tasklist /fi "IMAGENAME eq notepad.exe"
    taskkill /pid 1234

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/taskkill

---

## SW-CMD-009 | schtasks manages scheduled tasks

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
SCHTASKS can create, query, run, stop, change and delete scheduled tasks. It is the scriptable counterpart to Task Scheduler.

### Safe first move
Query before changing:

    schtasks /query /fo LIST /v

Administrative rights are required for many system-wide or remote operations.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/schtasks

---

## SW-NET-001 | ipconfig /all is a first network snapshot

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, supported Windows Server
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
IPCONFIG /ALL shows adapter configuration including addresses, DHCP state, default gateways and DNS servers. Capture it before making network changes.

Example:

    ipconfig /all

### Diagnostic sequence
Start with configuration, then name resolution, then route/port tests. Randomly resetting the entire network stack before observing it destroys useful evidence.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ipconfig

---

## SW-NET-002 | flush DNS without pretending it fixes everything

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, supported Windows Server
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
IPCONFIG /FLUSHDNS clears the DNS client resolver cache. PowerShell also provides Clear-DnsClientCache.

Examples:

    ipconfig /flushdns
    Clear-DnsClientCache

### Aletheia check
Flushing the cache helps when stale local DNS data is the problem. It does not repair a dead network adapter, a bad DNS server, a routing failure, a TLS certificate problem or a website outage.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ipconfig

---

## SW-NET-003 | DHCP release/renew is not the same as assigning an IP

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: DHCP-configured Windows adapters
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
IPCONFIG /RELEASE drops a DHCP lease and /RENEW asks DHCP for configuration again. These actions can temporarily remove network connectivity.

Examples:

    ipconfig /release
    ipconfig /renew

### Correction to old cheat sheets
PowerShell New-NetIPAddress and Remove-NetIPAddress create or remove IP address configuration. They are not simply synonyms for "DHCP release" and "DHCP renew". Treat static-address administration and DHCP-client lease operations as different tasks.

### Sources
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ipconfig
- https://learn.microsoft.com/en-us/powershell/module/nettcpip/

---

## SW-NET-004 | ping tests ICMP reachability, not whole-service health

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, supported Windows Server
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
PING sends ICMP echo requests. A reply shows that this particular form of network traffic reached the target and came back.

### Caveat
No reply does not prove the host is down. Firewalls and routers can block ICMP while web, file or application services remain healthy. Conversely, a successful ping does not prove a specific TCP service is listening.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/ping

---

## SW-NET-005 | tracert shows route behaviour, with caveats

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, supported Windows Server
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
TRACERT sends packets with increasing TTL values to reveal intermediate hops towards a destination.

### Caveat
Asterisks at an intermediate hop can mean that a router does not return the expected ICMP response. They do not automatically prove packet loss for the real application traffic.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/tracert

---

## SW-NET-006 | pathping adds hop loss/latency sampling

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, supported Windows Server
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
PATHPING combines route discovery with a longer sampling period that estimates latency and packet loss at hops. It is slower than TRACERT but can be more informative for intermittent path problems.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/pathping

---

## SW-NET-007 | netstat -ano links connections to PIDs

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, supported Windows Server
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
NETSTAT can show active connections and listening ports. The common -a -n -o combination shows all connections/listeners numerically and includes the owning process ID.

Example:

    netstat -ano

Then match a PID using Task Manager, TASKLIST or PowerShell.

### Security note
A listening port is evidence of a process listening. It is not by itself evidence of malware.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/netstat

---

## SW-NET-008 | Test-NetConnection checks ports

STATUS: VERIFIED
APPLIES_TO: Windows PowerShell on supported Windows
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Test-NetConnection can combine name resolution and connectivity tests and can explicitly test a TCP port.

Examples:

    Test-NetConnection example.com
    Test-NetConnection example.com -Port 443

### Why useful
This is a better answer than PING when the question is "can this computer reach the web service on TCP 443?"

### Source
- https://learn.microsoft.com/en-us/powershell/module/nettcpip/test-netconnection?view=windowsserver2025-ps

---

## SW-NET-009 | Resolve-DnsName is a modern DNS diagnostic

STATUS: VERIFIED
APPLIES_TO: supported Windows client/server with DnsClient PowerShell module
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Resolve-DnsName performs DNS queries from PowerShell and gives structured results that are easy to filter or automate.

Example:

    Resolve-DnsName swindon.org.uk

NSLOOKUP remains useful and widely installed, but structured PowerShell output is better for repeatable diagnostics.

### Source
- https://learn.microsoft.com/en-us/powershell/module/dnsclient/resolve-dnsname?view=windowsserver2025-ps

---

## SW-REP-001 | Run DISM before SFC for component corruption

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
ADMIN_REQUIRED: YES
LAST_CHECKED: 2026-09-23

### Summary
Microsoft's current repair guidance runs DISM first so the Windows component source used by System File Checker is healthy, then runs SFC.

Commands:

    DISM.exe /Online /Cleanup-image /Restorehealth
    sfc /scannow

### Rule
Do not close the SFC window until verification completes. If DISM needs an alternate repair source, use Microsoft's documented /Source and /LimitAccess procedure rather than inventing a random ISO path.

### Source
- https://support.microsoft.com/en-us/windows/experience/backup-recovery/use-the-system-file-checker-tool-to-repair-missing-or-corrupted-system-files

---

## SW-REP-002 | chkdsk without switches is read-only

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW WITHOUT REPAIR SWITCHES
LAST_CHECKED: 2026-09-23

### Summary
Running CHKDSK without repair parameters checks and reports volume/file-system status. It does not repair errors.

Example:

    chkdsk C:

### Why useful
Observation first is safer than immediately forcing an offline repair. The command's /F, /R, /X and related switches change the operation and can require locking or dismounting a volume.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/chkdsk

---

## SW-REP-003 | prefer /scan before heavier chkdsk repairs

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: NTFS on current Windows
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
ADMIN_REQUIRED: USUALLY YES
LAST_CHECKED: 2026-09-23

### Summary
CHKDSK /SCAN performs an online NTFS scan. /F fixes logical errors. /R includes /F and also reads for physical disk errors, which can take much longer.

### Safe sequence
For a live NTFS volume, start with observation or /SCAN unless evidence specifically calls for a repair. Back up important data before intensive disk work if drive failure is plausible.

### SSD note
Microsoft cautions that repeated full-surface scans with /R are unnecessary wear. Occasional diagnostic use is not treated as a major SSD hazard.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/chkdsk

---

## SW-REP-004 | System Restore is not a personal-file backup

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
System Restore rolls system files, registry settings, drivers and installed-program state back to a restore point. It is designed not to restore ordinary personal documents.

### Consequence
A restore point is useful before risky configuration work, but it does not replace backing up user data. Newer Windows 11 builds may also have newer recovery mechanisms; do not confuse them with classic System Restore.

### Source
- https://support.microsoft.com/en-us/windows/experience/backup-recovery/backup-restore-and-recovery-in-windows

---

## SW-REP-005 | Reset, repair reinstall and clean install differ

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, with some options Windows-11-only
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: HIGH
LAST_CHECKED: 2026-09-23

### Summary
Windows recovery options differ in what they preserve. System Restore changes system state. Reset this PC reinstalls Windows and can keep or remove personal files, but removes apps/settings. A Windows Update repair reinstall on supported Windows 11 versions can preserve files, apps and settings. A clean installation can remove everything.

### Rule
Use the least disruptive recovery option that addresses the problem. Back up important files first.

### Source
- https://support.microsoft.com/en-us/windows/experience/backup-recovery/recovery-options-in-windows

---

## SW-REP-006 | know the BitLocker recovery key before major recovery

STATUS: VERIFIED
APPLIES_TO: encrypted Windows 10/11 devices
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: HIGH IF KEY IS LOST
LAST_CHECKED: 2026-09-23

### Summary
Windows Recovery Environment and hardware/security changes can require the 48-digit BitLocker recovery key. Microsoft Support cannot recreate a lost key.

### Rule
Before BIOS/UEFI changes, storage work or major recovery, confirm where the key is stored. Possible locations include a Microsoft account, work/school account, printout or USB file depending on how encryption was configured.

### Source
- https://support.microsoft.com/en-gb/windows/security/encryption/find-your-bitlocker-recovery-key

---

## SW-PWR-001 | powercfg /batteryreport exposes battery history

STATUS: VERIFIED
APPLIES_TO: Windows portable devices
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
POWERCFG /BATTERYREPORT generates an HTML report with battery usage and capacity history.

Example:

    powercfg /batteryreport /output "%USERPROFILE%\Desktop\battery-report.html"

### Why useful
Comparing design capacity with recent full-charge capacity can help distinguish a tired battery from a software complaint about short runtime.

### Source
- https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/powercfg-command-line-options

---

## SW-PWR-002 | powercfg /energy diagnoses power inefficiency

STATUS: VERIFIED
APPLIES_TO: current Windows
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
POWERCFG /ENERGY observes the system and generates a report about power-efficiency problems. Microsoft recommends running it while the computer is idle with no open documents/programs affecting the test.

Example:

    powercfg /energy /output energy-report.html

### Source
- https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/powercfg-command-line-options

---

## SW-PWR-003 | sleep reports can explain modern standby behaviour

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: hardware/Windows configurations supporting the relevant sleep analysis
LIFECYCLE: MIXED
EVIDENCE: GOOD
CONFIDENCE: MEDIUM-HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
POWERCFG includes diagnostic reports such as /SLEEPSTUDY on compatible systems. They can show why a laptop consumed power while apparently asleep.

### Rule
Feature availability depends on platform sleep model and Windows build. Query powercfg /? and current Microsoft documentation before automating a report across mixed hardware.

### Source
- https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/powercfg-command-line-options

---

## SW-PKG-001 | search, then install by exact package ID

STATUS: VERIFIED
APPLIES_TO: Windows with App Installer / WinGet
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
WinGet can search, inspect and install applications. For repeatability, use an exact package ID rather than relying on a fuzzy name match.

Pattern:

    winget search powershell
    winget show --id Microsoft.PowerShell
    winget install --id Microsoft.PowerShell -e

### Security note
Use trusted sources. Do not bypass installer hash checks merely to make a failing installation "work".

### Source
- https://learn.microsoft.com/en-us/windows/package-manager/winget/install

---

## SW-PKG-002 | preview upgrades before winget upgrade --all

STATUS: VERIFIED
APPLIES_TO: Windows with WinGet
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Running WINGET UPGRADE with no package argument lists available upgrades. Microsoft explicitly recommends this preview before WINGET UPGRADE --ALL.

Pattern:

    winget upgrade
    winget upgrade --all

### Why useful
Bulk updating is convenient, but previewing catches packages you might want pinned, handled by a vendor tool, or deferred during a critical job.

### Source
- https://learn.microsoft.com/en-us/windows/package-manager/winget/upgrade

---

## SW-PKG-003 | export/import can rebuild much of an app set

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows with WinGet
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
WINGET EXPORT creates a JSON list of matched applications; WINGET IMPORT can use that file to reinstall them in sequence. This is useful before rebuilding a PC.

Examples:

    winget export -o apps.json
    winget import -i apps.json

### Caveat
Export cannot identify every installed program if its local metadata cannot be matched to a configured WinGet source. Treat the JSON as a useful rebuild manifest, not a complete machine image.

### Sources
- https://learn.microsoft.com/windows/package-manager/winget/export
- https://learn.microsoft.com/en-us/windows/package-manager/winget/import

---

## SW-PS-001 | PowerShell pipes objects rather than display text

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows PowerShell 5.1 and PowerShell 7.x
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
PowerShell commands usually emit .NET objects with named properties. The pipeline can pass those objects to later commands without reparsing columns of display text.

Example:

    Get-Process | Sort-Object CPU -Descending | Select-Object -First 10 Name,CPU,Id

### Why useful
This is the conceptual leap that makes PowerShell more reliable than long chains of FINDSTR parsing for structured administration.

### Source
- https://learn.microsoft.com/en-us/powershell/scripting/learn/ps101/04-pipelines

---

## SW-PS-002 | Get-Help, Get-Command and Get-Member are discovery tools

STATUS: VERIFIED
APPLIES_TO: Windows PowerShell / PowerShell
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
PowerShell can explain itself:
- Get-Command discovers commands.
- Get-Help explains syntax and examples.
- Get-Member reveals properties and methods on pipeline objects.

Examples:

    Get-Command *Dns*
    Get-Help Get-WinEvent -Examples
    Get-Process | Get-Member

### Source
- https://learn.microsoft.com/en-us/powershell/scripting/learn/ps101/02-help-system

---

## SW-PS-003 | Get-CimInstance replaces most WMIC usage

STATUS: VERIFIED
APPLIES_TO: modern Windows PowerShell / PowerShell on Windows
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
The CIM cmdlets query Windows Management Instrumentation through modern PowerShell interfaces. They are the preferred migration path for many old WMIC one-liners.

Examples:

    Get-CimInstance Win32_OperatingSystem
    Get-CimInstance Win32_BIOS
    Get-CimInstance Win32_LogicalDisk

### Source
- https://learn.microsoft.com/en-us/powershell/module/cimcmdlets/
- https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_wql?view=powershell-7.5

---

## SW-PS-004 | execution policy is not a security boundary

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: PowerShell
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
PowerShell execution policy helps prevent accidental execution of untrusted scripts and can enforce organisational policy choices, but Microsoft explicitly describes it as a safety feature rather than a security boundary.

### Rule
Do not respond to a blocked script by permanently setting the machine to the least restrictive policy. Understand the script, its provenance, scope and signing first.

### Source
- https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies

---

## SW-PS-005 | Get-FileHash verifies downloaded file content

STATUS: VERIFIED
APPLIES_TO: PowerShell
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Get-FileHash calculates a content hash. SHA256 is the default in current PowerShell documentation.

Example:

    Get-FileHash .\download.iso

### Correct use
Compare the result with a hash published through a trusted channel by the software vendor. Matching hashes show content equality with the reference; they do not prove that the reference itself came from a trustworthy source.

### Source
- https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/get-filehash?view=powershell-7.5

---

## SW-PS-006 | Get-WinEvent turns Event Viewer into queryable data

STATUS: VERIFIED
APPLIES_TO: PowerShell on Windows
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Get-WinEvent reads classic Windows logs and ETW-backed event logs and can filter by log, provider, event ID, time and structured queries.

Example:

    Get-WinEvent -LogName System -MaxEvents 50

### Why useful
Event Viewer is excellent for exploration. PowerShell is better when the same diagnostic query must be repeated across machines or saved as evidence.

### Source
- https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.diagnostics/get-winevent?view=powershell-7.5

---

## SW-LEG-001 | WMIC is removed from Windows 11 24H2 and later

STATUS: REMOVED
APPLIES_TO: Windows 11 24H2 and later
LIFECYCLE: REMOVED
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
The WMIC command-line utility has been removed from Windows 11 24H2 and later, and as of August 2026 is no longer available there as a Feature on Demand. WMI itself remains supported.

### Migration
Replace WMIC scripting with PowerShell CIM cmdlets or supported WMI APIs.

### Why this matters
A giant A-to-Z Windows command list can be historically accurate and still be wrong for a current computer.

### Source
- https://learn.microsoft.com/en-us/windows/whats-new/removed-features

---

## SW-LEG-002 | PowerShell 2.0 is removed from modern Windows

STATUS: REMOVED
APPLIES_TO: Windows 11 24H2 and Windows Server 2025 after current servicing
LIFECYCLE: REMOVED
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Microsoft removed the legacy Windows PowerShell 2.0 component from Windows 11 24H2 beginning in August 2025 and from Windows Server 2025 beginning in September 2025. PowerShell 5.1 and modern PowerShell 7.x remain the relevant families.

### Rule
Scripts that explicitly require version 2.0 should be modernised rather than preserving the obsolete engine.

### Source
- https://learn.microsoft.com/en-us/windows/whats-new/removed-features

---

## SW-DEV-001 | WSL is installed with wsl --install on supported systems

STATUS: VERIFIED
APPLIES_TO: supported Windows 10/11 configurations
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
ADMIN_REQUIRED: INSTALLATION USUALLY YES
LAST_CHECKED: 2026-09-23

### Summary
Windows Subsystem for Linux can install a Linux distribution without a separate virtual-machine workflow.

Typical commands:

    wsl --install
    wsl --list --online
    wsl --install -d Ubuntu

### Use case
WSL is excellent when Linux command-line tools or build environments are genuinely required. It is not necessary merely to run basic Windows administration commands.

### Source
- https://learn.microsoft.com/en-us/windows/wsl/install

---

## SW-DEV-002 | OpenSSH is built into modern Windows as an optional feature

STATUS: VERIFIED
APPLIES_TO: Windows 10 build 1809+, Windows 11, Server 2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Microsoft provides OpenSSH client/server components as Windows features. Windows Server 2025 includes them by default, although the server service still needs enabling/configuration.

### Security rule
Do not enable sshd merely because it exists. A listening remote-management service should have a clear purpose, firewall scope, authentication policy and patching plan.

### Sources
- https://learn.microsoft.com/en-us/windows-server/administration/openssh/openssh-overview
- https://learn.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse

---

## SW-OPT-001 | safe debloat starts with uninstall and startup control

STATUS: METHOD
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW TO MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
A safe Windows "debloat" order is:

1. Measure the actual problem.
2. Uninstall ordinary apps you do not use.
3. Disable unnecessary startup apps.
4. Review background behaviour and notifications.
5. Use supported storage cleanup.
6. Remove optional Windows features only when their purpose is understood.
7. Touch services, policy or registry only for a documented reason with rollback.

### Principle
Performance tuning should reduce work the user does not need, not dismantle Windows until benchmarks look tidy.

### Sources
- https://support.microsoft.com/en-us/windows/uninstall-or-remove-apps-and-programs-in-windows-4b55f974-2cc6-2d2b-d092-5905080eaf98
- https://support.microsoft.com/en-US/Windows/Experience/Startup-Boot/configure-startup-applications-in-windows

---

## SW-OPT-002 | Storage Sense is safer than mystery cleanup scripts

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW TO MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Storage Sense can remove temporary files and age out Recycle Bin content automatically. By default it does not touch Downloads or cloud content unless configured to do so.

### Why useful
It uses supported Windows mechanisms and exposes the policy to the user. That is preferable to a downloaded "cleaner" that deletes unknown caches, servicing files or registry entries.

### Source
- https://support.microsoft.com/en-us/windows/experience/storage-filemanagement/manage-drive-space-with-storage-sense

---

## SW-OPT-003 | do not mass-disable Windows services

STATUS: METHOD
APPLIES_TO: Windows 10, Windows 11, Windows Server
LIFECYCLE: CURRENT
EVIDENCE: CONTEXT
CONFIDENCE: HIGH
RISK: HIGH
LAST_CHECKED: 2026-09-23

### Summary
Service lists copied from "gaming tweaks" or old Windows builds age badly. A service that appears idle may support updates, networking, Store/MSIX installation, device discovery, WMI, security or an application dependency.

### Safe method
- Measure the symptom first.
- Identify the service and its dependencies.
- Prefer changing an application's own settings.
- Change one thing at a time.
- Record the original startup type.
- Reboot and test the functions that depend on it.

### Rule
Aletheia Debloat must never contain a universal "disable these 40 services" button.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/sc-query

---

## SW-OPT-004 | do not blindly remove AppX packages for every user

STATUS: METHOD
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT / BUILD-SPECIFIC
EVIDENCE: CONTEXT
CONFIDENCE: HIGH
RISK: HIGH
LAST_CHECKED: 2026-09-23

### Summary
PowerShell can remove provisioned or installed app packages, but broad commands copied from debloat scripts can affect new-user provisioning, Store-managed components and app dependencies.

### Safer approach
Use normal uninstall first. If a built-in app cannot be removed through supported UI, confirm whether it is actually causing a measurable problem before escalating to package manipulation.

### Source
- https://support.microsoft.com/en-us/windows/uninstall-or-remove-apps-and-programs-in-windows-4b55f974-2cc6-2d2b-d092-5905080eaf98

---

## SW-OPT-005 | registry tweaks need rollback and version evidence

STATUS: METHOD
APPLIES_TO: Windows
LIFECYCLE: MIXED
EVIDENCE: CONTEXT
CONFIDENCE: HIGH
RISK: HIGH
LAST_CHECKED: 2026-09-23

### Summary
Registry edits can change behaviour that has no exposed GUI, but keys can move, be ignored, be overridden by policy, or gain a different meaning in later Windows builds.

### Before editing
- Confirm the exact Windows version/edition.
- Prefer documented policy or Settings.
- Export the affected key or record its original value.
- Change the smallest scope possible.
- Test after one change.
- Keep a recovery path.

Microsoft's own startup-app documentation cautions that registry changes can have unintended consequences.

### Source
- https://support.microsoft.com/en-US/Windows/Experience/Startup-Boot/configure-startup-applications-in-windows

---

## SW-OPT-006 | configure diagnostic data through supported controls

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, with edition/management differences
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Windows exposes supported privacy and diagnostic-data controls in Settings and, for managed devices, policy/MDM. Diagnostic Data Viewer can show categories of diagnostic data on supported releases.

### Aletheia check
Avoid claims that a registry pack makes Windows "zero telemetry". Some data is necessary for security, update and service operation, settings differ by edition, and Microsoft changes policy names over time.

### Sources
- https://learn.microsoft.com/en-us/windows/privacy/configure-windows-diagnostic-data-in-your-organization
- https://support.microsoft.com/en-us/windows/view-your-diagnostic-data-with-the-diagnostic-data-viewer

---

## SW-SEC-001 | keep Defender and Firewall unless a managed replacement exists

STATUS: METHOD
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: CONTEXT
CONFIDENCE: HIGH
RISK: HIGH
LAST_CHECKED: 2026-09-23

### Summary
Security components are not "bloat" merely because they consume CPU, memory or background activity. Disabling Microsoft Defender protections or Windows Firewall to gain a tiny benchmark improvement increases attack surface.

### Rule
A security product can be replaced by an appropriate managed alternative, but "turn it off because gaming" is not an Aletheia optimisation card.

### Source
- https://support.microsoft.com/en-us/windows/stay-protected-with-windows-security

---

## SW-SEC-002 | least privilege beats permanent administrator use

STATUS: METHOD
APPLIES_TO: Windows client/server
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Run ordinary work with ordinary privileges and elevate only when a task needs administration. User Account Control makes privileged actions visible and helps prevent every process from receiving administrator rights by default.

### Admin-script rule
A knowledge card should state ADMIN_REQUIRED rather than telling the user to keep an elevated terminal open indefinitely.

### Source
- https://learn.microsoft.com/en-us/windows/security/application-security/application-control/user-account-control/

---

## SW-SEC-003 | Windows Backup is not the same thing as a full disk image

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows Backup can preserve files through OneDrive plus many settings, app information and Wi-Fi details associated with a Microsoft account. It is useful for migration and recovery.

### Caveat
That is different from a complete sector-level or system-image backup. Recovery Drive also does not include personal files. Choose backup method according to what must be restorable.

### Sources
- https://support.microsoft.com/en-us/windows/experience/backup-recovery/back-up-and-restore-with-windows-backup
- https://support.microsoft.com/en-us/windows/experience/backup-recovery/backup-restore-and-recovery-in-windows

---

## SW-ADM-001 | Active Directory is multi-master

STATUS: VERIFIED
APPLIES_TO: Active Directory Domain Services on supported Windows Server
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Modern Active Directory Domain Services is a multi-master directory: ordinary directory changes can be accepted by multiple domain controllers and replicated.

### Old-note correction
Windows NT's Primary Domain Controller / Backup Domain Controller architecture should not be taught as the model for current AD. Active Directory does retain a PDC Emulator FSMO role, but that is one specialised role inside a multi-master system, not a return to NT's PDC/BDC design.

### Sources
- https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/planning-operations-master-role-placement
- https://learn.microsoft.com/en-us/troubleshoot/windows-server/active-directory/fsmo-roles

---

## SW-ADM-002 | FSMO roles handle operations that need one owner

STATUS: VERIFIED
APPLIES_TO: supported Active Directory Domain Services
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
AD has five Flexible Single Master Operations roles. Three are domain-level: PDC Emulator, RID Master and Infrastructure Master. Two are forest-level: Schema Master and Domain Naming Master.

### Why
Most directory writes can replicate multi-master. Certain operations are deliberately single-owner to avoid conflicts.

### Source
- https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/manage/understand-fsmo-roles

---

## SW-ADM-003 | DNS is foundational to Active Directory

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Active Directory environments
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: HIGH
LAST_CHECKED: 2026-09-23

### Summary
Active Directory relies heavily on DNS service records and name resolution for clients and domain controllers to locate AD services.

### Diagnostic rule
When a domain logon, Group Policy or replication problem appears "mysterious", verify client DNS configuration and AD DNS health before inventing an authentication theory.

### Source
- https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/dns-and-ad-ds

---

## SW-ADM-004 | gpupdate changes processing; gpresult explains results

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025 in Group Policy scenarios
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW TO MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
GPUPDATE refreshes Group Policy. /FORCE reapplies all policy rather than only changes. GPRESULT reports the Resultant Set of Policy that actually applied.

Examples:

    gpupdate
    gpresult /r
    gpresult /h "%USERPROFILE%\Desktop\policy.html"

### Diagnostic principle
Before repeatedly forcing policy, use GPRESULT to learn which policy won and whether the expected object/user scope is present.

### Sources
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/gpupdate
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/gpresult

---

## SW-ADM-005 | RSAT lets a client manage server roles remotely

STATUS: VERIFIED
APPLIES_TO: Windows 10/11 Pro or Enterprise and supported Windows Server
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Remote Server Administration Tools provide Server Manager, MMC snap-ins, PowerShell modules and command-line tools for managing Windows Server roles from an administrator's client machine.

### Current install model
On modern Windows client, RSAT components are Features on Demand / Optional Features rather than the old standalone-download model used by earlier Windows generations.

### Source
- https://learn.microsoft.com/windows-server/remote/remote-server-administration-tools

---

## SW-ADM-006 | Windows Admin Center has no extra licence cost

STATUS: VERIFIED
APPLIES_TO: Windows Server / supported Windows clients
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Windows Admin Center is Microsoft's browser-based management tool for Windows Server and Windows systems. Microsoft states that it has no additional cost beyond valid Windows licensing.

### Why useful
It centralises many everyday server tasks and reduces the need to open a separate remote desktop session for every piece of routine administration.

### Source
- https://learn.microsoft.com/en-us/windows-server/manage/windows-admin-center/understand/faq

---

## SW-ADM-007 | remote management often beats routine RDP

STATUS: METHOD
APPLIES_TO: supported Windows Server
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Server Manager, PowerShell remoting, RSAT and Windows Admin Center let administrators manage roles, services, events and configuration remotely. RDP remains useful, but it should not be the automatic answer for every server task.

### Benefits
Remote management is more scriptable, auditable and scalable, and it works well with Server Core where a full desktop is intentionally absent.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/overview

---

## SW-CHR-001 | Chrome vertical tabs are now built in

STATUS: VERIFIED
APPLIES_TO: current desktop Chrome where feature is available
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Chrome's current What's New archive describes vertical tabs that move the tab strip to the side, show more of long titles and make tab groups easier to manage.

### How
Right-click the tab strip and choose Show tabs vertically.

### Source
- https://www.google.com/chrome/whats-new/archive/

---

## SW-CHR-002 | Chrome can sign and annotate PDFs

STATUS: VERIFIED
APPLIES_TO: current desktop Chrome where feature is available
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Chrome's built-in PDF viewer now includes annotation tools for hand-drawn marks, highlights and signatures, with a save step.

### Privacy note
A hand-drawn signature is sensitive personal data. Save signed documents deliberately and avoid treating a browser profile shared with others as private storage.

### Source
- https://www.google.com/chrome/whats-new/archive/

---

## SW-CHR-003 | Chrome split view puts two pages in one tab

STATUS: VERIFIED
APPLIES_TO: current desktop Chrome where feature is available
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Chrome Split View can show two pages side-by-side inside the same tab. Google documents dragging a tab to the left or right edge of the browser window, or using Open Link in Split View from a link's context menu.

### Use
Useful for comparing documentation with a terminal, form or note page without juggling separate windows.

### Source
- https://www.google.com/chrome/whats-new/archive/

---

# WEB ADMIN CROSSOVER

These cards are appended because Windows administration, browser testing, DNS, Search Console and Cloudflare are all part of the same practical troubleshooting chain for a static website. They are not intended to turn Secret Windows into a general SEO library.

## SW-WEB-001 | Search Console Domain property should be swindon.org.uk

STATUS: VERIFIED
APPLIES_TO: swindon.org.uk
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
For full-domain coverage in Google Search Console, create a Domain property using:

    swindon.org.uk

Do not include https:// and do not prefix www. A Domain property covers protocols and subdomains and requires DNS-record verification.

### Consequence
There is no need for special Google ownership code in .htaccess when the site is verified as a Domain property through DNS.

### Source
- https://support.google.com/webmasters/answer/34592

---

## SW-WEB-002 | submit sitemap.xml and expose it in robots.txt

STATUS: VERIFIED
APPLIES_TO: swindon.org.uk
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Keep the sitemap on the site, preferably at the root, make sure Googlebot can fetch it, and submit its URL in Search Console's Sitemaps report.

For this site the intended URL is:

    https://swindon.org.uk/sitemap.xml

The robots.txt file can also advertise:

    Sitemap: https://swindon.org.uk/sitemap.xml

### Caveat
A sitemap is a discovery and canonicalisation signal, not a guarantee of indexing.

### Source
- https://support.google.com/webmasters/answer/7451001

---

## SW-WEB-003 | URL Inspection is the correct single-page diagnostic

STATUS: VERIFIED
APPLIES_TO: Google Search Console
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Use URL Inspection on the exact page that is missing. Check:
- Page fetch / crawl accessibility.
- Whether indexing is allowed.
- Last crawl.
- Referring sitemap.
- User-declared and Google-selected canonical.
- Live Test after a fix.

Then Request indexing for important individual pages.

For many new or changed pages, use the sitemap rather than submitting every URL manually.

### Source
- https://support.google.com/webmasters/answer/9012289

---

## SW-WEB-004 | canonical signals should agree on one HTTPS URL

STATUS: VERIFIED
APPLIES_TO: swindon.org.uk
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
If the same content is reachable through HTTP/HTTPS, www/non-www or alternate paths, choose the preferred URL and make signals agree:
- permanent redirect from unwanted duplicates where appropriate;
- rel=canonical on HTML pages;
- only preferred canonical URLs in the sitemap;
- consistent internal links.

Google treats redirects and rel=canonical as strong signals and sitemap inclusion as a weaker signal.

### Source
- https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls

---

## SW-WEB-005 | Cloudflare must not accidentally obstruct legitimate crawlers

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Cloudflare-proxied sites
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Cloudflare identifies Verified Bots including recognised search engine crawlers. Bot Fight Mode is available on Free plans, but its challenges cannot be bypassed with ordinary WAF Skip rules. If bot protection appears to interfere with crawling or API traffic, inspect Security Analytics and the precise product behaviour before adding more rules.

### Practical rule for swindon.org.uk
Keep legitimate search crawling possible while separately deciding how AI training, AI search and automated-agent traffic should be handled. Do not use a broad "block all bots" rule as an SEO fix.

### Sources
- https://developers.cloudflare.com/bots/concepts/bot/verified-bots/
- https://developers.cloudflare.com/bots/get-started/bot-fight-mode/

---

# DEBLOAT DECISION MATRIX

Item / action | Default Aletheia treatment | Why
--------------+----------------------------+-------------------------------------------------------
Unused third-party/OEM trialware | REVIEW THEN UNINSTALL | Supported, reversible by reinstall
Unneeded startup apps | DISABLE FIRST | Easy rollback; measurable startup effect
Temporary files | STORAGE SENSE / supported cleanup | Lower risk than generic cleaners
Downloads folder | USER DECIDES | Storage Sense does not touch it by default unless configured
OneDrive | CONDITIONAL | May own/sync user paths and Windows Backup workflow
Xbox/gaming apps | CONDITIONAL | Safe value depends on gaming/services used
Widgets / current shell extras | VERSION-CHECK | Packages and dependencies change between builds
Microsoft Store / App Installer | GENERALLY KEEP | Store/MSIX and WinGet workflows can depend on components
WebView2 runtime | GENERALLY KEEP | Many desktop apps embed it
Windows Update components | KEEP | Required for servicing
BITS | KEEP UNLESS SPECIFIC DIAGNOSIS | Used by Windows/app transfer workflows
Windows Installer | KEEP | Application install/repair dependency
Task Scheduler | KEEP | Windows and applications depend on tasks
WMI/CIM infrastructure | KEEP | Management/monitoring dependency
RPC | KEEP | Fundamental Windows dependency
Defender / Firewall | KEEP OR MANAGED REPLACEMENT | Security boundary
Random registry "speed pack" | REJECT BY DEFAULT | Version drift and hard-to-reverse side effects
Mass service-disable script | REJECT | Unknown dependencies and poor portability
Mass AppX removal for all users | REJECT BY DEFAULT | Can break provisioning/dependencies
Disabling updates | REJECT AS "DEBLOAT" | Converts performance tweak into security debt

# SOURCE-DRIFT / MYTH-CORRECTION REGISTER

## SD-001 | "PDC and BDC" as the current AD architecture
STATUS: REJECTED FOR MODERN ACTIVE DIRECTORY

Older Windows Server interview material may describe Primary Domain Controllers and Backup Domain Controllers as if this were the current architecture. That belongs to the Windows NT model. Modern AD is multi-master with specific FSMO roles.

## SD-002 | "WMIC is a standard modern Windows command"
STATUS: REJECTED FOR CURRENT WINDOWS 11

WMIC appears in many A-to-Z command lists, but Microsoft removed it from Windows 11 24H2 and later. Preserve it only as a legacy migration keyword.

## SD-003 | "PowerShell Remove-NetIPAddress equals DHCP release"
STATUS: REJECTED

Removing an IP configuration and releasing a DHCP lease are not the same operation. Use the command that matches the network model.

## SD-004 | "Every slow Windows PC needs service disabling"
STATUS: REJECTED

Startup apps, disk pressure, update state, failing storage, thermal throttling, memory pressure and browser workloads are more useful first measurements. Service surgery is not a universal performance cure.

## SD-005 | "System Restore backs up my documents"
STATUS: REJECTED

System Restore is for system state. Personal files require a separate backup strategy.

## SD-006 | "A successful ping proves the website works"
STATUS: REJECTED

PING demonstrates ICMP response, not DNS correctness, TLS validity, TCP 443 service health, HTTP behaviour or application status.

## SD-007 | "A sitemap makes Google index every page"
STATUS: REJECTED

A sitemap helps discovery and communicates preferred URLs. Google still decides whether to crawl and index a page.

## SD-008 | "Google verification needs .htaccess code"
STATUS: REJECTED FOR SEARCH CONSOLE DOMAIN PROPERTY

A Search Console Domain property is verified using DNS. .htaccess may still be useful for normal Apache redirects or canonical HTTPS behaviour, but it is not required for Domain-property ownership verification.

# SAFE DIAGNOSTIC PLAYBOOKS

## Slow Windows PC

1. Record Windows version with winver.
2. Check free storage space.
3. Task Manager: CPU, Memory, Disk and Startup apps.
4. Disable unnecessary high-impact startup apps.
5. Remove clearly unused ordinary applications.
6. Run supported Storage Sense cleanup.
7. Check Windows Update state and reboot if servicing is pending.
8. Check Event Viewer / Get-WinEvent if freezes or crashes occur.
9. Use power/battery reports for mobile power complaints.
10. Only then investigate services, drivers or registry settings tied to evidence.

## "Internet is broken"

1. ipconfig /all
2. Confirm adapter has expected address, gateway and DNS servers.
3. Resolve-DnsName target
4. Test-NetConnection target -Port 443
5. ping or tracert only as supporting evidence.
6. Browser test.
7. Check proxy/VPN/security software.
8. Flush DNS only when stale resolver state is plausible.
9. Release/renew only for DHCP problems.
10. Record before resetting network configuration.

## Windows corruption / strange system failures

1. Back up important files.
2. Install pending Windows updates and restart when sensible.
3. Run DISM RestoreHealth.
4. Run SFC /scannow.
5. Check disk/file system state if symptoms point there.
6. Check Event Viewer / Get-WinEvent.
7. Use System Restore if problem follows a known system change and a suitable restore point exists.
8. Escalate to supported recovery/reinstall paths rather than piling on registry fixes.

## Before a Windows rebuild

1. Ensure personal files exist in a separate verified backup.
2. Record BitLocker recovery key.
3. winget export -o apps.json
4. Save browser bookmarks/profile data as appropriate.
5. Export application-specific settings that matter.
6. Record licences and authentication/recovery methods.
7. Confirm installation/recovery media.
8. After rebuild, update Windows first, then restore applications and data deliberately.

# SWINDON.ORG.UK ACTION CHECKLIST - 2026-09-23

This is the practical end section requested alongside the Windows knowledge work.

1. Search Console
   - Add or verify the Domain property: swindon.org.uk
   - Verify ownership by DNS TXT record.
   - Do not add protocol or www to the Domain property name.

2. Sitemap
   - Confirm https://swindon.org.uk/sitemap.xml returns normally to an anonymous browser and Googlebot.
   - Submit that exact sitemap in Search Console.
   - Check the Sitemaps report for fetch or parse errors.
   - Keep only canonical URLs in the sitemap.

3. robots.txt
   - Confirm https://swindon.org.uk/robots.txt is publicly readable.
   - Include: Sitemap: https://swindon.org.uk/sitemap.xml
   - Do not accidentally disallow the sections intended for Google Search.
   - Decide AI-training/search bot policy separately from ordinary search indexing.

4. URL Inspection
   - Inspect https://swindon.org.uk/ and several representative /resources/ pages.
   - Use Test live URL.
   - Check Page fetch, Indexing allowed, Referring sitemap and Google-selected canonical.
   - After fixing any error, Request indexing for the key pages.

5. Canonical / redirects
   - Pick one public canonical family, normally HTTPS.
   - HTTP, www/non-www and old duplicate entry points should consistently converge on it where appropriate.
   - Match redirects, canonical tags, sitemap URLs and internal links.
   - Do not add Google-specific rewrite hacks unless an actual Search Console error proves they are needed.

6. Cloudflare
   - Review Security Analytics if crawlers are failing.
   - Be careful with Bot Fight Mode because Free-plan Bot Fight Mode cannot be bypassed using normal WAF Skip rules.
   - Do not deliberately block Verified Search Engine Crawlers if the site should appear in search.
   - AI Search, AI agent and AI training access can be managed as separate policy choices.

7. Affiliate architecture
   - Keep Awin / Bookshop and other commercial links on clearly disclosed resource pages.
   - Keep Aletheia Knowledge Markdown evidence-first and free of affiliate tracking parameters.
   - Knowledge cards may carry a plain resource backlink once the corresponding resource page is live.
   - Affiliate systems must never affect evidence ranking or card content.


# V0.2 COMMAND-ATLAS ADDITIONS

These cards were promoted after a second pass over the supplied A-to-Z command material. They concentrate on commands that remain explicitly documented for current Windows 10/11 and supported Windows Server releases.

## SW-LIFE-007 | Server 2012/R2 ESU ends in October 2026

STATUS: VERIFIED
APPLIES_TO: Windows Server 2012 and Windows Server 2012 R2 enrolled in Extended Security Updates
LIFECYCLE: ESU ENDING
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Normal extended support for Windows Server 2012 and 2012 R2 ended in 2023. Microsoft's third and final Extended Security Update year ends in October 2026. Microsoft's current release-health notice gives 13 October 2026 as the end of ESU protection.

### Practical consequence
A remaining 2012/R2 server should be treated as an urgent migration item rather than a stable long-term platform. Record application dependencies before changing it, but do not mistake ESU for a new normal support lifecycle.

### Sources
- https://learn.microsoft.com/en-us/lifecycle/products/windows-server-2012-r2
- https://learn.microsoft.com/en-us/windows/release-health/status-windows-8.1-and-windows-server-2012-r2

---

## SW-LIFE-008 | Server 2016 extended support ends in January 2027

STATUS: VERIFIED
APPLIES_TO: Windows Server 2016
LIFECYCLE: SUPPORTED-LEGACY
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows Server 2016 is in extended support. Microsoft's English lifecycle page lists 13 January 2027 as its extended-support end date.

### Practical consequence
Machines still on Server 2016 are close enough to end of support that application compatibility, replacement hardware, backup/restore testing and upgrade paths should already be known.

### Source
- https://learn.microsoft.com/en-us/lifecycle/products/windows-server-2016

---

## SW-LIFE-009 | Server 2019 extended support ends in January 2029

STATUS: VERIFIED
APPLIES_TO: Windows Server 2019
LIFECYCLE: SUPPORTED-LEGACY
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
Windows Server 2019 left mainstream support in January 2024 and remains in extended support through 10 January 2029.

### Why useful
"Server 2019" still sounds fairly modern in mixed estates. Lifecycle data gives a better planning signal than the product name.

### Source
- https://learn.microsoft.com/en-us/lifecycle/products/windows-server-2019

---

## SW-CMD-010 | systeminfo captures OS and hardware configuration

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
SYSTEMINFO displays detailed information about Windows and the computer, including OS configuration, hardware properties, memory and network information.

Examples:

    systeminfo
    systeminfo /fo list
    systeminfo /fo csv

### Useful pattern
Capture a baseline before troubleshooting or changing a machine:

    systeminfo > "%USERPROFILE%\Desktop\systeminfo.txt"

### Privacy note
Inventory output can include computer names, network information and other environment details. Remove sensitive fields before posting it publicly.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/systeminfo

---

## SW-CMD-011 | whoami shows the current security token

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
WHOAMI can show the current user, groups, security identifiers, claims and privileges. It is one of the quickest ways to answer "who am I actually running as?"

Examples:

    whoami
    whoami /groups
    whoami /priv
    whoami /all

### Why useful
Many "access denied" problems are really context problems: wrong user, missing group membership, unelevated token or a privilege that is present but disabled.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/whoami

---

## SW-CMD-012 | driverquery inventories installed drivers

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
DRIVERQUERY lists installed device drivers and their properties. It can produce table, list or CSV output and can show verbose or signed-driver information.

Examples:

    driverquery
    driverquery /v
    driverquery /si
    driverquery /fo csv

### Why useful
It creates a quick before/after record when a driver update is suspected of causing a problem, without changing any driver.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/driverquery

---

## SW-CMD-013 | clip sends command output to the clipboard

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
CLIP sends text or another command's output to the Windows clipboard.

Examples:

    whoami /all | clip
    ipconfig /all | clip
    dir | clip

### Privacy note
The clipboard is convenient, not private storage. Before piping diagnostics to CLIP, consider whether the output contains usernames, machine names, IP addresses, paths or other information you do not intend to paste elsewhere.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/clip

---

## SW-CMD-014 | cmdkey inventories and manages stored credentials

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
CMDKEY can create, list and delete stored credentials.

Safe inventory:

    cmdkey /list

### Security rule
Avoid putting a plaintext password directly in a command line or script. If a command can prompt for a password, prefer the prompt. Process history, scripts, terminal transcripts and screenshots are bad places to store secrets.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/cmdkey

---

## SW-FS-001 | icacls reads and changes NTFS permissions

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW FOR INSPECTION; HIGH FOR RECURSIVE CHANGES
LAST_CHECKED: 2026-09-23

### Summary
ICACLS displays or modifies discretionary access-control lists on files and folders. Microsoft identifies it as the replacement for deprecated CACLS.

Safe inspection:

    icacls "C:\Path"

### Before changing
ICACLS can save ACLs to a file and restore them later. For important trees, preserve the current permissions before attempting grants, resets or ownership changes.

### Danger
Recursive /T operations can spread a mistaken ACL through a large tree. Never test a permissions recipe against Windows, Program Files or an unfamiliar shared-data root.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/icacls

---

## SW-FS-002 | takeown recovers ownership but changes security state

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: HIGH
ADMIN_REQUIRED: YES
LAST_CHECKED: 2026-09-23

### Summary
TAKEOWN lets an administrator recover access to a file by making the administrator or Administrators group the owner.

### Aletheia rule
"Access denied" does not automatically mean "take ownership." First identify the intended owner and ACL. Ownership changes can defeat carefully designed application, service or operating-system permissions.

### Recursion warning
The /R option operates recursively. Do not aim it casually at Windows system folders, application trees or enterprise shares.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/takeown

---

## SW-SVC-001 | sc query inspects service and driver state

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW FOR QUERY
LAST_CHECKED: 2026-09-23

### Summary
SC.EXE QUERY displays information about services and drivers, including state and status fields.

Examples:

    sc.exe query
    sc.exe query wuauserv
    sc.exe query state= all

### Syntax trap
SC parameters such as state= require a space between the equals sign and the value.

### Safety distinction
SC QUERY is observation. Other SC operations can reconfigure or delete services. Microsoft explicitly warns against using SC DELETE to remove built-in operating-system services.

### Sources
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/sc-query
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/sc-delete

---

## SW-EVT-001 | wevtutil queries and exports event logs

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW FOR QUERY/EXPORT; HIGH FOR CLEAR/CONFIGURE
LAST_CHECKED: 2026-09-23

### Summary
WEVTUTIL can enumerate logs and publishers, query events, inspect log configuration, and export or archive event logs.

Examples:

    wevtutil el
    wevtutil qe System /c:20 /rd:true /f:text
    wevtutil epl System "%USERPROFILE%\Desktop\System.evtx"

### Evidence rule
Export before clearing. Clearing an event log can destroy precisely the diagnostic or audit evidence needed to explain a failure.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/wevtutil

---

## SW-CFG-001 | reg query reads registry state without changing it

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
REG QUERY reads registry keys and values without modifying them. It can search recursively, filter by value/type and explicitly choose the 32-bit or 64-bit registry view.

Examples:

    reg query HKCU\Software
    reg query "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion" /v ProductName

### Why useful
When investigating a suggested registry tweak, query the existing value first. Record what is actually present before applying someone else's expected value.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/reg-query

---

## SW-SYS-001 | shutdown schedules restart/shutdown and /a can abort

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM; HIGH WITH /F
LAST_CHECKED: 2026-09-23

### Summary
SHUTDOWN can shut down, restart, hibernate or schedule power actions locally or remotely. A pending timed shutdown can be aborted with:

    shutdown /a

### Safety note
The /F switch forces applications to close and can lose unsaved work. A timed restart without /F is generally preferable when people may have open work.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/shutdown

---

## SW-ID-001 | net user lists or administers user accounts

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11, Server 2016/2019/2022/2025
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW FOR LISTING; HIGH FOR ACCOUNT CHANGES
LAST_CHECKED: 2026-09-23

### Summary
NET USER can list local user accounts, show account details, and with appropriate permissions add, modify or delete local or domain user accounts.

Safe inspection:

    net user
    net user username

### Security rule
Do not put passwords directly into reusable command text. For account administration, prefer password prompts or managed identity tools rather than storing credentials in scripts.

### Source
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/net-user

---


# WINDOWS 10 ESU, DRIVER CONTROL AND LEGACY-PC STABILITY

These cards support the companion **Aletheia Windows Debloat** app. The design goal is not to make an old PC "modern"; it is to keep a working machine useful, predictable and recoverable with the least unnecessary background load.

The evidence supports a more precise model than "Windows 10 must be allowed to update whenever Microsoft wants." Microsoft product terms authorise automatic updates **unless the device has been configured to prevent automatic updates using supported methods**. Consumer ESU still depends on Windows Update for monthly security servicing, so disabling the update machinery permanently trades stability risk for security risk rather than eliminating risk.

## SW-UPD-001 | ESU does not remove all supported update control

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10 22H2 enrolled or enrolling in ESU
LIFECYCLE: ESU
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Microsoft's current Windows product terms authorise automatic downloading and installation of Windows 10/11 updates unless the device is configured to prevent automatic updates using supported methods. ESU itself provides critical and important security updates; it does not turn every update or driver into a mandatory feature upgrade.

### ESU prerequisite
Consumer ESU enrollment requires an eligible Windows 10 22H2 device and current prerequisite servicing. Microsoft also distributes ESU preparation packages through Windows Update.

### Aletheia check
Do not state that accepting ESU means the user legally or technically loses all update control. The defensible statement is narrower: ESU relies on the Windows servicing system, and the PC must periodically receive applicable ESU security updates if the user wants ESU protection.

### Sources
- https://www.microsoft.com/licensing/terms/productoffering/WindowsDesktopOperatingSystem/MCA
- https://www.microsoft.com/en-US/windows/extended-security-updates
- https://support.microsoft.com/en-us/servicing/os/windows-10/2026/09/kb5126256-windows-10-21h2-22h2-standalone-cbs

---

## SW-UPD-002 | Controlled Update mode is safer than killing Windows Update

STATUS: METHOD
APPLIES_TO: Windows 10, especially legacy hardware and ESU systems
LIFECYCLE: CURRENT / ESU
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
For an old but still useful Windows 10 PC, the preferred Aletheia strategy is **Controlled Update mode**, not permanently breaking Windows Update services.

### Controlled Update mode
1. Identify Windows edition and build.
2. Back up user data and current drivers.
3. Exclude driver delivery from quality updates where the edition supports that policy.
4. On editions with Group Policy, use **Configure Automatic Updates = 2: Notify for download and auto install** when the user wants manual timing.
5. On Windows 10 Home, use the supported Pause Updates control when temporary deferral is needed.
6. Install ESU security updates deliberately, preferably after checking known issues and having a rollback path.
7. Restart at a chosen time and test sound, display, networking, storage and peripherals.
8. If an update causes a regression, use the documented rollback/recovery route.

### Why not simply disable the Windows Update service?
Service-disable tricks can be undone by servicing components, may interfere with ESU, Store/MSIX or other Windows components, and leave the machine unpatched without clearly telling the user what security debt was created.

### Sources
- https://learn.microsoft.com/en-us/windows/deployment/update/waas-wu-settings
- https://support.microsoft.com/en-us/windows/deployment/updates-lifecycle/pause-updates-in-windows

---

## SW-UPD-003 | Windows Update drivers can be excluded on supported editions

STATUS: VERIFIED
APPLIES_TO: Windows 10 Pro, Enterprise, Education and other editions supporting the documented policy
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Microsoft provides a supported policy named **Do not include drivers with Windows Updates**. When enabled, Windows quality updates do not include updates classified as drivers.

### Group Policy path
Computer Configuration > Administrative Templates > Windows Components > Windows Update > Manage updates offered from Windows Update > Do not include drivers with Windows Updates

Microsoft maps the policy to:

    HKLM\Software\Policies\Microsoft\Windows\WindowsUpdate
    ExcludeWUDriversInQualityUpdate = 1

### Why useful on older PCs
A stable vendor driver can be more valuable than a newer generic driver. Excluding driver-classified Windows Update packages lets security servicing continue while driver changes are handled separately.

### Caveat
The policy is not a guarantee that every hardware-related component will remain untouched forever; firmware, servicing components and software packages can be delivered through different mechanisms. Verify the actual update classification.

### Sources
- https://learn.microsoft.com/windows/client-management/mdm/policy-csp-update
- https://learn.microsoft.com/en-us/windows/deployment/update/waas-wu-settings

---

## SW-UPD-004 | roll back a driver after a bad Windows Update

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Microsoft explicitly documents driver rollback when a device stops working correctly after Windows Update.

### GUI route
Device Manager > device > Properties > Driver > Roll Back Driver

The rollback option is available only when Windows still has a previous driver version to restore.

### Aletheia rule
If a display, sound, network or other device fails immediately after an update, inspect the driver change before escalating to Reset this PC.

### Sources
- https://support.microsoft.com/en-us/windows/update-drivers-through-device-manager-in-windows-ec62f46c-ff14-c91d-eead-d7126dc1f7b6
- https://support.microsoft.com/en-gb/windows/hardware/audio/fix-audio-stops-working-after-a-windows-update-in-windows

---

## SW-DRV-001 | export existing third-party drivers before changing them

STATUS: VERIFIED
APPLIES_TO: Windows 10 version 1607+, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW FOR EXPORT
ADMIN_REQUIRED: RECOMMENDED
LAST_CHECKED: 2026-09-23

### Summary
PnPUtil can enumerate and export third-party driver packages from the Windows driver store before an update or rebuild.

Examples:

    pnputil /enum-drivers
    pnputil /export-driver * C:\DriverBackup

### Why useful
On an older PC, the currently working driver may be hard to find years later. A local driver export gives the user a recovery asset before experimenting.

### Important limitation
Exported driver packages do not constitute a complete machine backup and do not guarantee that every OEM utility, firmware package or device-specific application has been preserved.

### Sources
- https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/pnputil-command-syntax
- https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/pnputil-examples

---

## SW-DRV-002 | AI may find driver candidates but must not choose blindly

STATUS: METHOD
APPLIES_TO: Aletheia Windows Debloat driver-assistance workflow
LIFECYCLE: CURRENT
EVIDENCE: CONTEXT
CONFIDENCE: HIGH
RISK: HIGH IF AUTOMATED WITHOUT VERIFICATION
LAST_CHECKED: 2026-09-23

### Summary
AI can help search for a driver, but it should not decide that a vaguely similar download is correct and silently install it.

### Safe driver-discovery workflow
1. Enumerate the exact device and hardware IDs.
2. Record the currently installed provider, version and date.
3. Export the existing third-party driver package first.
4. Prefer the PC/OEM support page for laptops and integrated hardware.
5. Otherwise prefer the actual component manufacturer.
6. Confirm the candidate explicitly supports the device hardware ID and Windows version/architecture.
7. Prefer signed packages and HTTPS vendor sources.
8. Present the candidate to the user with source, version, date and rollback path.
9. Install only after explicit user choice.
10. Test the device before moving to the next driver.

Useful enumeration on supported Windows:

    pnputil /enum-devices /deviceids
    pnputil /enum-devices /drivers
    pnputil /enum-drivers

### Aletheia rule
AI is a **research assistant**, not a driver authority. A fabricated or mismatched driver URL can turn a performance tool into a very efficient bricklayer.

### Sources
- https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/pnputil-command-syntax
- https://support.microsoft.com/en-us/windows/hardware/drivers/automatically-get-recommended-and-updated-hardware-drivers

---

## SW-UPD-005 | use an update-recovery ladder before Reset this PC

STATUS: METHOD
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: HIGH
LAST_CHECKED: 2026-09-23

### Summary
If a Windows update makes a previously working PC fail to boot or behave correctly, do not jump immediately to Reset this PC.

### Recovery ladder
Depending on symptoms and what Windows Recovery Environment offers:

1. Record the update/error if possible.
2. Try Startup Repair for a boot-specific failure.
3. Roll back a recently changed driver where applicable.
4. Uninstall the latest update from Windows Recovery Environment if the failure follows an update.
5. Use System Restore when a suitable restore point exists.
6. Use DISM/SFC when system-file corruption is plausible and Windows can run.
7. Back up important data if not already protected.
8. Use Reset this PC only when less disruptive repair routes are unsuitable or have failed.
9. Use installation/recovery media or a clean install when Reset is unavailable or the system state is too damaged.

### Correction
Reset this PC does not always require separate installation media. Current Windows can offer local reinstall and, on supported configurations, cloud download. However, reset can remove installed applications and settings, so it remains a major recovery action rather than a routine post-update fix.

### Sources
- https://support.microsoft.com/en-us/windows/experience/backup-recovery/recovery-options-in-windows
- https://support.microsoft.com/en-us/windows/experience/backup-recovery/backup-restore-and-recovery-in-windows

---

# COMPANION APP AND RESOURCE ARCHITECTURE

## Aletheia Windows Debloat

**Aletheia Secret Windows** is the evidence library. **Aletheia Windows Debloat** is the companion application that may use selected cards to inspect and configure a PC.

The app should:
- detect Windows edition/build before offering a change;
- explain what each change does;
- show memory/background-process impact where measurable;
- distinguish recommended, optional, advanced and legacy-machine actions;
- create or confirm recovery assets before high-risk changes;
- support undo wherever Windows supports it;
- never silently install an AI-selected driver;
- treat update control as a profile, not as one irreversible "OFF" switch.

Suggested update profiles:

### ESU CONTROLLED
Keep Windows 10 ESU security updates available, exclude Windows Update drivers where supported, notify before downloading on supported editions, and let the user choose servicing time.

### QUIET LEGACY
Reduce startup/background software, scheduled updaters and non-essential applications while retaining operating-system security servicing.

### FROZEN / ISOLATED
For a machine deliberately kept in a fixed state for legacy software or hardware. This profile should carry a prominent warning that disabling security servicing makes an internet-connected PC progressively less safe. It is best suited to isolated or tightly restricted machines.

## Proposed physical files

The clean architecture is **four files across the two projects/sites**:

1. **Knowledge**
   aletheia-knowledge/knowledge/aletheia-secret-windows.md
   Canonical checked knowledge. This file exists now.

2. **App**
   aletheia-app/aletheia-windows-debloat/aletheia-windows-debloat.htm
   The executable browser/PowerShell-assistance interface.

3. **Aletheia resource page**
   aletheia-app/aletheia-windows-debloat/aletheia-windows-debloat-rsc.htm
   App-facing resources, documentation, driver/vendor guidance and disclosed affiliate links where appropriate.

4. **Swindon.org.uk resource page**
   swindon.org.uk/resources/aletheia-windows-debloat-rsc.htm
   Search/AEO-oriented public resource page for discovery, books/tools/resources and clearly disclosed affiliate links.

### Canonical rule
Do not make two competing copies of the knowledge Markdown. There should be **one canonical knowledge file**. The two resource HTML pages can have different presentation and commercial context, while both point back to the same Aletheia knowledge/app family.

### Backlinks
When the app and resource pages are live, add plain links near the end of this knowledge file:

    Companion app: <Aletheia Windows Debloat public URL>
    App resources: <Aletheia resource URL>
    Swindon resources: https://swindon.org.uk/resources/aletheia-windows-debloat-rsc.htm

Until those URLs exist, keep them marked PLANNED rather than publishing dead links.



## SW-REG-001 | Windows stopped automatic RegBack in Windows 10 1803

STATUS: VERIFIED
APPLIES_TO: Windows 10 version 1803 and later
LIFECYCLE: CURRENT BEHAVIOUR / LEGACY BACKUP CAN BE RE-ENABLED
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Microsoft stopped automatically backing up the system registry into Windows\System32\config\RegBack starting with Windows 10 version 1803. The hive files can still appear in that folder but be 0 KB.

### Why it changed
Microsoft states that this was a deliberate change intended to reduce the overall disk footprint of Windows.

### Re-enable the legacy periodic backup
Microsoft documents this registry value:

    HKLM\System\CurrentControlSet\Control\Session Manager\Configuration Manager
    EnablePeriodicBackup = 1  (REG_DWORD)

After restart, Windows creates registry backups in RegBack and uses the RegIdleBackup scheduled task for later backups.

### Aletheia rule
The Debloat app may offer this as an explicit option named **RE-ENABLE WINDOWS REGISTRY BACKUP**. It should first read and save the existing Configuration Manager key and explain that Microsoft recommends System Restore as the normal recovery route.

### Source
- https://learn.microsoft.com/en-us/troubleshoot/windows-client/installing-updates-features-roles/system-registry-no-backed-up-regback-folder

---

## SW-REG-002 | save touched registry keys before applying a profile

STATUS: METHOD
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW FOR SAVE; HIGH FOR RESTORE/APPLY
LAST_CHECKED: 2026-09-23

### Summary
Every Aletheia registry profile should create a timestamped backup of the registry keys it is about to change before making the first change.

Windows provides REG SAVE to save a registry subkey to a hive file and REG RESTORE to write a saved hive back.

Example pattern:

    mkdir D:\Aletheia-Backup\2026-09-23-0126
    reg save "HKLM\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate" "D:\Aletheia-Backup\2026-09-23-0126\WindowsUpdate.hiv"

### Design rule
Do not dump backups into a Windows-managed temporary folder. Prefer a clearly named Aletheia backup folder, ideally on a second physical disk or external drive when available.

### Restore warning
Restoring system-critical registry areas is an advanced recovery action. A saved hive is valuable evidence and rollback material, but it is not a substitute for a full system backup or recovery media.

### Sources
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/reg-save
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/reg-restore

---

## SW-BACK-001 | build a recovery pack before debloat or update changes

STATUS: METHOD
APPLIES_TO: Aletheia Windows Debloat
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW TO MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Before a high-risk debloat, update-policy or driver operation, create an **Aletheia Recovery Pack**.

### Suggested pack
1. Machine inventory: Windows edition/build and hardware IDs.
2. Export third-party drivers with PnPUtil.
3. Save the registry keys the app will touch.
4. Optionally re-enable Windows RegBack periodic backups.
5. Confirm a System Restore point or explain when System Restore is unavailable.
6. Offer creation of Windows recovery media.
7. If a second disk is available and the user wants stronger recovery, offer an advanced full/critical-volume backup using a supported imaging method.
8. Write a plain-text restore manifest explaining what was saved and where.

### Built-in advanced option
WBADMIN remains documented on Windows 10 and Windows 11 and can create VSS-based backups. The -allCritical option includes volumes required for operating-system state and is intended for bare-metal recovery scenarios.

This should be an **advanced** option because destination selection, available space and recovery testing matter.

### Why useful
If the SSD containing Windows fails while personal data lives safely on another disk, a driver archive plus recovery media and a proper system backup can turn a ruined afternoon into a fairly dull reinstall. Dull is excellent in disaster recovery.

### Sources
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/wbadmin-start-backup
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/wbadmin
- https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/bare-metal-recovery

---


## SW-UPD-006 | ESU changes the security window, not every update-control rule

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10 22H2 Consumer ESU
LIFECYCLE: ESU
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Windows 10 Consumer ESU extends the period in which an eligible Windows 10 22H2 PC can receive critical and important security updates. It does not restore normal Windows 10 feature development.

Under default Windows Update settings, applicable updates can still download and install automatically. On supported editions, Microsoft still documents update policies including Configure Automatic Updates and Do not include drivers with Windows Updates.

### Important distinction
There is not good evidence for the stronger claim that accepting ESU makes it technically impossible to control Windows Update or forces every update regardless of supported policy. What is true is that Windows servicing components can repair or reverse unsupported service-disabling tricks, and Windows Home offers fewer policy controls than Pro/Enterprise.

### Legacy-PC concern
On an older PC, any update can expose a latent driver or compatibility problem. This is why Aletheia Windows Debloat should combine:
- driver backup;
- driver-update exclusion where supported;
- a chosen update window;
- restore/rollback preparation;
- post-update checks for display, audio, network, storage and peripherals.

### Sources
- https://www.microsoft.com/en-US/windows/extended-security-updates
- https://learn.microsoft.com/en-us/windows/deployment/update/waas-wu-settings
- https://learn.microsoft.com/en-us/windows/deployment/update/waas-configure-wufb

---

## SW-REG-003 | downloadable RegBack enable and undo files

STATUS: VERIFIED
APPLIES_TO: Windows 10 version 1803 and later
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Microsoft documents EnablePeriodicBackup=1 to restore the legacy periodic RegBack behaviour. Secret Windows provides a transparent .reg file and a matching undo file.

### Downloads
Enable:
https://karstenevans.github.io/aletheia-knowledge/resources/downloads/enable-regback-periodic-backup.reg

Undo:
https://karstenevans.github.io/aletheia-knowledge/resources/downloads/undo-enable-regback-periodic-backup.reg

### Registry setting

    [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Configuration Manager]
    "EnablePeriodicBackup"=dword:00000001

After enabling, restart Windows. Microsoft says Windows then backs up the registry to RegBack and creates the RegIdleBackup scheduled task for later backups.

### Safety
Inspect registry files before importing them. Aletheia should also save the specific registry keys it is about to change before applying any wider tweak profile.

### Source
- https://learn.microsoft.com/en-us/troubleshoot/windows-client/installing-updates-features-roles/system-registry-no-backed-up-regback-folder

---

## SW-OPT-007 | replacing an HDD with an SSD can transform an old PC

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: PCs currently booting Windows from a mechanical HDD
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Microsoft describes SSDs as faster than HDDs, and its Windows performance guidance identifies storage speed as a major factor in responsiveness. On an otherwise serviceable older PC that still boots from a mechanical HDD, moving Windows and applications to an SSD is often one of the highest-impact hardware upgrades.

### Capacity guide
For a basic legacy Windows PC:
- 240/250/256 GB can work for Windows and light applications.
- 480/500/512 GB is a comfortable default when budget permits.
- 1 TB is useful when the machine actually needs that capacity.

Do not confuse capacity with interface. A 500 GB SATA SSD and a 500 GB NVMe SSD may fit completely different machines.

### Before buying
Identify the exact model and confirm whether it accepts:
- 2.5-inch SATA;
- mSATA;
- M.2 SATA;
- M.2 NVMe;
- another documented interface.

### Sources
- https://support.microsoft.com/en-US/Windows/Experience/Compatibility/all-about-ssd-hdd-and-storage-types
- https://support.microsoft.com/en-us/windows/experience/performance-optimization/tips-to-improve-pc-performance-in-windows

---

## SW-OPT-008 | 8 GB RAM is a strong practical target for light Windows use

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows PCs with upgradeable memory
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
Microsoft says 4 GB can be enough for basic web, documents and video, while recommending 8 GB for longer-term everyday use; 16 GB or more may suit heavier work.

### Legacy-PC interpretation
A 4 GB Windows PC can still be useful, especially with an SSD, but browsers and modern applications can push it into paging quickly. If the machine supports an inexpensive upgrade to 8 GB, that can materially improve multitasking. Moving to 16 GB can help heavier workloads, but only if the chipset, firmware, slots and memory type support it.

### 32-bit warning
A 32-bit Windows 10 installation is limited to about 4 GB of physical address space by the OS family. Do not buy extra RAM before confirming whether the machine and installed Windows can use it.

### Sources
- https://support.microsoft.com/en-us/windows/experience/compatibility/all-about-computer-memory
- https://learn.microsoft.com/en-us/windows/win32/memory/memory-limits-for-windows-releases

---

## SW-OPT-009 | research the exact machine before buying RAM or SSD

STATUS: METHOD
APPLIES_TO: legacy PC upgrade planning
LIFECYCLE: CURRENT
EVIDENCE: GOOD
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### Summary
The model number matters more than the marketing family name. Two laptops sold under almost the same name can have different soldered RAM, slot counts, storage interfaces or maximum memory.

### Copy/paste research prompt

    Find the official specification and service/maintenance manual for this exact computer:
    MAKE/MODEL: [PASTE THE FULL MODEL OR PRODUCT NUMBER HERE]

    Tell me:
    1. The exact CPU and chipset options for this model.
    2. How much RAM it was supplied with.
    3. Whether any RAM is soldered/onboard.
    4. How many RAM slots exist, how many are currently likely to be occupied, and the maximum supported RAM.
    5. Required RAM type, DDR generation, SO-DIMM/DIMM form, speed and voltage.
    6. Whether mixed capacities are supported and whether matched pairs are preferred.
    7. Every supported internal storage interface: 2.5-inch SATA, mSATA, M.2 SATA or M.2 NVMe, including M.2 length/key if relevant.
    8. Whether the optical drive bay can accept a SATA HDD/SSD caddy and its physical height if documented.
    9. BIOS/UEFI or boot limitations that affect an SSD upgrade.
    10. Give links to the official manufacturer manual/specification first.
    11. Then cross-check the model with Crucial and Kingston compatibility tools.
    Do not guess from a similar model. Mark anything not confirmed as UNKNOWN.

### Useful compatibility tools
- Crucial System Scanner / Upgrade Selector.
- Kingston PC Scanner / model search.

### Sources
- https://www.crucial.com/store/systemscanner
- https://www.kingston.com/en/solutions/pc-performance/pc-scanner

---

## SW-OPT-010 | an optical-bay caddy can reuse the old HDD

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: laptops/desktops with a compatible removable optical drive bay
LIFECYCLE: LEGACY HARDWARE
EVIDENCE: GOOD
CONFIDENCE: MEDIUM-HIGH
RISK: MEDIUM
LAST_CHECKED: 2026-09-23

### Summary
A common legacy-laptop upgrade is:
- SSD in the primary drive bay for Windows and applications;
- the old healthy HDD in a compatible optical-bay SATA caddy for bulk data.

### Check before buying
Do not buy a caddy from the laptop's screen size alone. Confirm:
- optical bay exists and is removable;
- interface is SATA rather than an older PATA/IDE design;
- caddy height, commonly 9.5 mm or 12.7 mm on older designs;
- connector position and bezel fit;
- BIOS/UEFI behaviour.

### Safety
The old HDD is not a backup merely because it moved into a second bay. Keep another copy of irreplaceable data.

### Source
- https://www.ifixit.com/Wiki/Optical_Bay_to_Hard_Drive_Enclosures

---


## SW-OPT-011 | Task Scheduler orchestrates maintenance; it does not optimise by itself

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW FOR INSPECTION; MEDIUM FOR CREATING TASKS
LAST_CHECKED: 2026-09-23

### The interesting fact
Windows already includes Task Scheduler, which can run a program when a time, system event or other configured trigger occurs. It is not a standalone speed-boosting algorithm: its value is in coordinating existing, documented tools without buying an additional always-running optimiser.

### Aletheia use
For an app-based debloat assistant, make task inspection read-only by default. If creating an optional task, disclose the exact executable and arguments, run account, power/idle conditions, output log, failure handling and how to undo the task. Use a supported GUI feature (such as Storage Sense) when simpler. Cross-reference SW-CMD-009, SW-OPT-001 and SW-OPT-002.

### Check on the article
The XDA headline's claim that Task Scheduler outperforms *every* paid optimiser is not established by comparative benchmarks. The verified fact is that Windows supplies a free, extensible scheduler for maintenance.

### Sources
- https://learn.microsoft.com/en-us/windows/win32/taskschd/about-the-task-scheduler
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/schtasks
- https://www.xda-developers.com/windows-pc-has-built-in-optimization-tool-hidden-plain-sight-beats-every-paid-alternative/

---

## SW-OPT-012 | Windows can pause maintenance when you return to the PC

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11; power/sleep behaviour depends on machine and policy
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW
LAST_CHECKED: 2026-09-23

### The interesting fact
Windows Automatic Maintenance uses Task Scheduler to group background housekeeping. Ordinary maintenance tasks can start opportunistically while the PC is idle and plugged into mains power, and Windows can suspend them when someone returns to work. Critical tasks may be allowed to finish instead.

### Unexpected consequence
A laptop used constantly on battery power may not spend enough time both idle and plugged in, so maintenance tasks may be delayed. A maintenance time on the clock does not guarantee execution on a sleeping laptop, either: sleep mode, firmware and wake policy matter.

### Safe inspection
Open Control Panel > System and Security > Security and Maintenance > Automatic Maintenance where available. Inspect the settings and state before changing anything. Do not disable Automatic Maintenance globally to solve an unexplained performance problem; identify the particular process or task first.

### Sources
- https://learn.microsoft.com/en-us/windows/win32/taskschd/task-maintenence
- https://github.com/MicrosoftDocs/win32/blob/docs/desktop-src/w8cookbook/automatic-maintenance.md

---

## SW-OPT-013 | Disk Cleanup can save named cleanup presets

STATUS: VERIFIED
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: MEDIUM: SELECTED CATEGORIES MAY DELETE WANTED DATA
LAST_CHECKED: 2026-09-23

### The interesting fact
The older built-in Disk Cleanup tool can *remember* your chosen cleanup categories. Run cleanmgr /sageset:1 once to pick categories; later cleanmgr /sagerun:1 reuses those choices. The numerical label allows separate presets, and /sagerun enumerates the computer's drives rather than applying the profile exclusively to C:.

### Example
    cleanmgr /sageset:1
    cleanmgr /sagerun:1

The article suggests scheduling the latter using Task Scheduler. Use the leading slash exactly as shown above; a bare sagerun:1 argument is not the documented syntax.

### Aletheia safety check
Show the categories before scheduling; avoid surprise removal of Recycle Bin contents or other wanted material. Test interactively before automation and keep the schedule infrequent. Storage Sense remains the simpler built-in option for routine temporary-file cleanup (SW-OPT-002). Clearing caches or deleting files is not evidence of an automatic speed increase.

### Sources
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/cleanmgr
- https://learn.microsoft.com/en-us/troubleshoot/windows-server/backup-and-storage/automating-disk-cleanup-tool
- https://support.microsoft.com/en-us/windows/experience/storage-filemanagement/manage-drive-space-with-storage-sense

---

## SW-OPT-014 | A hidden startup workload may be a scheduled task

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Windows 10, Windows 11
LIFECYCLE: CURRENT
EVIDENCE: STRONG
CONFIDENCE: HIGH
RISK: LOW FOR AUDIT; MEDIUM OR HIGH FOR DISABLING
LAST_CHECKED: 2026-09-23

### The interesting fact
Installed programs can register Scheduled Tasks to launch update checks, background components or other housekeeping at a specific time or trigger. A PC can therefore run program-created work even when that program is absent from the ordinary Startup Apps list.

### Safe read-only inspection
    schtasks /query /fo LIST /v

Or inspect Task Scheduler Library. Record the task's publisher, file path, action, trigger, run account, last result and purpose. Cross-reference SW-CMD-009. If a third-party task is confirmed unnecessary, prefer changing the parent application's settings or uninstalling that app. Export the task definition before any manual disable.

### Aletheia safety check
Do not treat every scheduled task as bloat. Never mass-disable Microsoft, driver, antivirus, backup, servicing or updater tasks; some third-party tasks carry essential security updates. A visible task is an investigation lead, not proof that it is harming performance.

### Sources
- https://learn.microsoft.com/en-us/windows/win32/taskschd/about-the-task-scheduler
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/schtasks-query
- https://learn.microsoft.com/en-us/powershell/module/scheduledtasks/?view=windowsserver2025-ps

---

## SW-OPT-015 | A browser cache is useful; routine purging can backfire

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: Chromium-family browsers; use each browser's supported controls
LIFECYCLE: CURRENT
EVIDENCE: STRONG FOR CACHE PURPOSE; CONTEXT FOR PERFORMANCE EFFECT
CONFIDENCE: HIGH
RISK: MEDIUM FOR UNSUPERVISED PROFILE-FOLDER DELETION
LAST_CHECKED: 2026-09-23

### The interesting fact
Browsers save images, text and other page resources specifically to help previously visited pages open faster. Clearing this cache may recover some storage or resolve stale/corrupt page resources, but doing it on a routine timer forces the browser to fetch that material again.

### Aletheia safety check
Do not adopt the article's proposed generic scheduled PowerShell Remove-Item command against a browser profile's Cache_Data directory. Browser profile locations, multiple profiles and active file use vary; filesystem deletion is more error-prone than the browser's own clearing UI. Prefer targeted clearing when troubleshooting or short of space. Never silently wipe cookies, history, saved passwords or site data.

### Source
- https://support.google.com/chrome/answer/2392709?hl=en

---

## XDA article check | 19 September 2026

The article is useful for the five card ideas above, but it is not an endorsement of one-click optimisation. These additional recommendations already overlap existing cards or need qualification:

- WinGet upgrades can be scheduled, but prefer manual preview with winget upgrade before winget upgrade --all. The article's --include-unknown broadens the upgrade set to packages whose installed version cannot be determined; do not silently enable it. Avoid hard-coding a versioned WindowsApps path to winget.exe in a portable guide. Cross-reference SW-PKG-002.
- SFC and CHKDSK are legitimate repair/diagnostic tools, not demonstrated periodic speed boosters. Microsoft recommends DISM before SFC for suspected protected-file corruption; CHKDSK without repair flags reports status but does not fix errors. Cross-reference SW-REP-001, SW-REP-002 and SW-REP-003.
- Claims of measurable improvement, especially against every paid product, need comparable baseline and post-change measurements. Neither extra scheduled tasks nor regularly deleting useful caches necessarily makes a PC faster.

Primary sources:
- https://learn.microsoft.com/en-us/windows/package-manager/winget/upgrade
- https://support.microsoft.com/en-us/windows/experience/backup-recovery/use-the-system-file-checker-tool-to-repair-missing-or-corrupted-system-files
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/chkdsk

---


# AI & CHATGPT FREE | Practical use and reusable prompts

These cards cover using AI **on** Windows, Android and iOS, not Windows system functions. Platform features are time-sensitive, and the usage advice is distinguished from documented product behaviour.

## SW-AI-001 | Free ChatGPT is more than a text-only chatbot

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: STRONG
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: LOW
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
ChatGPT Free includes everyday text chat, web search, file and image uploads, some data analysis, image generation and limited Voice. Separate feature limits apply, so availability and capacity vary.

### Why useful
For a current question, request web search and dated sources. Upload a relevant document when available instead of asking the model to guess what it says. Free users can also try Think for harder questions where it appears. Projects are available without a paid subscription.

### Aletheia check
Do not suggest that Free cannot upload files or search the web. Do not promise unlimited tools or rely on older fixed message limits.

### Sources
- https://help.openai.com/en/articles/9275245-chatgpt-free-tier-faq
- https://help.openai.com/en/articles/9237897
- https://help.openai.com/en/articles/8555545

---

## SW-AI-002 | Talking to ChatGPT is not the same as dictating a research task

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: STRONG for features; CONTEXT for workflow
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: LOW
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
Use Voice when you want a natural spoken discussion. For careful research, an editable transcript, a table or a document, consider microphone dictation into the normal text composer and review the prompt before sending.

### Why useful
Voice's Live mode can use web search and memory where available; it is not incapable of research. However, it uses a different conversation-oriented model, supports a different tool set and its transcript may not reproduce speech exactly. Dictation converts a recording into editable text for the normal chat. Where offered, use the response's Read Aloud or speaker action to listen to the finished text without giving up a readable answer.

### Aletheia check
Voice is a choice, not a safety rating. Ask for visible sources and a written output, then check any important claims. Button names and voice options vary by app/version.

### Sources
- https://help.openai.com/en/articles/20001274
- https://help.openai.com/en/articles/12168547

---

## SW-AI-003 | Prompt shortcuts are plain-language instructions, not magic codes

STATUS: METHOD
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: CONTEXT
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: LOW
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
Short commands can help shape an answer, but phrases such as EXECUTE, NO FAFF and TRUTH are not special ChatGPT control codes. Tell the AI exactly what behaviour you want, especially for important tasks.

### Why useful
**EXECUTE:** Complete the task in this reply, using the available tools; report anything you could not do.
**NO FAFF:** Start with the result, then give only essential detail.
**ELI5 / ELI10:** Explain this for a five-year-old / ten-year-old without changing the factual answer.
**SHORT:** Summarise in five sentences.
**STEP BY STEP:** Give numbered instructions; wait before irreversible actions.
**COMPARE:** Put the differences and trade-offs in a table.
**CHALLENGE:** Test my assumptions and show counterarguments.
**SOURCE CHECK:** Separate confirmed facts, uncertain points and missing evidence.

### Aletheia check
These are Aletheia-recommended prompt recipes. Their success depends on context and available tools; a keyword alone cannot guarantee truth, research, compliance or persistence.

### Sources
- https://help.openai.com/en/articles/9275245-chatgpt-free-tier-faq

---

## SW-AI-004 | Ask ChatGPT to search the web when freshness matters

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: STRONG
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: LOW
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
For news, prices, rules, software features and recent events, tell ChatGPT to search current sources and show publication dates. ChatGPT Free can search the web, subject to limits.

### Why useful
Reusable prompt: **SEARCH CURRENT:** Search the web for this question. Prefer primary sources, include links and dates, and separate verified information from your interpretation. For conflicting results, tell me what each source actually says. The /Search shortcut or search control is available in supported interfaces, but a normal-language request also works.

### Aletheia check
Never confuse a model's memory of an older web page with an actual search. Clicking a citation should reach a source that supports the claim.

### Sources
- https://help.openai.com/en/articles/9237897

---

## SW-AI-005 | Ask for the output format before the AI starts

STATUS: METHOD
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: CONTEXT
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: LOW
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
When you want a table, a checklist, a downloadable file or a direct answer, say that in the prompt. The ordinary text interface makes structured results easier to inspect and reuse than a voice-first conversation.

### Why useful
**TABLE:** Show a table with columns Topic | What is known | Source | Uncertainty.
**ONE QUESTION:** Ask only the single question needed to proceed, otherwise complete the task.
**DO NOT GUESS:** If a necessary fact is missing, label it unknown and say how to verify it.
**COPYABLE:** Give the final version in plain text with no preamble.
**AUDIT:** List the assumptions, calculations and facts that need checking.

### Aletheia check
An AI can still make a convincing-looking wrong table. Check the source rows and any important figures.

### Sources
- https://help.openai.com/en/articles/9275245-chatgpt-free-tier-faq

---

## SW-AI-006 | Custom Instructions are available on ChatGPT Free

STATUS: VERIFIED
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: STRONG
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: MEDIUM: PROFILE MAY CONTAIN PRIVATE PREFERENCES
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
ChatGPT Free users can set Custom Instructions so ordinary chats start with their preferred tone, level of detail and working style without repeating those preferences every time.

### Why useful
Find the available Personalization or Customize ChatGPT controls in Settings. Example: 'Lead with the answer. Be concise and precise. Do not invent facts, links or citations. Clearly label uncertainty. Ask only essential questions. Use light humour only when appropriate. When information may have changed, search and cite sources if search is available.'

### Aletheia check
Instructions guide behaviour but cannot confer missing tools or override platform safeguards. Keep private identifiers, secrets and unnecessary medical or financial details out of shared instruction templates.

### Sources
- https://help.openai.com/en/articles/8096356
- https://help.openai.com/en/articles/7039943

---

## SW-AI-007 | Audit what ChatGPT remembers before correcting its assumptions

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: STRONG
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: MEDIUM: PERSONAL DATA
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
Memory can make ChatGPT more useful but is not a complete or guaranteed record of every conversation. Review Memory in Settings > Personalization; use the Memory summary and its Manage controls if available.

### Why useful
Ask 'What do you currently remember about my preferences for this topic, and which parts are assumptions?' Compare the answer with the Memory summary and the original source chats/files. To correct or fully remove an unwanted personal detail, update the memory summary and remove original chats and other sources containing it. Memory controls and availability can vary by account.

### Aletheia check
Do not claim that saying 'forget this' instantly erases every source. Turning memory off is not the same as deleting history, and a chat summary is not proof of what all stored sources contain.

### Sources
- https://help.openai.com/en/articles/8590148

---

## SW-AI-008 | A free Project can carry Aletheia between chats

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: STRONG
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: MEDIUM: CHECK CONTENT BEFORE UPLOAD
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
Projects are available on ChatGPT Free. Create a Project for a continuing subject, add compact Aletheia bootstrap instructions and, if wanted, your own portable aletheia-memory.md file.

### Why useful
Use Project instructions for Aletheia's evidence and task rules. Keep the user-controlled memory file short and review it before upload. Free accounts currently allow five files per Project, with additional daily file-upload limits. Thalia humour and extra Aletheia apps should be explicitly selected rather than silently turned on.

### Aletheia check
Project instructions are not a replacement for checking whether the AI has actually loaded the right file. Do not claim a file was updated unless you can verify the write.

### Sources
- https://help.openai.com/en/articles/10169521
- https://help.openai.com/en/articles/8555545

---

## SW-AI-009 | Clean up privacy and chat history without confusing the controls

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: STRONG
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: MEDIUM: DELETION CAN BE IRREVERSIBLE
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
ChatGPT's Settings > Data controls lets eligible users manage model-improvement settings, request a data export and delete chats. Temporary Chat can be useful for one-off conversations you do not want in normal history.

### Why useful
'Improve the model for everyone' controls use of eligible new conversation data for model improvement; turning it off does not delete existing conversations. Temporary chats stay out of normal history unless saved and do not create new memories. Privacy-sensitive material should not be uploaded merely to make a generic bootstrap more detailed.

### Aletheia check
Archive, delete, disable training, disable memory and remove an item from a portable memory file are different actions. Review Library files and connected-app sources separately when complete removal matters.

### Sources
- https://help.openai.com/en/articles/7730893
- https://help.openai.com/en/articles/7039943

---

## SW-AI-010 | Use an evidence challenge instead of the word TRUTH

STATUS: METHOD
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: CONTEXT
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: LOW
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
Typing TRUTH is not a guarantee that ChatGPT will verify an answer. Request an evidence audit with explicit tests, citations and clear unknowns.

### Why useful
**VERIFY THIS:** Identify each checkable claim; search current primary sources when available; give the supporting links and dates; flag unsupported or contested claims; correct errors; and finish with 'What remains unknown'.
**RED TEAM:** Give the strongest factual objections to this proposal and explain what evidence would change the conclusion.
**CONFIDENCE CHECK:** State which parts rest on direct evidence and which are interpretation; do not invent a numerical confidence score.

### Aletheia check
Prompts can reduce careless output, not eliminate hallucinations. For health, legal, financial and safety-critical questions, independently verify with appropriate primary sources or qualified professionals.

### Sources
- https://help.openai.com/en/articles/9237897
- https://help.openai.com/en/articles/9275245-chatgpt-free-tier-faq

---

## SW-AI-011 | Make a portable checkpoint before changing AI or starting fresh

STATUS: METHOD
APPLIES_TO: ChatGPT Free on supported web, Windows, Android and iOS experiences; check current interface
EVIDENCE: CONTEXT
CONFIDENCE: HIGH for cited product behaviour; CONTEXT for suggested usage
RISK: LOW
LIFECYCLE: CURRENT / FEATURES AND LIMITS CAN CHANGE
LAST_CHECKED: 2026-09-23

### Summary
Aletheia's CHECKPOINT and HANDOVER prompts create an inspectable summary of the task, rather than trusting any provider to remember every detail from an earlier conversation.

### Why useful
**CHECKPOINT:** Summarise the current goal, completed work, open questions, sources, constraints, corrections and the next specific action.
**HANDOVER:** Produce a portable Markdown brief with confirmed facts, unresolved conflicts, file names, links and decisions, clearly labelling what has not been checked. Use it with the reviewed Aletheia bootstrap and optional personal memory file in a new chat or another AI.

### Aletheia check
Do not insert passwords, API keys or private records into a portable handover. A checkpoint is only as complete as the context the AI can actually access.

### Sources
- https://help.openai.com/en/articles/10169521
- https://help.openai.com/en/articles/8590148

---

## SW-AI-012 | Free Custom Instructions have a 1,500-character limit

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free; availability may vary by region, device and settings
LIFECYCLE: CURRENT / RECHECK IF PROVIDER CHANGES
EVIDENCE: STRONG FOR DOCUMENTED FEATURES; CONTEXT FOR WORKFLOW ADVICE
RISK: LOW FOR READING; MEDIUM WHEN SHARING OR DELETING PRIVATE DATA
LAST_CHECKED: 2026-09-23

### Summary
Free and Go profiles accept up to 1,500 characters of Custom Instructions; changes apply immediately. Keep the long Aletheia bootstrap in Project instructions and use a shorter global profile.

### Why useful
Desktop: Settings > Personalization, enable customization; mobile: Settings > Customize ChatGPT. Keep universal rules short and avoid private identifiers. Relevant Custom Instructions can be passed to a third-party plugin you choose to use. The text of earlier conversations is not retroactively erased by editing the profile.

### Aletheia check
Do not paste the whole 5.8 KB bootstrap into Free Custom Instructions; have AI Easy offer a character-counted short version.

### Sources
- https://help.openai.com/en/articles/8096356

---

## SW-AI-013 | Audit memory sources before correcting or deleting

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free; availability may vary by region, device and settings
LIFECYCLE: CURRENT / RECHECK IF PROVIDER CHANGES
EVIDENCE: STRONG FOR DOCUMENTED FEATURES; CONTEXT FOR WORKFLOW ADVICE
RISK: LOW FOR READING; MEDIUM WHEN SHARING OR DELETING PRIVATE DATA
LAST_CHECKED: 2026-09-23

### Summary
ChatGPT Memory can draw on chats, custom instructions, Library files and connected apps. The Memory summary is an overview, not a complete inventory of every source.

### Why useful
In Settings > Personalization > Memory, review the summary and Manage options. Where shown, inspect Sources beneath a personalised answer to see a relevant chat, file, email or saved memory. Asking not to mention something is different from deleting the original. Complete removal involves changing the Memory summary and removing original chats, archived chats, Library copies and connected sources containing the unwanted detail.

### Aletheia check
Turning Memory off does not delete chats; deleting a chat alone may leave a separately remembered detail. Aletheia's portable memory is its own separate, user-approved file.

### Sources
- https://help.openai.com/en/articles/8590148

---

## SW-AI-014 | Free Projects: five files, project-specific rules and safe sharing

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free; availability may vary by region, device and settings
LIFECYCLE: CURRENT / RECHECK IF PROVIDER CHANGES
EVIDENCE: STRONG FOR DOCUMENTED FEATURES; CONTEXT FOR WORKFLOW ADVICE
RISK: LOW FOR READING; MEDIUM WHEN SHARING OR DELETING PRIVATE DATA
LAST_CHECKED: 2026-09-23

### Summary
ChatGPT Free supports unlimited Projects, with up to five files per Project. Project instructions override global Custom Instructions. Project-only memory is a separate setting.

### Why useful
Create a Project for each ongoing topic; use a short Project bootstrap and an optional portable memory file. Where available, use Project settings to choose default versus Project-only memory. Shared Projects use Project-only memory; shared chats, files and instructions are visible to permitted collaborators. Free accounts can currently share with up to five collaborators. Save useful answers as Project sources or move eligible earlier chats into the Project.

### Aletheia check
Project-only memory does not make sharing invisible to collaborators. Review file contents and sharing permissions before inviting someone.

### Sources
- https://help.openai.com/en/articles/10169521
- https://help.openai.com/en/articles/8590148

---

## SW-AI-015 | Live, Standard and Advanced Voice are different experiences

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free; availability may vary by region, device and settings
LIFECYCLE: CURRENT / RECHECK IF PROVIDER CHANGES
EVIDENCE: STRONG FOR DOCUMENTED FEATURES; CONTEXT FOR WORKFLOW ADVICE
RISK: LOW FOR READING; MEDIUM WHEN SHARING OR DELETING PRIVATE DATA
LAST_CHECKED: 2026-09-23

### Summary
Live Voice can web-search and use memory; Standard transcribes before answering. Advanced can support video/screen sharing for eligible mobile subscribers. ChatGPT Live cannot currently retrieve files from the user's Library.

### Why useful
For research requiring editable prompts and verifiable tables, Dictation into ordinary text chat is often more convenient. Live's transcript is not verbatim. Live/Advanced Voice clips are generally retained for 30 days; Dictation clips are retained while the chat remains in history, with stated deletion exceptions. Review 'Include your audio recordings' in Data controls before sending sensitive speech. Live can mix text/images with voice where available and may use connected plugins when permitted.

### Aletheia check
Never say Voice cannot research: it can web-search. Do not claim Read Aloud or Advanced features exist on every account or device.

### Sources
- https://help.openai.com/en/articles/20001274
- https://help.openai.com/en/articles/12168547
- https://help.openai.com/en/articles/7730893

---

## SW-AI-016 | Web search, chat search and search-query privacy are different

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free; availability may vary by region, device and settings
LIFECYCLE: CURRENT / RECHECK IF PROVIDER CHANGES
EVIDENCE: STRONG FOR DOCUMENTED FEATURES; CONTEXT FOR WORKFLOW ADVICE
RISK: LOW FOR READING; MEDIUM WHEN SHARING OR DELETING PRIVATE DATA
LAST_CHECKED: 2026-09-23

### Summary
ChatGPT Free web search looks at current external sources; the sidebar search finds your existing chats, Projects and files. These are not the same search.

### Why useful
Request Search directly or choose it from the tools menu or slash menu where offered. Open cited sources and check their publication dates. For external web searching, ChatGPT may rewrite the query and share search terms plus general location with partner search providers; enabled memory can shape those query terms. Avoid entering private information merely to make web search more specific.

### Aletheia check
Do not treat a cited result as proof without checking the target text. Keep personal details out of a query sent to third-party search partners when unnecessary.

### Sources
- https://help.openai.com/en/articles/9237897

---

## SW-AI-017 | Free allows existing GPTs, Library and Think, not GPT creation

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free; availability may vary by region, device and settings
LIFECYCLE: CURRENT / RECHECK IF PROVIDER CHANGES
EVIDENCE: STRONG FOR DOCUMENTED FEATURES; CONTEXT FOR WORKFLOW ADVICE
RISK: LOW FOR READING; MEDIUM WHEN SHARING OR DELETING PRIVATE DATA
LAST_CHECKED: 2026-09-23

### Summary
Free users can use existing GPTs but cannot currently create or publish new GPTs on personal accounts. ChatGPT Free includes 500 MB of Library storage and Think where supported.

### Why useful
Free text chat is generally unlimited subject to safeguards. Voice, uploads, image generation and data analysis have separate quotas. Think is supported in mobile and rolling out on web. Use a normal Project for Aletheia setup and keep an independent Markdown backup. An uploaded Project file, a chat attachment and a Library file are distinct contexts; check which one the AI can actually access.

### Aletheia check
Do not publish obsolete fixed rate limits or direct Free users to create new GPTs. Preserve the fallback of pasting the bootstrap and approved memory into an ordinary chat.

### Sources
- https://help.openai.com/en/articles/9275245-chatgpt-free-tier-faq
- https://help.openai.com/en/articles/10169521

---

## SW-AI-018 | Privacy controls: training, Temporary Chat and deletion differ

STATUS: VERIFIED_WITH_CONTEXT
APPLIES_TO: ChatGPT Free; availability may vary by region, device and settings
LIFECYCLE: CURRENT / RECHECK IF PROVIDER CHANGES
EVIDENCE: STRONG FOR DOCUMENTED FEATURES; CONTEXT FOR WORKFLOW ADVICE
RISK: LOW FOR READING; MEDIUM WHEN SHARING OR DELETING PRIVATE DATA
LAST_CHECKED: 2026-09-23

### Summary
Switching off model improvement does not delete chat history. A Temporary Chat stays outside normal history, creates no new memories and is not used for training, but may use existing personalization if selected.

### Why useful
In Settings > Data controls, choose whether eligible new conversations can be used for model improvement. Temporary Chat can start with personalization enabled or disabled where offered; if saved, it becomes a regular chat. For deletion of remembered content, change the Memory summary and remove all source chats, Library files and connected app data. Archiving is not deletion. Before irreversible cleanup, consider an account data export and review existing shared links.

### Aletheia check
Separate voice/dictation recording settings from training, Memory and chat retention. Avoid promising complete immediate erasure.

### Sources
- https://help.openai.com/en/articles/7730893
- https://help.openai.com/en/articles/8590148
- https://help.openai.com/en/articles/20001274

---

# RESEARCH BACKLOG

Candidate additions for a later version, each requiring a current version check before promotion:
- BitLocker manage-bde and PowerShell equivalents.
- Windows Sandbox availability by edition.
- Hyper-V client/server feature matrix.
- Event Forwarding.
- Performance Monitor and perfmon counters.
- Resource Monitor.
- Reliability Monitor.
- ProcMon / Process Explorer / Autoruns from Microsoft Sysinternals.
- PowerToys utilities with version-specific cards.
- DISKPART inspection commands with strong destructive-operation guard rails.
- Storage Spaces.
- ReFS vs NTFS use cases.
- File History and enterprise backup alternatives.
- Credential Manager and Windows Hello.
- Smart App Control / application-control generations.
- Defender Offline and advanced scan workflow.
- Windows Firewall PowerShell administration.
- SMB signing / SMB version checks.
- RDP security and Network Level Authentication.
- Remote PowerShell / WinRM.
- DHCP scopes, reservations and superscopes.
- DNS scavenging / ageing.
- Active Directory replication diagnostics.
- dcdiag and repadmin.
- Server Core management.
- Windows Update for Business / WSUS lifecycle.
- Windows Server 2012/R2 final ESU retirement.
- Server 2016 and Server 2019 lifecycle cards.
- IIS diagnostics.
- Certificate store / certutil, with safe boundaries.
- curl and tar in modern Windows.
- BITS PowerShell versus legacy bitsadmin.
- Scheduled task XML export/import.
- Environment variables in CMD versus PowerShell.
- FOR / FORFILES with destructive-delete warnings.
- CMD delayed expansion.
- SETX caveats compared with temporary SET / PowerShell environment changes.
- NTFS permissions and icacls.
- takeown and ownership recovery risks.
- symbolic links / junctions.
- alternate data streams.
- Windows Search/indexing diagnostics.
- Device Manager / pnputil.
- driver rollback and optional update workflow.
- safe startup / clean boot diagnostic cards.
- Fast Startup versus Restart behaviour.
- Windows 11 accessibility and senior-friendly configuration.
- Chrome profile, password-manager and sync safety.
- Chrome DevTools basics for static-site debugging.
- Search Console page-indexing report interpretation.
- Cloudflare cache, SSL/TLS mode and redirect-loop diagnostics.
- swindon.org.uk live robots/sitemap/header verification once external fetch is consistently available.

# COLLECTION-LEVEL GIST

1. Version comes first. "Windows" is not one stable target.
2. Old command lists are useful maps but poor authorities.
3. Observe before changing.
4. Prefer supported Settings, PowerShell and documented commands over folklore tweaks.
5. PowerShell is the modern automation layer; CMD remains valuable for compact diagnostics and compatibility.
6. WMIC and PowerShell 2.0 demonstrate why deprecation tracking belongs inside the knowledge.
7. "Debloat" should mean removing unnecessary user workload, not amputating platform services.
8. Backups, BitLocker keys and rollback are part of optimisation, not paperwork after it.
9. Server administration moved from old PDC/BDC thinking to multi-master AD, FSMO roles and remote management.
10. Browser, DNS, Search Console and Cloudflare diagnostics belong in the same practical toolbox when the Windows PC is being used to administer a website.
11. Resource/affiliate pages are distribution and funding surfaces; evidence remains independent.
12. Every time-sensitive card should be rechecked before it becomes an automated action.
13. For legacy PCs, "controlled servicing" is a safer default than either unrestricted updating or permanently disabling the update stack.
14. AI can research drivers, but exact hardware IDs, vendor provenance, signatures and rollback determine whether a driver should be installed.

---
ADOPTED_PROTOCOL: [exact title of the protocol file in your folder, for example PROTOCOL.md]
HISTORY_FILE: none
PROJECT_TIMEZONE: [for example America/New_York]
STALE_LOG_DAYS: 14
---
GENERAL_LEAD: [assistant name] (basis: [what its past logs show it did well])

CURRENT STATE (as of [YYYY-MM-DD], [OWN- tag]; 15 lines at most)
Active:
- Protocol: [exact protocol file title]. Master prompt: [name and version, or none]. General lead: [name].
- Zones: [letter and general name of each zone, or "one zone only"].
- Daily carry-forward job: [name, time and timezone, or "none yet"].
Verified:
- [scheduled jobs whose own logs have confirmed name, time and timezone; capabilities shown under rule 14]
Open:
- [decisions waiting on the Owner, each with the log that raised it]
Superseded recently:
- [entries replaced within STALE_LOG_DAYS, with what replaced them]

[PROJECT] STATUS
Maintained by the Owner. Assistants propose changes as STATUS-YYYY-MM-DD-MODEL-NN files; they never edit this file, except to apply an Owner-directed edit (rule 11), which is logged with an AUDIT-TAG line.

TEAM ROSTER
- [Assistant name], tag [TAG]: [role]. Can save straight into the folder: [yes/no, as last verified].
- [Assistant name], tag [TAG]: [role]. Paste mode: [yes/no].

STABLE FACTS
- [Facts that rarely change: project name, purpose, key constraints.]

OPERATIONAL RHYTHM (scheduled jobs; "planned" until each owner checks its own scheduler)
- [Job name], [assistant], [time and timezone], [planned / verified on YYYY-MM-DD].

DATED ENTRIES (newest at the end; never rewritten, only replaced by later entries)
- [YYYY-MM-DD, time] [OWN- tag] [what was decided, in the Owner's words where possible]
  AUDIT-TAG: [OWN- tag] | [type] | [short summary] | Log: [log title]

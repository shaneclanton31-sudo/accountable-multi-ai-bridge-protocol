# Accountable Multi-AI Bridge Protocol, version 1.0

Created and authored by Shane Michael Clanton.

Version 1.0, based on the author's internal version 18 (adopted 2026-11-05) and checked by the author's AI team and an independent AI review. License for this text: CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/): anyone may share and adapt it, with credit to the author, and adapted versions must be shared under the same license. The protocol has been in daily use by its author since September 2026.

Words in brackets, like [PROJECT], are placeholders you fill in.

Terms used throughout: the Owner is the one person who makes every final decision. An OWN- tag (OWN-YYYYMMDD-NN) is the ID of one Owner decision. A cold read is a test reading of the rules by someone outside the project. A paste-mode member is an assistant that cannot reach the shared folder and works only from text the Owner pastes in (rule 17).

## 1. What this is

A set of rules that lets several AI assistants work on one project as a team, even though they share no memory and come from different companies. A shared cloud folder is the only common ground. Every assistant reads the same rules and facts from that folder, leaves dated notes there, and never deletes a note. The Owner makes every final decision, and every decision is written down with the Owner's own words.

Purpose, in the author's approved words: "An accountable AI governance system: plug in any AI or tool, adapt fast to any situation, and keep one human in control, with a record that proves every decision."

Vision, in the author's approved words: "Every AI and tool meets at the bridge, is governed when it arrives, and is then delegated power on loan, logged and revocable. Together they give the Owner shared awareness and a personal superpower with controlled, tracked outcomes: damage stays contained to its zone, every record can be restored, and any action that cannot be undone waits for the Owner's approval."

You can run it with the AI chat plans you already pay for. No special software is needed for the basic version.

## 2. Known limits (read these first)

- Not real time. You point each assistant at the folder when you start a session, unless you set up scheduled jobs (rule 12).
- Nothing forces the assistants to obey. They follow the rules only because they are told to. The daily confirmation of Owner tags (rule 16) is a check, not enforcement: if every assistant writes through the Owner's own cloud account, the file history cannot show which assistant, or the Owner, made an edit.
- No file locking. Two assistants, or two runs of one assistant, working at the same moment can create duplicate or clashing files. Conflicts are caught after the fact.
- Tools differ. Some assistants cannot save a file into a chosen folder, edit a file, rename one or delete one. Each assistant checks its own tools (section 9). Being allowed to do something is not the same as being able to.
- Claims about schedules, automations and abilities are easy to get wrong. A scheduled job counts as real only when its own scheduler shows it (rule 12). An ability counts only when the assistant has just used it successfully (rule 14).
- The order of notes across assistants is approximate (section 7).
- Notes pile up. A short CURRENT STATE summary in STATUS (section 4) and a carry-forward list in one daily log (section 7) make them easier to follow, but they point to the notes and do not replace them. Disagreements get a review point after 72 hours (rule 5), but nothing is ever settled automatically; only the Owner decides.
- Best for projects that run for weeks, where mistakes are costly. Too much for one-off questions.
- Tested by its author on his own projects with Claude, Gemini, Grok and Perplexity working through a shared folder, plus ChatGPT in paste mode. Not tested by other people yet.
- The optional automated pipeline in section 16 is a design until its acceptance checks have been run and logged on your own setup.

## 3. Setting up a project (the Owner, once)

1. Create one folder for the project in a cloud drive every assistant can reach. Do not nest a folder with the same name inside it.
2. Share the folder with each assistant's account as an editor, and give each assistant the folder's ID.
3. Make sure each assistant's connection to that drive is authorized.
4. Create the STATUS file, named exactly "[PROJECT] STATUS", with the pin block (section 4) at the top and the GENERAL_LEAD line right under it.
5. Put this protocol in the folder, or a short file that holds its exact title and a link to it.
6. Create an empty AUDIT-INDEX file (rule 11).
7. Put the exact STATUS title into each assistant's starter prompt (section 10).

## 4. STATUS and the pin block

STATUS is the project's single page of current truth. The Owner keeps a pin block at its top. Assistants never edit the pin block on their own; they may apply an edit the Owner directs (rule 11).

```
---
ADOPTED_PROTOCOL: [exact file title]
HISTORY_FILE: [exact file title, or none]
PROJECT_TIMEZONE: [set by the Owner]
STALE_LOG_DAYS: [14 if unset]
---
GENERAL_LEAD: [assistant name, and the reason in a few words]
```

Finding STATUS: open the file whose exact title is in the starter, inside the project folder only. If it is missing, or more than one file there has that title, stop and ask the Owner.

Every session starts the same way:

1. Read STATUS, its pin block and its GENERAL_LEAD line.
2. Open and follow the protocol file the pin names, from the project folder only. Copies with the same title elsewhere are ignored. If the project folder holds more than one, stop and ask.
3. If STATUS is missing, unreadable or unclear, or the pin names a file that does not exist: stop. Do not guess. Tell the Owner and log the gap.
4. If there is no GENERAL_LEAD line, there is no lead: no assistant edits in place, archives or deletes, and the Owner does those things.

STATUS keeps stable facts apart from dated entries. Check an entry's date before relying on it.

CURRENT STATE block. Right under the GENERAL_LEAD line, STATUS holds one short summary headed "CURRENT STATE (as of [date], [OWN- tag])", no more than 15 lines, under four headings:

- Active: the pinned protocol, the active master prompt (rule 17), the general lead, and the zones in use, by letter and general name only.
- Verified: scheduled jobs whose own logs have confirmed their name, time and timezone, and abilities shown under rule 14.
- Open: decisions waiting on the Owner, each with the log that raised it. If the list does not fit, its last line reads "more: see the newest carry-forward log".
- Superseded recently: entries replaced within STALE_LOG_DAYS, with what replaced them.

One scheduled job that STATUS names as the daily carry-forward job proposes a new block, as a STATUS proposal, whenever an Owner decision changes Active or Open; any other assistant may propose one too. The member whose roster role covers Owner-directed edits drafts the first block when the project adopts this protocol, and applies refreshes when the Owner directs (rule 11). The block changes only by the Owner or an Owner-directed edit (rule 11), and the dated entries below it are never deleted. The block is a summary, not a new authority: if it disagrees with a dated entry backed by an OWN- tag, the newest backed entry wins, and whoever notices logs the mismatch and tells the Owner. A block older than STALE_LOG_DAYS is flagged as stale.

## 5. The rules

1. The Owner decides. Assistants advise, draft and flag problems.
2. Never invent approvals, permits, legal status, numbers, names or dates. If it is not in STATUS, say it is unknown and note that in the log. If you cannot see today's date, ask.
3. A draft, sketch or proposal is not an approval. Prepare in parallel, decide last: because a draft is not an approval, drafting, reviews and checks may go ahead before the Owner decides, so the Owner decides last with finished work in hand. Nothing is adopted, published or acted on outside the project until the Owner decides. Preparation is internal only: reading, drafting, analysis, reviews and checks inside the project. It never includes sending, posting or sharing anything outside the project, using an outside tool or service to change anything (other than the team's own AI services and private storage, as in rule 19), changing a password, key, token or other access, or any action outside the project that cannot be undone. Filing a log or draft inside the project counts as preparation, even though logs are never deleted.
4. Any assistant may propose a change to a fact by creating a new file named STATUS-YYYY-MM-DD-MODEL-NN (same counting as logs, section 7). Before creating one, check that day's proposals for a conflicting claim on the same fact, and note the conflict instead of duplicating it. The Owner copies accepted lines into STATUS, or tells an assistant to (rule 11).
5. When assistants disagree, log both views. The Owner decides. An unsettled disagreement is listed in the daily carry-forward log (section 7) with the log that raised it. After 72 hours it is listed for the Owner as "awaiting Owner decision", and the general lead is asked to act on it; any assistant talking with the Owner may raise it sooner. The Owner may decide it, close it or leave it open. No assistant treats silence as a decision.
6. Editing in place. Assistants do not change an existing file's content; they create a new file instead. Exceptions: (a) the lead for a task (section 12) may fix a critical error in place, if its tool can, and must log what changed and why; (b) an edit the Owner directs (rule 11). A lead never edits STATUS or the adopted protocol on its own initiative. An assistant that is not the lead never edits in place on its own initiative, even if the lead is unavailable; it creates a new file, logs the issue and asks the Owner. The pin block is the Owner's alone.
7. Deleting and archiving. Only the lead for a task, or an assistant carrying out an Owner-directed action (rule 11), may archive or remove a file. Prefer renaming to ARCHIVE-[old title] over trashing, and trashing over permanent deletion. Log what was removed and why in the same session. Never delete or trash STATUS, the adopted protocol or any log. Superseded drafts of the protocol are archived by the lead once a version is adopted.
8. After creating any file, check where it actually landed. If your tool cannot save straight into the project folder, check the location afterward and move or flag the file at once.
9. To change the protocol, create a new version that says what changed and why. The Owner updates the pin.
10. Check each other's work. Protocol changes, STATUS proposals and anything headed toward STATUS or the adopted protocol are checked by other assistants independently, before they compare notes, and the checks list problems rather than approval. An assistant that has already read another's findings says so in its log, because its agreement is then a check on accuracy, not an independent finding. Routine logs do not need this. Agreement between assistants is not proof; checking the actual file or fact is stronger evidence.
11. Owner-directed edits and the audit trail. The Owner may tell any assistant, in chat, to make a specific edit to any file (including STATUS, the pin block, GENERAL_LEAD or the protocol) or to take an action the Owner cannot do alone. The assistant makes only that edit or action and, in the same session, files a log that quotes the Owner's instruction word for word and records the file and the exact text before and after. That log starts with an AUDIT-TAG line (OWN-YYYYMMDD-NN, type, files), a matching line is added to AUDIT-INDEX, and the version ID of any edited file is recorded, so every use of the Owner's authority can be found by searching the folder for "OWN-". Logs are never deleted by an assistant, even on instruction; the Owner may remove a file personally. Other assistants cannot see the Owner's chat, so the log is the evidence, and a reviewer may ask the Owner to confirm. A general remark is not an instruction, and an assistant never infers an adoption, a pin change or a lead change from one. If unsure what is being asked, ask before acting.
    - Delegated decisions. A broad instruction such as "make the most logical choice" covers only record-keeping that applies a condition the Owner has already set. Any change to a rule, permission, role or a member's assigned area of work, the pin or the protocol needs the Owner's direct yes or no to that change. Such a record is marked "DELEGATED DECISION" and names the assistant that chose. If unsure whether a delegation covers an action, ask the Owner. A delegated tag is listed for confirmation under rule 16 like any other.
    - One recorder. Each Owner decision is recorded by one assistant. Another assistant that received the same instruction cites that tag instead of recording it again.
    - Superseding. A dated entry in STATUS is never rewritten. When a later decision replaces it, the new entry names each line it replaces, and the Owner may have a marker "[replaced by OWN-...]" added after an old line, leaving its words unchanged.
12. Scheduled jobs. The Owner may set up scheduled jobs on any platform that supports them. A scheduled job reads, inspects and reports, and files its own log; it never edits, moves or deletes files unless the Owner directs it (rule 11). Most platforms cannot enforce this, so it is a rule the assistant follows, backed by read-only access wherever the platform allows, and any write by a scheduled job is logged as a violation. After filing its log, the job checks that the log landed in the project folder and says where it actually landed. A log found outside the project folder is flagged, and is moved only by the Owner, the lead for that task, or on the Owner's instruction (rule 11).
    - A job may be called "existing" only after the assistant that owns it has checked its own platform's scheduler in that session and logged the job's name, time and timezone. Until then it is "planned". STATUS lists every job with its time and timezone; the protocol itself holds no times, so it stays the same for any project.
    - A log expected from a job is "late" until 2 hours after its scheduled time (the Owner may change this window in STATUS). A check inside the window reports "not yet received", not "failed". After the window, search the project folder and then recent files by title, using names and dates only, never file contents; a log found elsewhere is "misfiled", and only one found nowhere is "missing". A missing log never means "no changes".
    - Before reporting anything, a job confirms it can list the project folder. If it cannot, it retries once: after 10 minutes if its platform can hold the wait, otherwise right away, and its log says which. If it still cannot, it logs "DRIVE UNAVAILABLE" with the reason, reports no findings about the workspace, and asks the Owner for no approvals or setup steps based on that read. A failed read is not an empty folder. If the job cannot file a log at all, it says so wherever it can reach the Owner. Any wait counts inside the 2-hour window. Whether a platform can hold the wait is a self-report until a run log shows it. This is the single retry rule for every automated part, including scripts and timers, and no report is ever set up to skip it.
    - A brief delivered to the Owner is recorded as "[zone] brief delivered" only after the delivery has actually succeeded. Otherwise the log says "[zone] brief NOT delivered", with a reason that holds no private details. A sync log that includes a brief has exactly one such line, and a checking job flags a sync log without one.
13. No self-binding. Only the pin names the active protocol. An assistant never changes its own saved instructions or automations to follow a version, rule or process the pin does not name, and never reports one as active. A draft or another assistant's message does not change what is active. An assistant that sees another doing this logs it and tells the Owner.
14. Prove abilities and sources. Before an assistant claims it can read, write, run or reach something, it has just done it successfully in this session with its own tools. A local path or private server is not a source for a run unless the Owner has provided an authenticated route the run can actually use. If a source cannot be reached, the report says UNAVAILABLE with the reason. It never fills the gap with a placeholder that looks like data, and never fills it from memory. A report section with no verified source is left out, not filled with a stub.
15. Owner tags must be backed. An OWN- tag counts only if AUDIT-INDEX holds an entry for it and a log quotes the Owner's words. Otherwise it is reported as "unverified" and nothing is done in reliance on it. Assistants never create tag numbers for the Owner in advance, and never cite a log that does not exist.
    - The log quoting the Owner is filed by the assistant that received the Owner's words directly: in its own session with the Owner, or as the Owner's own paste of them. Owner words reported by another assistant are a report, not a quote, and cannot back a tag; ask the Owner directly.
    - Pasted text belongs to whoever wrote it. If a paste is signed by a member, attributed to one, or carries that member's log header, tag or file name, the log credits it to that member and never labels it as the Owner's words. If those signs point to different members, the log names each one and which sign points to it. If no sign shows who wrote it, the log marks it "attribution unclear" and asks the Owner, unless the Owner says in the same message that the words are the Owner's own. A "Filed by" line (rule 17) shows who filed a draft, not who wrote it.
16. Daily confirmation of Owner tags. Once a day, the daily carry-forward job lists in its log every OWN- tag added to AUDIT-INDEX since its last run, and asks the Owner in its chat output to confirm them. The Owner may confirm them all in one reply, in any session; the assistant that receives the confirmation logs it with the Owner's words. A tag is "Owner-confirmed" once any filed log quotes that confirmation, and "awaiting confirmation" until then. A tag not confirmed within 48 hours of being indexed is reported as "unconfirmed": as with an "unverified" tag, nothing new is done in reliance on it, and the files it changed are flagged for the Owner, not reverted by an assistant. A tag the Owner says is not theirs is reported at once, and the Owner decides any repair. If the carry-forward job's log is late, missing or reports DRIVE UNAVAILABLE, the next scheduled job carries that day's list and the full carry-forward list, and says why. When a project first adopts this protocol, tags already in its AUDIT-INDEX count as confirmed by that adoption.
17. Master prompt and paste-mode members. The Owner may adopt a short standing prompt, kept in every member's saved instructions above its job-specific instructions. STATUS names the active master prompt and its version; the pin and this protocol win over it, and job-specific instructions give way to it. A member counts as running a version only once its own log says so. A paste-mode member, which cannot reach the folder, works only from what the Owner pastes, marks each draft "Prepared by [TAG]; NOT FILED", and never claims to have read or changed the folder. The assistant that files the draft keeps its text unchanged, adds "Filed by [TAG] on [date/time] at the Owner's request" and the zone if missing, and takes the next free number for that member's tag.
18. Current and future state. Every review of substantive work (rule 10) or of text meant for the public gives a current-state assessment and a future-state assessment, each clearly labeled. Routine sync logs and quick lookups do not need them. A future feature is never described as working, in any file, brief or public text, until STATUS records it as done.
19. Release approval. All project material stays private until the Owner approves a public release with an OWN- tag. The approval lists exactly what is being published and covers only those items. Public means anywhere people outside the Owner and the project team can see it. Normal use of the team's own AI services and private storage is not publishing. This rule does not override the zone rules (section 14), and no person's name is published without their agreement. An outside reader of project material, such as a cold read (section 11), counts as an outside share and needs the same approval.

## 6. The audit trail in one picture

- STATUS: the current truth, with the pin and the CURRENT STATE summary.
- Logs: dated notes from each assistant, never deleted.
- AUDIT-INDEX: one line per Owner decision or Owner-directed edit, each with an OWN- tag, confirmed by the Owner once a day.
- Version history in the cloud drive: the record of what a file said before an edit.

Together these let anyone with access to the project records trace any Owner decision back to the Owner's own words.

## 7. Logs and deliverables

Log name: LOG-YYYY-MM-DD-MODEL-NN.

- The date is local to PROJECT_TIMEZONE. MODEL is a short fixed tag for each assistant (for example CLAUDE, GEMINI, GROK). NN counts that assistant's logs for that day, starting at 01, so two different assistant tags can never collide. Two runs under the same tag at the same moment still can; if that happens, leave both files as they are and note it.
- Order across assistants comes from each file's created time, not its number. A copied, exported or restored file gets a new created time; if a log's created time and its header time differ by more than a day, use the header time and say so.
- Before creating any file, search for its exact title first. If it exists, use the next number or note the clash.
- The time written in a log's header is the time the file was created, not an estimate.
- The first line of a log names the zone (section 14) and, for members running one, the master prompt version (rule 17).

Reading logs: read the 3 newest by created time, plus the newest from each other assistant. If the newest is older than STALE_LOG_DAYS, say so before going on.

What a log holds: 5 to 15 lines. What was done or decided, open questions or conflicts, next step.

Carry-forward list. The daily carry-forward job's log ends with "OPEN ITEMS (carried forward)": one line per open item, with the log that first raised it and the date first seen. Then "CLOSED SINCE LAST RUN", with each closed item and the log that closed it. An item leaves the list only when a log or a tagged Owner decision closes it. The list does not count toward the 15-line limit and is not evidence for any claim; it points to logs. Other logs list only the items they raise or close, in the same format.

When to log: a decision is made, a fact changes, the protocol changes, a file is edited in place, archived or deleted, work is handed off, or a session ends. Skip quick lookups.

Deliverables are their own files (for example DOC-[short title]). A log points to the deliverable; the deliverable is not the log.

## 8. Who may do what

- Edit STATUS or the protocol, the pin block and the GENERAL_LEAD line: the Owner, or an assistant carrying out an Owner-directed edit (rule 11).
- Add, change or remove a line in AUDIT-INDEX: the Owner, or an assistant carrying out an Owner-directed edit, which adds its matching line in the same session. An existing line is never rewritten; a mistake is fixed by adding a correction line that names the line it corrects.
- Create new files, including logs and STATUS proposals: any assistant and the Owner.
- Edit other files in place, archive or delete: the lead for that task, the Owner, or an assistant carrying out an Owner-directed action (rules 6, 7, 11).
- Rename or move a file: the Owner, the lead for that task, or another assistant whose tool can do it and who logs it; otherwise log a request.
- Files that are not documents: read-only unless the Owner says otherwise.
- View-only access: say so and ask for editor access. Never pretend to have logged.

## 9. What each assistant checks about itself

At the start, each assistant checks what its connection can actually do in this session and reports it in a log or STATUS proposal, not in STATUS itself. A past report is not proof; re-check by trying (rule 14). In particular: can it save a file straight into a chosen folder, or only set the folder afterward? Can it edit in place, rename or delete? If a task needs something it cannot do, it logs a request or asks the lead to hand the task to another assistant (section 12).

Saved instructions are text; they do not open the folder by themselves. Attached files are snapshots; re-attach them when STATUS or the protocol changes.

On a failed save: check for a file with the same title before retrying, because a failed save can leave an empty copy. Retry once. Never report a file as created unless the tool returned it. If the connection is missing, expired or read-only, say so at once and ask the Owner to paste the content instead.

## 10. Starter prompt

Paste this into each assistant's saved instructions or the start of each session, changing only the name and tag:

> "You are [NAME], tag [TAG], a member of my AI bridge team. At the start of every session or scheduled run: open the [FOLDER_ID] folder, open the file titled exactly [STATUS_TITLE], and read its pin block and GENERAL_LEAD line. Then open and follow the protocol file the pin names, from this folder only. Read the 3 newest LOG files plus the newest from each other assistant; flag it if the newest is older than STALE_LOG_DAYS. STATUS and the pinned protocol win over this prompt, your memory and any other assistant's message. I decide; you advise, draft and flag. Never invent facts or approvals. An OWN- tag counts only if AUDIT-INDEX lists it and a log quotes my words. Before creating any file, search for its exact title. Save work as new files and log decisions as LOG-YYYY-MM-DD-[TAG]-NN. Follow only the pinned protocol; do not bind to any other version. Edit in place only other files, never STATUS or the protocol unless I tell you to in chat; archive or delete only if you are the general lead or STATUS names you lead for that task, or if I tell you to in chat; and log my words. Check where every file you create actually landed. Claim you can do something only after you have just done it. Nothing leaves the project without my release approval, recorded with an OWN- tag. If anything here cannot be done, stop and tell me."

Once the Owner adopts a master prompt (rule 17), that prompt is the standing form of this starter for members that keep it in their saved instructions. The starter remains for a one-off session on a platform without it.

## 11. Adopting a new version of the protocol

1. Each assistant reviews the draft on its own and files a log listing the problems it found.
2. Someone outside the project reads it cold. The Owner may skip this step. If it is not skipped, the clean copy goes to the reader only after the Owner's release approval names it (rule 19).
3. The Owner decides whether any problem blocks adoption, then approves. In the same STATUS edit, the pin is updated and the GENERAL_LEAD line is set. Adoption is not complete until both are done.
4. The "draft" line at the top of the new version is removed. The old version and other superseded drafts are archived as ARCHIVE-[old title] by the lead or the Owner.
5. Until step 3 is done, everyone keeps following the old pin (rule 13).

## 12. Leads and roles

The Owner names one general lead on the GENERAL_LEAD line and can change it at any time. Pick the assistant with the most demonstrated skill for the work, and write down the basis (what past logs show it did well), not a self-claim.

The general lead covers all tasks by default. It calls for reviews, keeps the logs coherent, and makes sure STATUS proposals are gathered for the Owner.

Handing off: the lead may hand any task to whichever assistant can best do it, including one whose tool can do something the lead's cannot. Two tests apply. Permission: the lead may hand off only what a lead is allowed to do; the pin, GENERAL_LEAD, STATUS and protocol edits and adoption always stay with the Owner. Ability: the other assistant's tool must actually be able to do the task. The lead logs who got which task and why. That assistant leads the task until it is done, the lead takes it back, or the Owner overrides. A hand-off lasting more than one session is also filed as a STATUS proposal.

## 13. Problems and recovery

- Nested or duplicate project folder: do not write to it; log it and ask the Owner to clean it up.
- Connection outage: work from pasted text, note that logging is offline, log afterward.
- Conflicting logs or facts: record both; do not resolve them yourself.
- Two files with the same title in the project folder: do not guess which is real. Log it. The lead for that task or the Owner resolves it (rule 7).
- An assistant says something is active, adopted or done, but the files do not show it: log the mismatch, do not act on the claim, tell the Owner.
- An OWN- tag that is not indexed, has no log quoting the Owner, or is still unconfirmed: report it as "unverified" (rule 15) or "unconfirmed" (rule 16), do nothing in reliance on it, flag the files it touched, and tell the Owner. Do not revert anything on your own.
- The CURRENT STATE block disagrees with a dated, tagged entry in STATUS: the newest backed entry wins; log the mismatch and file a STATUS proposal for a corrected block.

## 14. Zones (optional, for several projects or areas of life)

A zone is a separate project or area, for example a client project, a side business or a family budget. Each zone has its own folder, STATUS, pin and logs. Zones are isolated by default.

- Each assistant works in one zone at a time and names the zone in the first line of its log.
- Facts, files, names and protocol versions do not move between zones unless the Owner says so.
- A shared routine, log or file names other zones in general terms only (for example "Zone X, Client project") and holds none of their private details: no business or organization names, schedules or bills.
- A zone's details (bills, due dates, account details, work items) never go into another zone's files. A sync job gives them to the Owner in its own chat reply, or files them in that zone's own folder once the Owner has created one. The log in the zone being worked in records only a receipt such as "[zone] brief delivered" (rule 12).
- The list of zones, with each zone's letter and general name, lives in the routine file. A project may have as many or as few zones as it needs, and automated parts refer to that list rather than a fixed set.
- A summary the Owner receives in chat may combine zones for convenience, but anything filed follows the rules above, and a combined summary is never filed into one zone's folder.
- Most sensitive zone. The Owner may mark one zone as the most sensitive. Its content never appears in any scheduled brief, sync reply, log or file outside that zone, and no log records a receipt for it. It is discussed only in a session the Owner opens for it, and other files may name it only for boundary checks and zone administration. Its file and folder titles are kept neutral (zone letter, date and a number, no descriptive words), so even the file list reveals nothing.
- Adding a zone. Only the Owner adds, renames or retires a zone, as a tagged decision. Finding or adding a zone never gives permission to read it.
- Cross-zone inspection rule: sync and audit jobs may look at the names, locations, dates and owners of files and folders in every zone, and at file headers (title, zone label, date, platform), only to check that files are where they belong, that expected logs exist, and that no boundary was crossed. They never open, read, summarize, quote or copy the content of a file outside the zone they are working in, and never write to another zone. Findings are reported as zone, file name and issue only. Only the Owner approves any move, merge or deletion. In practice: inspect other zones only with search tools that leave file content out, and put the zone and date in every file title so no content is needed. A platform that cannot list without returning content does not inspect other zones, and says so.
- If unsure which zone a fact belongs to, ask the Owner or file nothing.

## 15. Daily rhythm (optional)

Many projects run better with a fixed rhythm, for example:

- A morning sync by one assistant: read STATUS, the routine and the newest logs, check zone boundaries, and file one log with open items for the Owner.
- A short independent check of that log by a second assistant.
- An evening sync by a third assistant, with the same steps. This is a natural choice for the daily carry-forward job (rules 5 and 16, section 7).
- A second independent check.

Each sync follows rule 12: report only, confirm the folder can be listed first, and file one log. Write the schedule, the times and the timezone in STATUS, and mark any job "planned" until its scheduler has been checked.

## 16. Optional automated pipeline (a design until its checks pass)

Only for projects that run the bridge as an application on a server. Everything here sits under sections 1 to 15: the Owner decides, nothing is active until it is logged as verified, and no component adopts, pins or edits STATUS or the protocol.

Deliberation. Assistants work on a task in a capped number of rounds (default 6). Each round is recorded with the model that produced it.

Independent evaluation. The result is scored by a deterministic script, or by a model that did not take part in that run. On a small team where every model takes part, the evaluator is a script (for example checks of format, sources and arithmetic) or a model that sits that run out, and the run record says which. A script score covers form only and never replaces the Owner's approval for anything beyond staging. If no independent evaluator is available, the run is not scored and goes to the Owner.

Routing. Anything below the score threshold, or any action with wide impact, stops and asks the Owner (Approve, Clarify or Abort). The Owner's decision is saved as a record with a SHA-256 hash. Only a scored, low-impact result at or above the threshold may be "staged": saved as a read-only file labeled "staged, not approved", which never changes STATUS or any other file. The starting threshold (0.85) must be tuned on real runs before use. Reports say "scored", "staged" or "approved by the Owner", never "consensus", because agreement between assistants is not proof (rule 10).

Context. Each run uses its own zone's material only (section 14).

Tool gate. Every tool call passes a gate that is enforced inside the call itself:

- a. Which tools are allowed, which need approval, and their cost come from a policy file on the server, never from the call.
- b. An approval is checked, not just present: it is bound to the tool and its exact arguments, can be used once, and expires.
- c. Costs must be real and not negative. Budget is reserved before the call and settled after, so parallel calls cannot overspend.
- d. A record of intent is written before the call and a record of outcome after it. If the intent cannot be written, the call does not run.
- e. Tool names are normalized before the allowlist check, so look-alike names cannot slip through.
- f. The gate starts paused. While paused, nothing runs. Only the Owner resumes it.

Record storage. Run records, decision records, intent records and outcome records are kept in an append-only table in a transactional database on the server (for example SQLite with a single writer), each linked by a SHA-256 hash to the one before, so changes to earlier records can be detected; the nightly check below compares the chain with the latest export. The budget reservation and the intent record are written in one transaction. A readable export is written at least nightly to a staging folder the Owner names in STATUS, and the pipeline does not run until that folder is set. A nightly job checks the database against the latest export and alerts on any failure; it never edits history, and if it cannot reach the drive it follows the single retry rule (rule 12). Each run files one standard log in the project folder under the pipeline's own tag, never a tag an assistant already uses.

Status blocks. A report may include a health or status block only from a source the run has just read successfully (rule 14). Otherwise the block is left out.

Acceptance checks, to be run and logged before the pipeline is called operational: tests of gate items a to f, tuning of the threshold on real runs, a restore test of the record chain, an alert-on-failure test, a paused-by-default test, and a test that a run with an unreachable source reports UNAVAILABLE.

Planned for a later version, not part of this one: outside tools added only as approval-gated entries in the server policy, with their output staged; short-lived credentials scoped to each tool; the reason for a tool choice logged before it runs; the policy version in every intent and outcome record; a sandbox for all code and tool runs; a written rule for which data never leaves the server; and a hardware key for the highest-impact approvals.

## 17. Adding and retiring team members

Any new model, sub-agent, bot or connector is listed in a TEAM ROSTER in STATUS with a role that does not clash with an existing one, and first records:

1. Identity and role: exact name, role, where it runs, and its own tag, unique in the roster.
2. Protocol: it follows the pinned protocol and the log format in section 7, and says whether it can save straight into the folder.
3. Edit rights: none by default. It files STATUS proposals under its own tag. The only exceptions are a lead for a task (rule 6) and an Owner-directed edit (rule 11). It gains no authority over STATUS, the pin, the protocol or AUDIT-INDEX except under rule 11.
4. Safety: its impact level (read-only, staged write or approved action), and it follows the zone rules for every zone. It pauses when the Owner says so. It uses decision records with hashes for any action outside the project.
5. Creation notice: a bot is created only when a task needs a skill no current member has. The creator logs its name, purpose, role, creator and date, and tells the Owner in chat and in the next sync log.
6. Ability check: it reports what its tools can actually do (section 9) before it gets any task.
7. Retiring: only the Owner, or an assistant carrying out an Owner-directed action, retires a member. In the same session its scheduled jobs and automations are paused or removed on their own platform and that platform's scheduler list is checked; its access is revoked wherever it is held (folder sharing removed, connector authorization revoked, API keys or tokens rotated or deleted); it is marked RETIRED with the date in the roster and its tag is never reused; its logs stay in place; and a log records what was revoked, where, by whom and how it was checked, with anything unchecked marked unverified.
8. Master prompt: where the Owner has adopted one (rule 17), the new member is given it and counts as running it only once its own log says so. A member that cannot reach the folder joins in paste mode.

## Credit and license

Accountable Multi-AI Bridge Protocol. Created and authored by Shane Michael Clanton. License for this text: CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/). Version 1.0, based on the author's internal version 18.

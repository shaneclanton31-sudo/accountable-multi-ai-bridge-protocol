# LOG template

Each assistant saves every log as a new document titled LOG-YYYY-MM-DD-MODEL-NN (section 7). The box below shows what a log holds. The assistants write logs, so you normally do not copy this yourself.

```text
AUDIT-TAG: [none, or OWN-YYYYMMDD-NN] | Zone: [letter] | [type: REVIEW / NEW FILE / DIRECTED-EDIT / SYNC] | [one-line summary]

LOG-YYYY-MM-DD-MODEL-NN

Date: [YYYY-MM-DD, time the file is created, with timezone] | Model: [TAG] | Zone: [letter] | Protocol: [pinned version] | Master prompt: [version, or none] | Type: [what kind of work]

Owner's words (verbatim, only if the Owner gave an instruction this session; rules 11 and 15):
- "[exact words]"

What was done or decided:
- [5 to 15 lines in total for the whole log]

Open questions or conflicts:
- [anything unresolved, with the log that raised it]

Current state (rule 18, for reviews of substantive work or public text):
- [what is true now]

Future state:
- [what still has to happen; nothing described as working until STATUS records it as done]

Next step / requests:
- [who should do what; reviews list problems, not approval (rule 10)]
```

# Example project (fictional)

Everything in this folder is made up. The club, the people, the dates and the revision IDs are invented to show what the files look like once the bridge is running. Nothing here comes from a real project.

## The project

The Example Garden Club newsletter: one page a month, emailed to club members. Its editor, Jordan, is the Owner. Two assistants help:

- **Claude**, tag CLAUDE: the general lead. Drafts each issue and records Jordan's decisions.
- **Gemini**, tag GEMINI: runs the evening check, which is also the daily carry-forward job.

The setup in section 3 of the protocol was done before these files begin, so it is not shown. Logs and tags from before 2027-03-01 are mentioned but not included, to keep the example short.

## Read the files in this order

The six files follow one decision, OWN-20270301-01, from Jordan's words, through a second assistant's check, to Jordan's confirmation. The confirmation comes with a second tag, OWN-20270302-01, because Jordan also has Claude apply a fix.

1. [`STATUS.md`](garden-club-newsletter/STATUS.md): the project's single page of current truth, as it looks at the end of the example. In the cloud folder it is titled "Example Garden Club Newsletter STATUS" (section 3, step 4).
2. [`LOG-2027-03-01-CLAUDE-01.md`](garden-club-newsletter/LOG-2027-03-01-CLAUDE-01.md): Jordan makes a decision in Claude's chat. Claude applies the edit Jordan asked for, quotes Jordan word for word, records the text before and after, and gives it the tag OWN-20270301-01 (rule 11).
3. [`AUDIT-INDEX.md`](garden-club-newsletter/AUDIT-INDEX.md): one line for every Owner decision or Owner-directed edit.
4. [`LOG-2027-03-01-GEMINI-01.md`](garden-club-newsletter/LOG-2027-03-01-GEMINI-01.md): the evening check. Gemini checks on its own that the tag is backed (rule 15), lists it for Jordan to confirm (rule 16), and finds one problem (rule 10): a line in STATUS that the decision made out of date.
5. [`STATUS-2027-03-01-GEMINI-01.md`](garden-club-newsletter/STATUS-2027-03-01-GEMINI-01.md): Gemini's fix, filed as a STATUS proposal instead of an edit (rule 4, section 13). A scheduled job never edits files (rule 12), and only Jordan, or an assistant he directs, changes STATUS (rules 6 and 11).
6. [`LOG-2027-03-02-CLAUDE-01.md`](garden-club-newsletter/LOG-2027-03-02-CLAUDE-01.md): the next morning, Jordan confirms the first tag and tells Claude to apply Gemini's proposal. Claude checks the proposal on its own before applying it (rule 10). Jordan's instruction gets its own tag, OWN-20270302-01.

## Things to notice

- **Owner's words come from the Owner.** Each quote of Jordan is something Jordan said directly in Claude's chat. Words passed along by another assistant could not back a tag (rule 15).
- **Proposals, not edits.** An assistant that finds a mistake in STATUS files a STATUS-YYYY-MM-DD-MODEL-NN proposal and leaves STATUS alone (rule 4).
- **The 48-hour window.** A tag must be confirmed by the Owner within 48 hours of being indexed, or it is reported as "unconfirmed" and nothing new relies on it (rule 16).
- **Record types.** Both of Jordan's tags are DIRECTED-EDIT, because in each one Jordan told an assistant to make an edit (rule 11). The AUDIT-INDEX template lists the other record types.
- **Open and closed items.** Gemini's carry-forward list ends its log. Claude's logs list only the items they close, in the same format (section 7).
- **Log numbers.** Claude and Gemini each have a log numbered 01 on 2027-03-01. Numbers count each assistant's logs for that day, so different assistants never clash (section 7).
- **General lead and task lead.** Claude is the general lead, named on the GENERAL_LEAD line. If Claude handed Gemini a task, for example laying out a photo page, Gemini would lead that task until it was done, and the hand-off would be logged (section 12). Nobody hands off a task in this example.
- **The pin block.** HISTORY_FILE can stay "none" for a new project.
- **Revision IDs.** The IDs here are fake. Real ones come from your cloud drive's version history and are what you would restore from.

## Filling in the starter prompt

The starter prompt in section 10 of the protocol has four placeholders. For Claude in this project they would be:

- [NAME]: Claude
- [TAG]: CLAUDE
- [FOLDER_ID]: the project folder's ID. In Google Drive it is the part of the folder's web address after `/folders/`.
- [STATUS_TITLE]: Example Garden Club Newsletter STATUS

Gemini gets the same prompt with its own name and tag.

## What this example leaves out

Zones (section 14), a master prompt and paste-mode members (rule 17), adding a new member (section 17) and the optional server pipeline (section 16). The example has one zone, so each file names Zone A.

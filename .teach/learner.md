# Learner profile

This file tracks what you know, what you're working on, and what tripped you up. It is updated by the tutor at the end of each session. You can edit it by hand too — it's just markdown.

## Currently studying

- LPIC-1 — exams 101-500 and 102-500, objectives version 5.0.

## Goal

One sentence: what you want to be able to *do* once you understand the current topic. Set during calibration; paired with `Currently studying` — when the topic shifts, replace both together. Downstream modes (tutoring and arc planning) read this to calibrate what is worth emphasizing.

- Certification — pass both LPIC-1 exams to get certified.

## Known solid

Things you've retrieved correctly on multiple occasions, including after a gap. The tutor will use these as foundations to build on and as analogies when teaching new material.

_(Empty. Fills in as you demonstrate solid understanding.)_

## Shaky

Things you've seen but haven't consolidated. The tutor will prioritize these for drill and for Feynman-style explain-backs.

- Numeric permissions — 2026-10-03: unable to interpret chmod 755; 2026-10-05: decoded 644/755, directory x entry, chmod numeric/symbolic practiced; needs independent recall.
- Output redirection — 2026-10-03: recognizes combined output/errors; 2026-10-05: applied >, >>, <, 2>, &>, 2>&1 and pipes with guidance; stream placement still shaky.
- systemd service lifecycle — 2026-10-03: start versus enable unknown.
- Bash quoting and empty arguments — 2026-10-03: guided success; splitting and argument counts need review.
- PATH lookup — 2026-10-03: explained order; 2026-10-05: clean fresh example on ./python3, bare PATH lookup and first match; more review due.
- Variable reassignment and PATH updates — 2026-10-03: substitution improved; construction needed hints.
- Command classification via type — 2026-10-03: identified cd builtin and ls alias; 2026-10-05: forgot type and initially misclassified external path; needs review.
- Shell variable inheritance and export — initially shaky 2026-10-03; 2026-10-04 explained reassignment and child changes not affecting parent after guidance; retention pending.
- File operations and quoted filenames — 2026-10-04: cp/mv/rm and recursion understood; composing exact spaced filenames needed scaffolding.
- Directory removal — 2026-10-04: rmdir and parent traversal understood stepwise; needs independent recall.
- Globbing and find — 2026-10-04: assembled quoted -name/-iname with -type f; Bash expansion versus find matching remains shaky.
- History and documentation — 2026-10-04: history, numbered recall, Up, help and man demonstrated; manual searching needed hints.
- File-copy paths and file inspection — 2026-10-05: mkdir -p, cp directory destinations, study/. dotfiles and file/touch practiced with hints; review independently.
- Text filters and pipelines — 2026-10-05: grep, head/tail, wc, sort/uniq practiced; initially missed nonadjacent-duplicate and frequency behavior.
- Output versus error redirection — 2026-10-05: >, >>, 2>, &> and pipes applied; initial confusion on which stream reaches wc, then resolved.
- Regex basics — 2026-10-05: ^, $, ., *, .*, [0-9] practiced; .* same-char model corrected after contrast; needs spaced recall.
- Vi editing — 2026-10-05: open/insert/save-quit/delete/undo/search/yank/navigate practiced same-session; needs independent recall.
- Archiving and compression — 2026-10-05: tar -cf/-tf/-xf/-zcf, gzip replacement/-d, zcat practiced with hints; needs review.
- File ownership and links — 2026-10-05: chown owner/group, directory-x entry, hard vs symlink survival understood after guidance; needs recall.

## Misconceptions caught

Confidently-held beliefs that turned out to be wrong. These are high-value entries — they flag places where future teaching needs to actively work against a prior model, not just add to a blank slate. Include the date.

- find -P scope — 2026-10-04: thought it restricted Bash expansion; clarified it controls symlink handling, while the path specifies search scope; recheck later.
- uniq scope — 2026-10-05: expected separated duplicate lines to collapse; corrected that uniq only removes adjacent repeats, so sort first.
- Regex .* scope — 2026-10-05: thought ^A.*C$ required same repeated middle char; corrected that each . can differ after A* vs .* contrast.
- Hard-link survival — 2026-10-05: thought symlink or neither survives original deletion; corrected hard link persists as second name for same data.
- Directory-x meaning — 2026-10-05: thought r-- directory allows opening inside files; corrected x is needed to enter/reach entries.

## Calibration notes

One-line notes from calibration runs. Useful to see how your self-assessment has shifted over time.

- 2026-10-03 — Self-rated medium; Ubuntu/Debian user; foundational exam gaps; neither exam booked.
- 2026-10-03 — Active shell is Fish; tutor initially assumed Bash. Use Bash for exam practice.

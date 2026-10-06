# LPIC-1 Progress

Last updated: 2026-10-06

**Stage:** Exam 101 preparation → Module 1: Command-line workflows  
**Current objective:** 103.1 — Bash variables, quoting and PATH updates (review in progress).

Earlier tutoring incorrectly called file management 103.2; 103.2 is text-stream processing.

## Skills demonstrated this session

| Skill | Progress |
|---|---|
| Single quotes versus double quotes | Correct answers across several examples |
| Quoting filenames containing spaces | Applied independently with `cd "$folder"` |
| Unquoted word splitting | Understood after hints; needs review |
| Empty argument versus no argument | Needed repeated guidance; needs review |
| `PATH` search order | Correctly identified the first matching directory |
| Absolute paths and `./command` | Correct answers and explanation |
| Variable reassignment | Understood with simpler examples |
| Preserving and extending `PATH` | Completed with guidance; needs independent practice |
| Functions, builtins, external commands | Builtin and alias identified; alias expansion needed guidance |
| Export and child environments | Explained updated values and child-to-parent isolation after guidance |
| History and documentation | Used history recall, Up, help, man, and guided manual searches |
| cp, mv, rm and -i | Correct command choices; quoted filename composition needed guidance |
| Recursive copying/removal | Correctly identified -r and nested-directory behavior |
| rmdir and -p | Distinguished empty-only removal and parent traversal after hints |
| Hidden files | Independently explained ls -a |
| find | Constructed -name/-iname with -type f; quoted wildcard reasoning needs review |
| mkdir -p and file inspection | Used mkdir -p, file and touch; required prompts on command arguments and repeat behavior |
| Copying directories | Understood existing versus missing destination after a hint; used study/. for dotfiles |
| File inspection and filters | Applied cat, less, head, tail, grep -i and wc -l |
| Sorting and duplicate handling | Combined `sort` with `uniq` and `uniq -c`; corrected nonadjacent duplicate misconception |
| Streams and redirection | Used >, >>, 2>, &> and pipelines; distinguished stdout/stderr after hints |
| Input redirection and tee | Used <, 2>&1 into pipes and tee display-plus-save after guidance |
| Cut, regex and counts | Built cut -d/-f, ^/$/./*/[] patterns and sort \| uniq -c with corrections |
| Vi editing | Practiced open/insert/save-quit/delete/undo/search/yank/first-last navigation |
| Archives and compression | Used tar -cf/-tf/-xf/-zcf, gzip replace/-d and zcat with prompts |
| Permissions, ownership, links | Decoded 644/755, directory-x entry, chmod/chown and hard-vs-symlink after guidance |

## Overall syllabus

- **1 module in progress:** Command-line workflows.
- **9 modules not started.**
- **0 modules marked mastered; 1 review skill mastered (PATH lookup).** Full modules require broader coverage and recall across sessions.

Objective **103.1 is substantially introduced but unmastered**; PATH lookup is the first mastered review skill. **103.3** includes file operations, directory copies, find, tar and compression; **103.2** includes text filters, cut, regex basics and sort/uniq; **103.4** includes pipes, redirection, tee and stderr handling; **103.8** vi basics introduced. Early **104.5–104.7** permissions, ownership, links and FHS also started. Each module remains partially covered.

## Next session

1. Enter **Bash** for exam practice.
2. Review learning-bucket sorting/uniq, regex, export and stderr separately; revisit empty quoted arguments, tar -f and vi Esc where hints were needed.
3. Resume at the unanswered PATH assignment: prepend `/opt/tools` while preserving the old PATH.

## Summary

PATH lookup reached review-skill mastery on a second clean day; no complete module is mastered yet. Sorting/uniq, regex, export and error redirection moved into learning after fresh recall. Empty arguments and quote distinctions, tar -f and vi mode changes still needed hints. Next up: independent PATH assignment.

Session notes: [Session 1 — Command-Line Fundamentals](session-01-command-line.md).

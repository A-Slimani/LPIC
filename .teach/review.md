# Review queue

Items the tutor will drill you on for retention. Managed by the tutor — you don't need to edit this, though you can if you want to drop an item.

See the `teach` skill's `references/review-buckets.md` for how items move between buckets (wherever the skill is installed on your system).

## new

Items introduced recently. Not yet due for drill — they need a session to settle first.

- Bash quoting and word splitting — introduced 2026-10-03; literal quotes correct, splitting needed hints.
- Empty quoted versus unquoted expansion — introduced 2026-10-03; argument counts need review.
- Variable reassignment and PATH updates — introduced 2026-10-03; preserving old values needed hints.
- Command classification with type — introduced 2026-10-03; builtin vs alias identified, expansion needed hints.
- Shell vs exported variables across processes — introduced 2026-10-03; guided success 2026-10-04 on reassignment and child isolation; clean recall pending.
- File operations with quoted filenames — introduced 2026-10-04; cp/mv/rm and -i practiced; composition needed hints.
- Recursive copying and removal — introduced 2026-10-04; cp -r and rm -r identified independently.
- Empty-directory and parent removal — introduced 2026-10-04; rmdir and -p needed scaffolding.
- Globbing and find patterns — introduced 2026-10-04; -name/-iname, -type f, -P practiced; quoting mechanism needs review.
- History and documentation lookup — introduced 2026-10-04; recall methods correct, manual search guided.
- Hidden filenames — introduced 2026-10-04; explained dot names and ls -a independently.
- mkdir -p and directory-copy destinations — introduced 2026-10-05; mkdir repeat and existing vs missing cp destination practiced with hints.
- Copying directory contents and symlinks — introduced 2026-10-05; study/. includes dotfiles, cp -a preserves links; guided.
- File type and timestamps — introduced 2026-10-05; file and touch used after scaffolding.
- Text inspection and filtering — introduced 2026-10-05; cat/head/tail, grep -i, wc -l and pipe applied.
- Sorting, uniq, and counts — introduced 2026-10-05; sort before uniq and uniq -c; count needed prompt.
- Normal/error output and redirection — introduced 2026-10-05; >, >>, 2>, &> and pipe; final placement correct.
- Input redirection and tee — introduced 2026-10-05; < feeds stdin, tee shows+saves; utility questioned then applied.
- Cut fields and role counts — introduced 2026-10-05; -d/-f, sort | uniq -c; Feynman explanation held.
- Regex anchors and quantifiers — introduced 2026-10-05; ^, $, ., *, .*, [0-9]; same-char model corrected.
- Vi editing basics — introduced 2026-10-05; open/insert/save/quit/delete/undo/search/yank/navigate practiced.
- Tar and gzip handling — introduced 2026-10-05; -cf/-tf/-xf/-zcf, gzip replace/-d, zcat; file flag needed prompts.
- Permissions, ownership and links — introduced 2026-10-05; 644/755, directory x, chmod/chown, hard vs symlink; guided.

## learning

Items you've seen but haven't fully consolidated. Most drill activity happens here.

- PATH search and explicit command paths — introduced 2026-10-03; clean application 2026-10-05, clean drill later same day; remains learning pending another-day recall.

## mastered

Items you've retrieved cleanly on multiple separate sessions. Occasionally re-checked; demoted back to `learning` if you miss one.

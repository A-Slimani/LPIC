# Review queue

Items the tutor will drill you on for retention. Managed by the tutor — you don't need to edit this, though you can if you want to drop an item.

See the `teach` skill's `references/review-buckets.md` for how items move between buckets (wherever the skill is installed on your system).

## new

Items introduced recently. Not yet due for drill — they need a session to settle first.

- Bash quoting and word splitting — introduced 2026-10-03; literal quotes correct, splitting needed hints.
- Empty quoted versus unquoted expansion — introduced 2026-10-03; argument counts need review.
- Variable reassignment and PATH updates — introduced 2026-10-03; preserving old values needed hints.
- Command classification with type — introduced 2026-10-03; builtin vs alias identified, expansion needed hints.
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
- Input redirection and tee — introduced 2026-10-05; < feeds stdin, tee shows+saves; utility questioned then applied.
- Cut fields and role counts — introduced 2026-10-05; -d/-f, sort | uniq -c; Feynman explanation held.
- Vi editing basics — introduced 2026-10-05; open/insert/save/quit/delete/undo/search/yank/navigate practiced.
- Tar and gzip handling — introduced 2026-10-05; -cf/-tf/-xf/-zcf, gzip replace/-d, zcat; file flag needed prompts.
- Permissions, ownership and links — introduced 2026-10-05; 644/755, directory x, chmod/chown, hard vs symlink; guided.

## learning

Items you've seen but haven't fully consolidated. Most drill activity happens here.

- Sorting, uniq, and counts — introduced 2026-10-05; clean fresh sort | uniq -c for separated roles 2026-10-06; repeat another day.
- Regex anchors and quantifiers — introduced 2026-10-05; clean ^READY$ and zero-or-more in ^A.*C$ 2026-10-06; other forms still due.
- Shell vs exported variables across processes — introduced 2026-10-03; clean Oct 6 prediction of B after export then reassignment; repeat another day.
- Normal/error output and redirection — introduced 2026-10-05; clean Oct 6 prediction 2>&1 | wc -l counts stdout+stderr; other operators still need recall.

## mastered

Items you've retrieved cleanly on multiple separate sessions. Occasionally re-checked; demoted back to `learning` if you miss one.

- PATH search and explicit command paths — introduced 2026-10-03; clean Oct 5 and clean drill Oct 6 across separate days.

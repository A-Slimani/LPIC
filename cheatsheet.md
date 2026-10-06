# LPIC-1 command cheat sheet

Run these examples in **Bash** (your usual Fish shell behaves differently).

| Command | Quick reminder |
|---|---|
| `bash` | Start a Bash shell for exam practice. |
| `exit` | Leave the current shell. |
| `name="Aboud Ali"` | Set a shell variable; no spaces around `=`. |
| `echo "$name"` | Print its value as one argument, preserving spaces. |
| `echo '$name'` | Print the literal text `$name`. |
| `echo $name` | Unquoted expansion can split into multiple arguments. |
| `name=""` | Set an empty value; `"$name"` is one empty argument, `$name` can disappear. |
| `mkdir "$name"` | Make one directory, even if its name contains spaces. |
| `touch "$name"` | Create a file; quote names containing spaces. |
| `cd "$folder"` | Change into a directory whose name may contain spaces. |
| `ls -l "$file"` | List details for a filename, preserving spaces. |
| `printenv PATH` | Show the exported command-search directories in order. |
| `PATH="/home/aboud/bin:$PATH"` | Prepend a directory, keeping the old PATH. |
| `PATH="$PATH:/home/aboud/tools"` | Append a directory, keeping the old PATH. |
| `./hello` | Run `hello` in the current directory without searching PATH. |
| `/usr/bin/hello` | Run an executable by absolute path without searching PATH. |
| `type cd` | Identify how Bash resolves `cd` (a builtin). |
| `type ls` | Check whether `ls` is an alias, builtin, or executable. |
| `export course` | Mark the variable for inheritance by future children; each gets its value at launch. |
| `bash -c 'echo $course'` | Start a child Bash, run one command, then exit. |
| `printenv lesson_probe` | Show a variable if it was exported to this process. |
| `history` | List commands you've entered with their history numbers. |
| `!<number>` | Rerun that numbered history entry in interactive Bash. |
| `↑` | Recall the previous command for editing before running it. |
| `help cd` | Read Bash's help for its `cd` builtin. |
| `cd --help` | Show Bash's short help for `cd`. |
| `man ls` / `man cp` | Read manual pages for external commands. |
| `ls --help` | Show quick help for `ls`. |
| `/interactive` (inside `man cp`) | Search the manual page for “interactive”. |
| `cp notes.txt notes-backup.txt` | Copy source to destination; existing destination may be overwritten. |
| `cp -i notes.txt notes-backup.txt` | Ask before overwriting the destination. |
| `cp -i "study notes.txt" "backup notes.txt"` | Copy spaced filenames, asking before overwrite. |
| `mv "study notes.txt" "final notes.txt"` | Rename or move a file; the old path disappears. |
| `mv -i source destination` | Ask before replacing an existing destination. |
| `rm "final notes.txt"` | Delete the named file. |
| `cp -r study study-backup` | Copy a directory and its nested contents recursively. |
| `rm -r study-backup` | Remove a directory and its contents recursively. |
| `rmdir study-backup` | Remove an empty directory; fails if it has contents. |
| `man -k 'remove empty directories'` | Search manual descriptions for matching commands. |
| `echo *.md` | Bash expands matches first; with none, default Bash leaves the pattern literal. |
| `ls -a` | Include dot-prefixed (hidden) names such as `.config`. |
| `rmdir -p study/week1` | Remove the named directory, then its parents, only while each is empty. |
| `find study -name 'notes.txt'` | Search recursively under `study` for this exact name. |
| `find -P study -name '*.txt' -type f` | Find regular `.txt` files recursively; `-P` means do not follow symbolic links (default). |
| `find study -iname '*.txt' -type f` | Match regular files case-insensitively, including `.TXT`. |
| `mkdir -p labs/linux/day1` | Create missing parent directories; existing ones are okay. |
| `cp -r study backup/` | If `backup/` exists, copy the tree as `backup/study/`. |
| `cp -r study backup` | If `backup` is absent, create it as the copied tree. |
| `cp -rp study/. backup/` | Copy directory contents, including dotfiles, and preserve metadata. |
| `cp -a study/. backup/` | Archive-copy contents, preserving links and metadata. |
| `file photo.txt` | Inspect file contents to identify type, regardless of extension. |
| `touch results.txt` | Create an empty file, or update an existing file's timestamps. |
| `type python3` | Show how Bash resolves a command name. |
| `cat results.txt` | Print the whole file. |
| `less results.txt` | Browse a file a screen at a time. |
| `head -n 3 results.txt` | Print the first three lines. |
| `tail -n 5 results.txt` | Print the last five lines. |
| `grep -i 'ERROR' results.txt` | Print lines containing ERROR, ignoring case. |
| `grep -i 'ERROR' results.txt \| head -n 3` | Print the first three matching lines. |
| `grep 'ERROR' results.txt \| wc -l` | Count matching lines, not occurrences within a line. |
| `sort names.txt` | Print lines in sorted order without changing the file. |
| `sort names.txt \| uniq` | Remove duplicates after sorting puts them next to each other. |
| `sort names.txt \| uniq -c` | Show each distinct line with its frequency. |
| `wc -l names.txt` | Count all lines in a file. |
| `sort names.txt \| uniq > unique-names.txt` | Save output, creating or replacing the destination. |
| `sort names.txt >> sorted.txt` | Append output without replacing existing contents. |
| `sort names.txt 2> errors.txt` | Save errors while leaving normal output on screen. |
| `sort names.txt &> all-output.txt` | In Bash, save both normal output and errors. |
| `sort names.txt 2> errors.txt \| wc -l` | Save sort's errors; count lines of its normal output. |
| `sort < input.txt` | Feed file contents into sort through standard input. |
| `wc -l < input.txt` | Count lines without printing a filename. |
| `sort missing.txt 2>&1 \| wc -l` | Send errors into the pipe by joining stderr to stdout. |
| `grep -i 'ERROR' results.txt \| tee matches.txt` | Show matches and save them to a file. |
| `tee -a matches.txt` | Append instead of replacing the file. |
| `cut -d : -f 2 users.txt` | Print field 2 using : as delimiter. |
| `grep '^ERROR' results.txt` | Match lines starting with ERROR. |
| `grep 'ERROR$' results.txt` | Match lines ending with ERROR. |
| `grep '^ERROR$' results.txt` | Match lines containing only ERROR. |
| `vi notes.txt` | Open a file in vi. |
| `i` / `Esc` | Enter insert mode / return to command mode. |
| `:w` / `:wq` / `:q!` | Save / save-quit / quit without saving. |
| `dd` / `u` | Delete current line / undo. |
| `/ERROR` / `n` | Search forward / next match. |
| `yy` / `p` | Copy line / paste below. |
| `gg` / `G` | First line / last line. |
| `tar -cf study.tar study/` | Create an uncompressed archive. |
| `tar -tf study.tar` | List archive contents. |
| `tar -xf study.tar` | Extract an archive. |
| `tar -zcf study.tar.gz study/` | Create a gzip-compressed archive. |
| `gzip notes.txt` | Replace file with compressed .gz version. |
| `gzip -d notes.txt.gz` | Decompress back to the original name. |
| `zcat notes.txt.gz` | View compressed text without restoring. |
| `chmod 644 notes.txt` | Set owner rw, group r, other r. |
| `chmod u+x script.sh` | Add owner execute permission. |
| `chown sam notes.txt` | Change file owner to sam. |
| `chown sam:dev notes.txt` | Change owner to sam and group to dev. |
| `ln -s target link` | Create a symbolic link to target. |

Quote `find` patterns so **find**, not Bash in the current directory, matches them.

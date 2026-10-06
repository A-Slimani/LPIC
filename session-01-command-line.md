# LPIC-1 — Session 1: Bash Command-Line Fundamentals

Date: 2026-10-03  
Objective: 103.1 — Work on the command line  
Goal: prepare for LPIC-1 exams 101-500 and 102-500 (objectives v5.0).

## 1. Our practice shell: Bash

Your terminal was running **Fish**. We discovered this when `type cd` displayed a Fish function defined in `/usr/share/fish/functions/cd.fish`.

LPIC-1 objective 103.1 assumes **Bash**. The examples below use Bash syntax and behavior; Fish differs, including in variable handling and word splitting.

Start a Bash session for practice:

```bash
bash
```

Use `exit` to return to Fish. This does not change your default shell.

## 2. Variables: assignment and expansion

Assign a value with `name=value`, with no spaces around `=`:

```bash
name="Aboud"
echo "$name"
# Output: Aboud
```

- `name` on the left names the variable being assigned.
- `$name` retrieves its current value (variable expansion).
- Quotes group text; the quote characters themselves are not part of the stored value.

A new assignment replaces the previous value:

```bash
color="blue"
color="red"
echo "$color"
# Output: red
```

## 3. Double quotes versus single quotes

```bash
name="Aboud Ali"
```

| Expression | What Bash passes as arguments |
|---|---|
| `"$name"` | One argument: `Aboud Ali` |
| `'$name'` | One literal argument: `$name` |
| `$name` | In these command examples, two arguments: `Aboud` and `Ali` |

**Double quotes** allow variable expansion while preserving the expanded value as one argument. **Single quotes** preserve the text literally, without variable expansion.

Examples (assuming the directories do not already exist):

```bash
mkdir "$name"   # Creates one directory: Aboud Ali
mkdir $name     # Creates two directories: Aboud and Ali
mkdir '$name'   # Creates one directory literally named $name
```

## 4. Word splitting and filenames with spaces

In Bash, unquoted variable expansion in ordinary command arguments undergoes word splitting. With the default settings, spaces separate words (tabs and newlines also act as separators).

```bash
file="study notes.txt"
ls -l "$file"
```

The quoted version passes the complete filename as one argument. Without quotes, `ls` receives separate names, `study` and `notes.txt`.

The same pattern applies to directory names:

```bash
folder="exam practice"
cd "$folder"
```

**Useful habit:** double-quote variable expansions representing a single filename or directory.

## 5. An empty argument is different from no argument

```bash
name=""
```

| Command | Arguments passed to the command |
|---|---|
| `mkdir "$name"` | One argument containing an empty string |
| `mkdir $name` | Zero arguments |
| `touch "$name" notes.txt` | Two arguments: an empty string and `notes.txt` |
| `touch $name notes.txt` | One argument: `notes.txt` |

Think of an argument as a box: **an empty box still counts as a box**. With an empty, unquoted expansion, that box disappears.

`mkdir` cannot create a directory with an empty name. That error is different from receiving no directory-name arguments at all; neither case prompts interactively for a name.

## 6. PATH and command lookup

`PATH` contains a **colon-separated list of directories**, not the commands themselves.

View it with:

```bash
printenv PATH
```

Example value:

```text
/home/aboud/bin:/usr/bin:/bin
```

When Bash searches `PATH` for an external command, it searches from left to right. If both `/home/aboud/bin` and `/usr/bin` contain an executable named `hello`, the earlier matching executable is found first.

Scope note: this describes external-command lookup. Shell functions and builtins also exist; investigating those is where we paused.

### Explicit paths

```bash
/usr/bin/hello  # Explicit absolute path; no PATH search
./hello        # Explicit relative path: hello in the current directory
```

A bare `hello` can fail while `./hello` works if the current directory is not in `PATH`. We practiced explaining this distinction.

## 7. Updating PATH while keeping existing directories

The following are assignment examples; the paths must refer to real directories containing executables to be useful on your machine.

### Add a directory at the beginning

```bash
PATH="/home/aboud/bin:$PATH"
```

If the old value was `/usr/bin:/bin`, the new value becomes:

```text
/home/aboud/bin:/usr/bin:/bin
```

Bash expands the old `$PATH` on the right before assigning the combined text back to `PATH`.

### Add a directory at the end

```bash
PATH="$PATH:/home/aboud/tools"
```

The existing directories remain first, so their matching executables are found before matching ones in the added directory.

### Replacing is different from adding

```bash
PATH="/home/aboud/bin"
```

This replaces the entire search list with that one directory. It does not automatically retain `/usr/bin` or `/bin`. Including `$PATH` explicitly is what carries the old list into the new assignment.

We have not yet covered making these changes persistent across new shell sessions.

## 8. What we discovered with type

You ran:

```bash
type cd
```

Fish reported that `cd` was a function and displayed its definition. Your description of that output was correct; the tutor had assumed Bash too early.

**Next session:** enter Bash and run `type cd` there. We have not yet examined that output or finished the distinction between functions, builtins, and external commands.

## 9. Progress and next steps

### Demonstrated during this session

- Distinguished literal single quotes from expanding double quotes.
- Used `cd "$folder"` independently for a directory containing a space.
- Identified left-to-right external-command lookup through `PATH`.
- Used absolute paths and `./hello`, and explained why a bare command may fail.
- Built a PATH value preserving existing directories after guided practice.

### Review next time

- Word splitting in unquoted variable expansions.
- One empty argument versus zero arguments.
- Assignment replacement versus using the old value in a new assignment.
- Constructing PATH updates without hints.

These are initial learning results, not yet spaced-retrieval mastery. We will review them in a later session before marking them mastered.

Permissions, service management, and the detailed redirection questions were calibration probes, not completed lessons.

## Official reference

[LPI LPIC-1 objectives, version 5.0](https://www.lpi.org/our-certifications/exam-101-102-objectives/)

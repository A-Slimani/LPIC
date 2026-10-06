# Syllabus: LPIC-1

This file is the agreed learning arc for the topic named above. The tutor drafted it, you shaped it, both sides respect it. Ticking items off happens during teaching; reshaping happens by re-entering `prepare-syllabus` mode.

Draft awaiting learner shaping and confirmation. These are coverage modules; teaching will break each into individual concepts. Source: https://www.lpi.org/our-certifications/exam-101-102-objectives/ (v5.0, read 2026-10-03). Prepare Exam 101 first, then Exam 102. Objective weights guide practice emphasis, not omissions.

## Goal

Pass exams 101-500 and 102-500 to earn LPIC-1 certification.

## Non-goals

Things this syllabus deliberately does NOT cover. Useful for containing scope creep.

- Proposed for confirmation: advanced administration beyond the published LPIC-1 objectives.

## Arc

Ordered list of concepts, from first to last. Items keep their number for the life of the syllabus — deferred or dropped items leave a numbered gap rather than being renumbered, so references in the Deviations log stay valid.

1. Command-line workflows (103.1–103.4, 103.7–103.8: Bash, files, filters, redirection, regex, vi) — in progress since 2026-10-03
2. File access (104.5–104.7: permissions, ownership, links, FHS) — pending
3. Process control (103.5–103.6: jobs, signals, monitoring, priorities) — pending
4. Boot lifecycle (101.1–101.3, 102.2, 102.6: hardware, boot, GRUB, systemd/SysVinit, guests) — pending
5. Storage administration (102.1, 104.1–104.3: layout, partitions, filesystems, integrity, mounts) — pending
6. Software packages (102.3–102.5: libraries, Debian tools, RPM/YUM/Zypper) — pending
7. Shell automation (105.1–105.2: startup files, environment, functions, scripts) — pending
8. Host administration (107.1–107.3, 108.1–108.2: accounts, scheduling, locales, time, logging) — pending
9. Host networking (109.1–109.4: protocols, addressing, persistent configuration, troubleshooting, DNS) — pending
10. Host security and user services (110.1–110.3, 106.1–106.3, 108.3–108.4: security, SSH/GPG, desktops, accessibility, mail, printing) — pending

## Deviations

Append-only log of sessions that strayed from the next-due arc item. Do not delete entries — the trail is what tells you whether the plan still fits reality or needs reshaping.

_(Empty.)_

- 2026-10-04: Symbolic-link target and dangling-link behavior (104.6) — brief explanation prompted by `cp -a` preserving links during 103.3 file-copy practice.
- 2026-10-05: Permissions, ownership and hard/symbolic links (104.5–104.7) — started during Arc item 1 file-copy/compression practice; item 1 remains in progress.

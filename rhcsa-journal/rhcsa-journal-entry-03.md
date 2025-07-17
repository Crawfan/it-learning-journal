# Journal Entry 03 - Shell History, Expansion, and Archiving

**Date:** 2025-07-09
**Focus Area:** RHCSA Shell Utilities & Archiving

---

##  Summary

Today's RHCSA lesson focused on **shell navigation**, **command history**, **shell expansion**,
**archiving**, and **file linking**.

---

##  Commands Reviewed

- `history`, `!n`, `!string`, `ctrl+r`, `ctrl+a/e/l/u`, `alt+f`, `alt+b`
- `touch file{1..9}` - brace expansion
- `ls *`, `ls a?`, `ls [a-z]*` - globbing
- `export VAR=value`, `alias`, `unalias`
- `source ~/.bash_profile`

---

## Archiving + Linking

- `tar czvf archive.tgz /etc /opt`
- `ln -s source target`
- `rm` to test what happens to soft links

---

## Metaphor

> “Globbing is like a filter for your file cabinet—`ls a*` says: ‘Show me every folder that starts with A.’ It keeps you from flipping through every single folder.”

---

## Lab Summary

- Archived `/etc` and `/opt`
- Created symbolic links to `/tmp`
- Deleted source files and observed link behavior

---

## Next Steps

- Practice `find` with complex filters
- Review `~/.bashrc` vs `~/.bash_profile` behavior
- Try customizing prompt and aliases for faster productivity

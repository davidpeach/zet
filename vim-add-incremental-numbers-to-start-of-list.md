# Vim add incremental numbers to start of list

2025-04-03 12:42:58

Visually select the list and use the following substitute command:

```bash
s/^/\=(line('.') - line("'<") + 1) . '. ' /
```

Can also pipe the selected text to `nl` external command

```bash
!nl -w 1 -s '. '
```

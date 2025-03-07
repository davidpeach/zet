# Bash script development with on-save live changes using entr

Thursday, 01 February 2024. 17:04:45GMT

- entr is a program that can be told to watch a set of files, and run a given command when any of those files changes.
- I can't believe I've never heard of this program until a few days ago.

## Basic usage

```bash
echo myscript | entr ./myscript
```

- install the `entr` package from your package manager of choice.
- open up a script file you want to work on.
- Assuming your script is called `myscript`
- in a separate terminal pane, run `echo myscript | entr ./myscript`.
    - This will tell `entr` to watch the myscript file and call that script whenever the file is updated.
- I use this in tmux and have a left-hand pane with the script im working on, and the right-hand pane with `entr` running.

## Running more that one command

You can run more than one command on file change by calling `sh` with the `-c` option and pass in the commands to run like below.
```bash
echo myscript | entr sh -c 'clear && ./myscript'
```

## Extra
- `man entr` locally after installing it.
- [entr man page on Arch Linux website](https://man.archlinux.org/man/community/entr/entr.1.en)

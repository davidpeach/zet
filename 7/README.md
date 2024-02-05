# Grep files and pass to vim

Monday, 05 February 2024. 10:11:59GMT

```bash
grep -rl todo ./app | xargs -o vim --
```

This example will recursively (`-r`) search the `./app` directory for the word "todo".

The `-l` flag tells grep to just list out the file names that contain a match.

I then pipe it `|` to `xargs`, which is a way to pass output of a previous command into the 
input of the next command. So it takes the list of grepped file into `vim` in this case.

The `-o` basically helps when passing to an interactive application, such as vim.

From the `xargs` man page:

> -o, --open-tty
    Reopen stdin as /dev/tty in the child process  before  executing  the
    command.   This is useful if you want xargs to run an interactive application.

One `vim` is opened with the files passed as arguments, vim has those files in its `argslist`.

I can then use `:argdo` to run a command over every file in the arglist.

```bash
:argdo %s/TODO/DONE/g
```

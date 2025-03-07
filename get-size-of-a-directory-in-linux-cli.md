# Get size of a directory in linux cli

Wednesday, 21 February 2024. 12:28:49GMT

## Total size of directory given

```bash
du -sh /path/to/dir
# OR
sudo du -sh /path/to/dir
```

## Total size of directories one level deep

```bash
du -h --max-depth=1 /path/to/dir
# OR
sudo du -h  --max-depth=1 /path/to/dir
```

- **-s** Display only total size.
- **-h** Display size in human-readable format.

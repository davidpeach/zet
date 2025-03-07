# Setting up s3cmd to backup s3-compliant bucket data

Tuesday, 05 November 2024. 12:07:34GMT

Install
```bash
sudo pacman -Syu s3cmd
```

Configure.
Will need:

- s3 access key
- s3 access secret
- default region (ams3)
- s3 endpoint (ams3.digitaloceanspaces.com)
- dns-style (%(bucket)s.nyc3.digitaloceanspaces.com)
- encryption password
- Use HTTPS protocol (yes)
- HTTP Proxy server name : leave blank

```bash
s3cmd --configure
```

The generated config will be store in plain text at `~/.s3cfg`

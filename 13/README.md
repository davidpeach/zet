# Limiting host cpu usage from docker compose

Tuesday, 12 November 2024. 15:22:24GMT

Docker containers can sometimes go crazy if you don't limit the resources that they can access on the host machine.

I had this issue recently and so found a line to add to the compose yml file to limit the resources - cpus in this case - that the container could get access to.

The example below will limit the container that is created to only access 0.4 cpus (40% of one cpu I think - need to verify that).

```yaml
services:
    my-service:
        # other compose key value pairs
        cpus: 0.4
        # other compose key value pairs
```

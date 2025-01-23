### Removing Images Older Than 30 days
---

To remove unused Docker images that are older than 30 days, use the following command:

`docker image prune -a --filter "until=720h"`

- `-a`: remove both unused and dangling images
- `--filter "until=720h"`: remove images older than 720 hours (30 days)
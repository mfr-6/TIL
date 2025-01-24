### What is dangling image in Docker?
---

Dangling Image is an untagged image that isn't referenced by any container.

This happens when image lost its association with any tagged image. An example of this case is building a new image with the same tag as an existing image.

Dangling images have no tag and it's shown as `<none>:<none>`

```
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
<none>       <none>    dacb7133d988   13 days ago   1.54GB
```
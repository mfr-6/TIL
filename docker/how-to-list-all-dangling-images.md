### How to list all Dangling Images in Docker?
---

To show the list of dangling images, use the following command:

`docker image ls -f ”dangling=true”`

```bash
x ~ % docker images -f "dangling=true"
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
<none>       <none>    dacb7133d988   13 days ago   1.54GB
<none>       <none>    f764ebe566c7   13 days ago   1.78GB
<none>       <none>    2a8b1c6030aa   13 days ago   1.78GB
<none>       <none>    de3e62435baf   3 weeks ago   1.54GB
```

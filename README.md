# docker-boinc

## Berkeley Open Infrastructure for Network Computing

Running `Seti@Home` client software in a docker container.

Used Apline linux to create a small client container.

Run `boinc_client` using `docker run`:

```
docker run --name seti -d kayvan/boinc \
  --attach_project http://setiathome.berkeley.edu YOUR_ACCOUNT_KEY
```

Later, if you want to finish the jobs and kill the container gracefully,
you can use the `boinccmd` tool to tell the BOINC client to not request more
work from the project and to check the current running tasks till they
are completed:

```
$ docker exec -it seti bash
bash-4.3# boinccmd --project http://setiathome.berkeley.edu nomorework
bash-4.3# boinccmd --get_tasks
[...]
```

## Reference

* http://setiathome.ssl.berkeley.edu
* https://boinc.berkeley.edu
* https://www.alpinelinux.org
* https://boinc.berkeley.edu/wiki/Boinccmd_tool

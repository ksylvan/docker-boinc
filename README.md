# docker-boinc

## Berkeley Open Infrastructure for Network Computing

Running `Seti@Home` client software in a docker container.

Used Apline linux to create a small client container.

Run `boinc_client` using `docker run`

```
docker run -d kayvan/boinc --attach_project http://setiathome.berkeley.edu YOUR_ACCOUNT_KEY
```

## Reference

* http://setiathome.ssl.berkeley.edu
* https://boinc.berkeley.edu
* https://www.alpinelinux.org

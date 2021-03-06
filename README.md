# Supported tags and respective `Dockerfile` links

-	[`latest` (*Dockerfile*)](https://github.com/adagio211/docker-nginx-webdav/blob/master/Dockerfile)


# How to use this image

```console
$ docker run --name webdav -p 80:80 -v /webdav:/webdav -d adagio211/webdav
```
This will start a webdav server listening on the default port of 80.
Then access it via `http://localhost:80` or `http://host:80` in a browser.

This server will serve files located in your /webdav folder and config the nginx `create_full_put_path  on`

Image's supported volumes:
- `/webdav` - served directory

To restrict access to only authorized users, you can define two environment variables: `USERNAME` and `PASSWORD`
```console
$ docker run --name webdav -p 80:80 -v /webdav:/webdav -e USERNAME=webdav -e PASSWORD=webdav -d adagio211/webdav
```

# Supported Docker versions

This image is officially supported on Docker version 1.10.2.
Support for older versions (down to 1.6) is provided on a best-effort basis.
Please see [the Docker installation documentation](https://docs.docker.com/installation/) for details on how to upgrade your Docker daemon.

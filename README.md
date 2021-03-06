This is boilerplate for [docker-sync](https://github.com/EugenMayer/docker_sync).
Either as a starting point for your configuration or to try out what docker-sync offers in terms of performance and the toolchain in practical.

If you have issue, create a issue at [docker-sync](https://github.com/EugenMayer/docker_sync)

**Start with**

 1) Install docker-sync, if you did not yet

```
gem install docker-sync
```

 2) Now get the boilerplate
```
git clone https://github.com/EugenMayer/docker-sync-boilerplate
cd docker-sync-boilerplate
```

 3) Now start the sync, first choose the boilerplate either simplest, unison, unison_dualside, rsync, or even advanced. See [strategies](https://github.com/EugenMayer/docker-sync/wiki/8.-Strategies) to understand the important differences

---

## Examples

For example rsync
```
cd rsync
docker-sync-stack start
```
This will start the sync, and start your app-stack defined by in the docker-compose file. All in one step

---

If you wonder, how you would keep the docker-compose.yml portable, see splitted-compose. The changes for docker-sync are incorporated into an overaly-docker-compose file
In this case you do:

```
cd splitted-compose
docker-sync start

<open a new shell>

cd splitted-compose
docker-compose -f docker-compose.yml -f docker-compose-dev.yml up
```

More about this in [the wiki](https://github.com/EugenMayer/docker-sync/wiki/Keep-you-docker-compose.yml-portable)

---

For example dynamic-configuration-dotnev you will need to copy `.env.dist` to
`.env`

```
cd dynamic-configuration-dotnev
cp .env.dist .env
```

And after that start things as described above


## Reference

If you want to know, what options you actually have, see the [configuration-reference](https://github.com/EugenMayer/docker-sync/wiki/2.-Configuration#docker-syncyml)

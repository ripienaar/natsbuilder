## NATS Builder

This creates basic NATS Clusters for Docker Compose.

It requires you to have [AppBuilder 0.7.3](https://choria-io.github.io/appbuilder/) or newer.

## Creating Networks

To create a network with 3 clusters and 3 nodes each in the `3x3` directory run:

```
$ abt generate 3x3 --clusters 3 --members 3
```

This will create all the needed compose files, config files and more.

Start it with `docker compose up`.

Once running use `abt shell` to access the user account, the shell has numerous `nats` contexts setup, see `nats ctx 
ls`.

Multiple networks can be run at the same time by adjusting the base port used for allocation client ports using
`--port`.

If you wish to run a Nightly build of NATS Server create the network like this while fixing the date stamp in the image:

```
$ abt generate 3x3 --image synadia/nats-server:nightly-20230906 --config-path /nats/conf/nats-server.conf
```

## Contact

Chat with `ripienaar` on the NATS slack.

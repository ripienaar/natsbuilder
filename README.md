## NATS Builder

This creates basic NATS Clusters for Docker Compose.

It requires you to have [AppBuilder 0.7.2](https://choria-io.github.io/appbuilder/) or newer.

## Creating Networks

To create a network with 3 clusters and 3 nodes each in the `3x3` directory run:

```
$ abt generate 3x3 --clusters 3 --members 3
```

This will create all the needed compose files, config files and more.

Start it with `docker compose up`.

Once running use `abt shell 1 2` to access the user account connect to server 1 in cluster 2.  Pass `--system` to access
the System account.

Multiple networks can be run at the same time by adjusting the base port used for allocation client ports using 
`--port`.

## Contact

Chat with `ripienaar` on the NATS slack.
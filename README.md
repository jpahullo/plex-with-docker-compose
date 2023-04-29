# [Plex](https://www.plex.tv/) with [docker-compose](https://docs.docker.com/compose/)

This is the skeleton to run your Plex server into your computer.

## Prerequisites

You must have `docker` and `docker-compose` installed. Follow official
documentation to install them on your computer.

## How to start

Clone this repository:

```
git clone https://github.com/jpahullo/plex-with-docker-compose.git plex
cd plex/docker
./bin/start-plex
```

This will start your own Plex server.

## Populate with your content.

Put into directory `data/` all your movies, music, whatever you want
to play with Plex.

Just as an example, at the moment of updating this README, I have this
directory structure more or less:

```shell
├── movies
│   ├── 3D-spanish
│   ├── children-spanish
│   ├── english
│   └── spanish
├── music
├── transcode
└── tvshows
    ├── english
    └── spanish
```

## Start your plex easily

You need to have the `bin/` into your PATH. To do so, I recommend this way:

* Update your `.bashrc` or similar to include this directory into your 
PATH, something like `PATH=$PATH:/path/to/plex/bin`.

There is no worry if the unit where you placed the plex server is located
into an external hard disk, it will only run whenever connected.

## Advantages

1. No dependencies on your computer, just docker and docker-compose.
1. Easy installing on every hard disk, even on an external unit.
    * You can have the configuration and all the media on the external hard
      disk, as I do. 

## Disadvantages

1. By default, you have the docker related stuff of the Plex server still on your computer,
into /var/lib/docker, as usual. However, you can set up this directory out of
your main hard disk if you want to.

## Thanks

Thanks to [linuxserver.io](https://github.com/linuxserver) for maintaining such
a bunch of docker images to use everywhere, even at **home**.

## Author

Jordi

## License

GPL v3

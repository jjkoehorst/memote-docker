# memote – the genome-scale metabolic model test suite

Easily run the memote command line tools from a docker container. You can find the main documentation on [readthedocs](https://memote.readthedocs.io/).

## Installation

We aim to release containers for every memote release from version 0.4.5 onwards. You can thus use a specific version tag or simply 'latest'.

```bash
docker pull opencobra/memote:latest
```

## Usage

The container exposes the memote command line tool directly. If you run the container without any arguments you will see the base help message.

```bash
docker run opencobra/memote
```

**We may work on allowing you to pipe the model to the docker container. So in future you would be able to do the following:**

```bash
my-model.xml > docker run opencobra/memote run
```

However, you would still not be able to easily access output files. For now the best way is to mount a local directory into the container. The only hurdle is that you may have to afterwards change the owner from `root` to your own user.

```bash
docker run -v ~/local/path/to/models/directory:/opt opencobra/memote run /opt/my-model.xml
```

## Contact

For comments and questions get in touch via

-   our [gitter chatroom](https://gitter.im/opencobra/memote)
-   or our [mailing list](https://groups.google.com/forum/#!forum/memote).

Are you excited about this project? Consider [contributing](https://memote.readthedocs.io/en/latest/contributing.html) by adding novel tests, reporting or fixing bugs, and generally help us make this a better software for everyone.

## Copyright

-   Copyright (c) 2017, Novo Nordisk Foundation Center for Biosustainability, Technical University of Denmark.
-   Free software: [Apache Software License 2.0](LICENSE)


# Rock Docker

This repository contains the docker image for [Rock](https://github.com/vknabel/Rock)

The Rock Docker comes preinstalled with the latest [Rock](https://github.com/vknabel/Rock) and Swift 3 Version of [kylef/swiftenv-docker](https://github.com/kylef/swiftenv-docker).

## Usage

Create your own Dockerfile containing

```dockerfile
FROM vknabel/rock

# Sets the path to your project
RUN mkdir -p /code
WORKDIR /code
ADD . /code

# You can install your dependencies like so
RUN rock install

# You can install your Swift Version using
# RUN swiftenv install
```

Then, if you want to build your project run.

```bash
$ docker build -t your-project .
```

## License

Rock is available under the [MIT](LICENSE) license.

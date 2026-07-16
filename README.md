# Node.js for LoongArch (loong64)

<p align="center"><a href="README.md">English</a> | <a href="README-zh.md">中文</a></p>

[Node.js](https://nodejs.org/) Docker container images ported to the **LoongArch (loong64)** architecture.

This repository builds and publishes Node.js container images for LoongArch based on the upstream
[nodejs/unofficial-builds](https://github.com/nodejs/unofficial-builds).

## Docker Images

Images are published to Docker Hub under
[`kubernetesloong64/node-loong64`](https://hub.docker.com/r/kubernetesloong64/node-loong64).

- [![kubernetesloong64/node-loong64](https://img.shields.io/docker/v/kubernetesloong64/node-loong64/v20.20.2-debian?arch=loong64&logo=docker&label=kubernetesloong64%2Fnode-loong64&sort=semver)](https://hub.docker.com/r/kubernetesloong64/node-loong64/tags)
- [![kubernetesloong64/node-loong64](https://img.shields.io/docker/v/kubernetesloong64/node-loong64/v22.23.1-debian?arch=loong64&logo=docker&label=kubernetesloong64%2Fnode-loong64&sort=semver)](https://hub.docker.com/r/kubernetesloong64/node-loong64/tags)
- [![kubernetesloong64/node-loong64](https://img.shields.io/docker/v/kubernetesloong64/node-loong64/v24.18.0-debian?arch=loong64&logo=docker&label=kubernetesloong64%2Fnode-loong64&sort=semver)](https://hub.docker.com/r/kubernetesloong64/node-loong64/tags)
- [![kubernetesloong64/node-loong64](https://img.shields.io/docker/v/kubernetesloong64/node-loong64/v26.5.0-debian?arch=loong64&logo=docker&label=kubernetesloong64%2Fnode-loong64&sort=semver)](https://hub.docker.com/r/kubernetesloong64/node-loong64/tags)

Three base image variants are provided per version:

- **anolis** — based on `openanolis/anolisos:23.4`
- **debian** — based on `lcr.loongnix.cn/debian:14`
- **debian-slim** — based on `lcr.loongnix.cn/debian:14-slim`

### Pull Images

```shell
docker pull kubernetesloong64/node-loong64:v20.20.2-anolis
docker pull kubernetesloong64/node-loong64:v20.20.2-debian
docker pull kubernetesloong64/node-loong64:v20.20.2-debian-slim

docker pull kubernetesloong64/node-loong64:v22.23.1-anolis
docker pull kubernetesloong64/node-loong64:v22.23.1-debian
docker pull kubernetesloong64/node-loong64:v22.23.1-debian-slim

docker pull kubernetesloong64/node-loong64:v24.18.0-anolis
docker pull kubernetesloong64/node-loong64:v24.18.0-debian
docker pull kubernetesloong64/node-loong64:v24.18.0-debian-slim

docker pull kubernetesloong64/node-loong64:v26.5.0-anolis
docker pull kubernetesloong64/node-loong64:v26.5.0-debian
docker pull kubernetesloong64/node-loong64:v26.5.0-debian-slim
```

## Verifying releases

- Releases are signed with GPG.
- Download the public key from [keys.openpgp.org](https://keys.openpgp.org).
- Fingerprint: [FCF8724722CCBF9F51B1FBE376532BE7E3013105](https://keys.openpgp.org/debug?q=FCF8724722CCBF9F51B1FBE376532BE7E3013105)
- [Manual download](https://keys.openpgp.org/vks/v1/by-fingerprint/FCF8724722CCBF9F51B1FBE376532BE7E3013105)

```shell
gpg --keyserver keys.openpgp.org --recv-keys FCF8724722CCBF9F51B1FBE376532BE7E3013105
echo "FCF8724722CCBF9F51B1FBE376532BE7E3013105:6:" | gpg --import-ownertrust
```

Or download the key file manually and import it:

```shell
gpg --import /tmp/xxx
```

## License

[Apache License 2.0](LICENSE)

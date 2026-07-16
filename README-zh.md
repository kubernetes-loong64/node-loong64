# Node.js for LoongArch (loong64)

<p align="center"><a href="README.md">English</a> | <a href="README-zh.md">中文</a></p>

将 [Node.js](https://nodejs.org/) Docker 容器镜像移植到 **LoongArch (loong64)** 架构。

本仓库基于上游 [nodejs/unofficial-builds](https://github.com/nodejs/unofficial-builds)，构建并发布适用于 LoongArch 的 Node.js 容器镜像。

## Docker 镜像

镜像发布在 Docker Hub 上的
[`kubernetesloong64/node-loong64`](https://hub.docker.com/r/kubernetesloong64/node-loong64)。

- [![kubernetesloong64/node-loong64](https://img.shields.io/docker/v/kubernetesloong64/node-loong64/v20.20.2-debian?arch=loong64&logo=docker&label=kubernetesloong64%2Fnode-loong64&sort=semver)](https://hub.docker.com/r/kubernetesloong64/node-loong64/tags)
- [![kubernetesloong64/node-loong64](https://img.shields.io/docker/v/kubernetesloong64/node-loong64/v22.23.1-debian?arch=loong64&logo=docker&label=kubernetesloong64%2Fnode-loong64&sort=semver)](https://hub.docker.com/r/kubernetesloong64/node-loong64/tags)
- [![kubernetesloong64/node-loong64](https://img.shields.io/docker/v/kubernetesloong64/node-loong64/v24.18.0-debian?arch=loong64&logo=docker&label=kubernetesloong64%2Fnode-loong64&sort=semver)](https://hub.docker.com/r/kubernetesloong64/node-loong64/tags)
- [![kubernetesloong64/node-loong64](https://img.shields.io/docker/v/kubernetesloong64/node-loong64/v26.5.0-debian?arch=loong64&logo=docker&label=kubernetesloong64%2Fnode-loong64&sort=semver)](https://hub.docker.com/r/kubernetesloong64/node-loong64/tags)

每个版本提供三种基础镜像变体：

- **anolis** — 基于 `openanolis/anolisos:23.4`
- **debian** — 基于 `lcr.loongnix.cn/debian:14`
- **debian-slim** — 基于 `lcr.loongnix.cn/debian:14-slim`

### 拉取镜像

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

## 验证发布

- 发布文件使用 GPG 签名。
- 从 [keys.openpgp.org](https://keys.openpgp.org) 下载公钥。
- 指纹：[FCF8724722CCBF9F51B1FBE376532BE7E3013105](https://keys.openpgp.org/debug?q=FCF8724722CCBF9F51B1FBE376532BE7E3013105)
- [手动下载](https://keys.openpgp.org/vks/v1/by-fingerprint/FCF8724722CCBF9F51B1FBE376532BE7E3013105)

```shell
gpg --keyserver keys.openpgp.org --recv-keys FCF8724722CCBF9F51B1FBE376532BE7E3013105
echo "FCF8724722CCBF9F51B1FBE376532BE7E3013105:6:" | gpg --import-ownertrust
```

或者，手动下载公钥文件后导入：

```shell
gpg --import /tmp/xxx
```

## 许可证

[Apache License 2.0](LICENSE)

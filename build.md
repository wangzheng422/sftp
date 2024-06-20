# build steps for sftp

```bash

cd /data

git clone https://github.com/wangzheng422/sftp

cd sftp

git checkout wzh

podman build -t quay.io/wangzheng422/imgs/sftp:2024.06.20 -f Dockerfile.rocky9 ./


```
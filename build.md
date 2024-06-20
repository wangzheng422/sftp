# build steps for sftp

```bash

cd /data

git clone https://github.com/wangzheng422/sftp

cd sftp

git checkout wzh

podman build -t quay.io/wangzheng422/imgs/sftp:rockey9-2024.06.20 -f Dockerfile.rocky9 ./

podman push quay.io/wangzheng422/imgs/sftp:rockey9-2024.06.20

# test locally
podman run --privileged  --name sftp -p 2222:22 -d quay.io/wangzheng422/imgs/sftp:2024.06.20 foo:pass:::upload


```

# ubi9

```bash

podman build -t quay.io/wangzheng422/imgs/sftp:ubi9-2024.06.20 -f Dockerfile.ubi9 ./

```
# build steps for sftp

```bash

cd /data

git clone https://github.com/wangzheng422/sftp

cd sftp

git checkout wzh

podman build -t quay.io/wangzheng422/qimgs/sftp:rockey9-2024.06.20 -f Dockerfile.rocky9 ./

podman push quay.io/wangzheng422/qimgs/sftp:rockey9-2024.06.20

# test locally
podman run --privileged  --name sftp -p 2222:22 -d quay.io/wangzheng422/qimgs/sftp:rockey9-2024.06.20 foo:pass:::upload


```

# ubi9

To build base on ubi9, we need a rhel os as builder host os.

```bash

podman build -t quay.io/wangzheng422/qimgs/sftp:ubi9-2024.06.20 -f Dockerfile.ubi9 ./

podman push quay.io/wangzheng422/qimgs/sftp:ubi9-2024.06.20

# test locally
podman run --privileged  --name sftp -p 2222:22 -d quay.io/wangzheng422/qimgs/sftp:ubi9-2024.06.20 foo:pass:::upload

```
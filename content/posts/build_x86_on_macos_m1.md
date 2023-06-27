---
title: "Build x86 on mac os m1"
date: 2023-06-27
draft: false
description: ""
---
```brew install colima docker```  
```colima start --arch x86_64```   

```
#!/bin/bash

ARCH=arm64
VERSION=v0.10.4
curl -LO https://github.com/docker/buildx/releases/download/${VERSION}/buildx-${VERSION}.darwin-${ARCH}
mkdir -p ~/.docker/cli-plugins
mv buildx-${VERSION}.darwin-${ARCH} ~/.docker/cli-plugins/docker-buildx
chmod +x ~/.docker/cli-plugins/docker-buildx
docker buildx version
```
source: https://dev.to/luizkowalski/how-to-migrate-from-docker-desktop-to-colima-on-a-mac-m1-48ae   
```docker buildx build . -f ubuntu.Dockerfile -t sw:86 --output type=docker```  

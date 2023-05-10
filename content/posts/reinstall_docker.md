---
title: "reinstall docker on mac m1"
date: 2023-05-10
draft: false
description: "cannot connect to the Docker daemon"
---
Fix:
uninstall Docker app (brew uninstall docker).  

https://github.com/docker/for-mac/issues/6683#issuecomment-1383403011  
```
rm -rf ~/Library/Group\ Containers/group.com.docker
rm -rf ~/Library/Containers/com.docker.docker
rm -rf ~/.docker
rm -rf ~/Library/Application\ Support/com.docker.docker
rm -rf ~/Library/Application\ Support/Docker\ Desktop
```
Install new version.  
```brew install homebrew/cask/docker``` 

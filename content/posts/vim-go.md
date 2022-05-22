---
title: "install vim-go to neovim"
date: 2022-05-20
draft: false
description: "vim-go install to neovim github.com/fatih/vim-go"
---
# vim-go install to neovim github.com/fatih/vim-go

```
https://github.com/fatih/vim-go
For nvim - vim-plug
    Plug 'fatih/vim-go', { 'do': ':GoUpdateBinaries' }
```
Need to check $PATH

Tip: for start plugin work - change file extention to .go

```
Error message "go: go.mod file not found in current directory or any parent directory; see 'go help modules'"
source: https://stackoverflow.com/q/66894200

regulate
go mod init # <file> 
or manually:
go env -w GO111MODULE=off
```


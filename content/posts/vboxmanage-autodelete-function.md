---
title: "vboxmanage script"
---
# vboxmanage script for stop & delete related resources

```
function killvms() {   VBoxManage list runningvms | awk '{print $2;}' | xargs -I vmid VBoxManage controlvm vmid poweroff;   VBoxManage list vms | awk '{print $2;}' | xargs -I vmid VBoxManage unregistervm --delete vmid; }
```
killvms provide cleaning all running vms and power off them.

Use after vagrant halt or similar things.

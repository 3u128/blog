---
title: "hashicorp gpg key problem"
date: 2023-04-10
draft: false
description: "The following signatures couldn't be verified because the public key is not available"
---
```
Err:6 https://apt.releases.hashicorp.com focal InRelease
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY AA16FCBCA621E701
~
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: https://apt.releases.hashicorp.com focal InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY AA16FCBCA621E701
W: Failed to fetch https://apt.releases.hashicorp.com/dists/focal/InRelease  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY AA16FCBCA621E701
W: Some index files failed to download. They have been ignored, or old ones used instead.
```

Fix: https://github.com/hashicorp/terraform/issues/32622#issuecomment-1498838107  

```
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo gpg --yes --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list > /dev/null
```

OR/AND try check chmod:  
```
chmod 644 /usr/share/keyrings/hashicorp-archive-keyring.gpg
```

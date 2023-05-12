# 1Password Connect & Operator

## Manual Steps

The 1password-credentials.json needs to manually be manually applide to the Cluster at first:

```sh
kubectl create secret generic op-credentials --from-file=1password-credentials.json=./1password-credentials.json
```
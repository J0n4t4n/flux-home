# 1Password Connect & Operator

## Manual Steps

The 1password-credentials.json needs to manually be manually applide to the Cluster at first:

```sh
cat 1password-credentials.json | base64 | \
  tr '/+' '_-' | tr -d '=' | tr -d '\n' > op-session

kubectl create secret generic op-credentials --from-file=1password-credentials.json=op-session

kubectl create secret generic onepassword-token --from-literal=token=<OP_CONNECT_TOKEN>"
```
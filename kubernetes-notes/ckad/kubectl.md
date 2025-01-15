# `kubectl`

- [Quick reference guide](https://kubernetes.io/docs/reference/kubectl/quick-reference/)

## Useful `kubectl` shortcuts

| shortcut | command |
|----------|---------|
| `rs` | `replicaset` |
| `po` | `pod` |
| `deploy` | `deployment` |
| `svc` | `service` |
| `ns` | `namespace` |
| `no` | `node` |

## Create YAML manifests quickly

- `--dry-run=client` will not create the resource, but it will print the object that would be sent to the server.
- `-o yaml` will output the resource in YAML format.

You can use these two options together to generate a YAML file for a resource without creating it:

```bash
kubectl run nginx --image=nginx --dry-run=client -o yaml > pod-definition.yaml
```

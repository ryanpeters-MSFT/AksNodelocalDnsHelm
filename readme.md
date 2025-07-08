# Nodelocal DNS (Helm)

## Commands

```powershell
# generate dry run (from node-local-dns folder)
helm upgrade --install nodelocaldns . --namespace kube-system --dry-run=client  > ..\helm-dryrun.yaml

# run a sample nslookup on a test pod
kubectl run dns-check --image=busybox -i --restart=Never --rm --quiet -- sh -c 'nslookup azure-policy-webhook-service.kube-system.svc.cluster.local'
```
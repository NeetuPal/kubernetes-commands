# minikube-commands
```
minikube version

```
```
minikube status

```
```
minikube start --driver=docker
```
```
minikube start
```
```
minikube delete --all --purge
```
```
minikube start --driver=virtualbox --memory=2500mb --cpus=2
```
# Add VirtualBox to Git Bash PATH
```
nano ~/.bashrc
```
```
notepad ~/.bashrc
```
```
export PATH=$PATH:/d/virtual-box

```
```
source ~/.bashrc

```
```
VBoxManage --version
```
STEP 2 — Disable Hyper-V, WSL2, Memory Integrity

VirtualBox cannot run if these are ON.

Run this in PowerShell (ADMIN):
```
bcdedit /set hypervisorlaunchtype off
```

Disable Windows features:
```
Disable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-All
Disable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
Disable-WindowsOptionalFeature -Online -FeatureName Windows-Subsystem-Linux
```

Restart the system.

```
kubectl delete namespace webapps --force --grace-period=0

```
```
helm search repo vault

```
```
helm install vault hashicorp/vault -n vault --create-namespace -f values.yaml

```

```
helm upgrade vault hashicorp/vault -n vault -f values.yaml

```
```
kubectl logs vault-0 -n vault

```
```
kubectl describe pod bankapp-697b5f7bbd-2p545 -n webapps
```
```
kubectl logs pod/bankapp-697b5f7bbd-2p545 -n webapps -c vault-agent-init
```

```
kubectl exec -it vault-0 -n vault -- vault status

```
```
helm list -A

```
```
helm uninstall vault -n vault 2>/dev/null
```
```
kubectl delete namespace vault 2>/dev/null
```
```
kubectl exec -n vault -it vault-0 -- vault read auth/kubernetes/role/vault-role

```
# open docker desktop on mac
```
open /Applications/Docker.app
```
```
kind get clusters

```
```
kubectl cluster-info

```
```
kubectl logs -n webapps mysql-f758f45f5-vnh46 -c vault-agent-init

```
```
kubectl get nodes -o wide

```
```
TOKEN=$(kubectl -n webapps create token vault-auth)

```
```
kubectl get deploy -n webapps

```
```
kubectl rollout restart deployment bankapp -n webapps

```
```
kubectl describe deploy bankapp -n webapps

```
```
kubectl run temp --image=neet95402927/bankapp1:v161 -n webapps --rm -it -- /bin/sh

```
```
kubectl get sa vault-auth -n webapps -o yaml

```
```
kubectl patch sa vault-auth -n webapps -p '{"automountServiceAccountToken":true}'

```
```
kubectl get events -n webapps --sort-by=.metadata.creationTimestamp

```
```
kubectl exec -n vault -it vault-0 -- vault auth list

```

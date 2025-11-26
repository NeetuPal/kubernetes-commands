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

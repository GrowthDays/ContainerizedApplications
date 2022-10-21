# Kubernetes

## Install Minikube

Install:

```bash
$ wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
$ sudo cp minikube-linux-amd64 /usr/local/bin/minikube
$ sudo chmod 755 /usr/local/bin/minikube
```

Verify:
```bash
$ minikube version
```

You should see something like this:

```
minikube version: v1.27.0
commit: 4243041b7a72319b9be7842a7d34b6767bbdac2b
```

---

## Install Kubectl

```bash
$ LATEST_STABLE="$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)"
$ curl -LO "https://storage.googleapis.com/kubernetes-release/release/${LATEST_STABLE}/bin/linux/amd64/kubectl"
$ chmod +x kubectl
$ sudo mv kubectl /usr/local/bin/
```

Verify:

```bash
$ kubectl version -o yaml
```

Output:
```
clientVersion:
  buildDate: "2022-09-21T14:33:49Z"
  compiler: gc
  gitCommit: 5835544ca568b757a8ecae5c153f317e5736700e
  gitTreeState: clean
  gitVersion: v1.25.2
  goVersion: go1.19.1
  major: "1"
  minor: "25"
  platform: linux/amd64
kustomizeVersion: v4.5.7
serverVersion:
  buildDate: "2022-08-23T17:38:15Z"
  compiler: gc
  gitCommit: a866cbe2e5bbaa01cfd5e969aa3e033f3282a8a2
  gitTreeState: clean
  gitVersion: v1.25.0
  goVersion: go1.19
  major: "1"
  minor: "25"
  platform: linux/amd64

```

## Start Minikube

```bash
$ minikube start --driver=docker
```

Verify

```bash
$ minikube status
```

Output:

```
minikube
type: Control Plane
host: Running
kubelet: Running
apiserver: Running
kubeconfig: Configured
```

---

```bash
$ kubectl cluster-info
```
Output:

```
Kubernetes control plane is running at https://192.168.49.2:8443
CoreDNS is running at https://192.168.49.2:8443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy

To further debug and diagnose cluster problems, use 'kubectl cluster-info dump'.
```

---

```bash
$ kubectl get nodes
```

Output:

```
NAME       STATUS   ROLES           AGE   VERSION
minikube   Ready    control-plane   13m   v1.25.0
```

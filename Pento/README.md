# [Pento Broken Server](https://kodekloud.com/lessons/pento/)

- Let's take a tour of [Solution Video](https://kodekloud.com/lessons/2-solution-troubleshooting-nodes-and-deploying-file-server/).


> Note: -

1. At location of `/etc/kubernetes/manifests`, in `kube-apiserver.yaml` client ca file name is wrong. Fix it with correct name.
2. After fixing the `kube-apiserver.yaml` file, move to the path of `/root/.kube/`, as per description match the name of `user` and `api-server` port number.
3. After cluster up, do `kubectl get nodes` to check the status of nodes.
4. Second node is not set to schedule Pods. Fix it with certain command.

```
$ kubectl uncordon node01
```
5. Check the CoreDNS Pods in the `kube-system` namespace.
6. Edit the CoreDNS deployment manifest file and update image name as per description. Run the following commands:-

```

$ kubectl edit deploy coredns -n kube-system

$ kubectl get deploy coredns -n kube-system

$ kubectl get pods -n kube-system
```

7. Now cluster in configured to perform the following tasks. 


# Install kubernetes K8s Ubuntu LTS 20.04

I created three virtual machines Ubuntu 20.04 LTS (8 Gb RAM) 

>To run the Playbook for all the nodes
```
ansible-playbook -i v2Inventory v2Kubernetes.yaml -u antonio  -K
```

>and finally only in the master node

```
ansible-playbook -i v2Inventory master.yaml -u antonio  -K

```
```
kubeadm init --pod-network-cidr=10.244.0.0/16
```

```
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config
```

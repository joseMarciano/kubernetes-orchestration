# Daemonset

A Daemonset is a resource that ensures that all NODES have a specific copy of a pod running. When new NODES are added in cluster, 
the DaemonSet ensures automatically that the pods will be running inside the new NODES;
The main purpose is ensure certain tasks will be running in a NODE like: Logging services, Monitoring Services

## DaemonSet on Specific Nodes

The default behavior of DaemonSet is to create one pod by node.
But you can change this setting what node do you want the pod run using `Node Labels`
OBS:
- If you are using minikube. Use `minikube node add` to add new nodes and see the pods creation
- Node with labels: `kubectl get nodes --show-labels`
- Create label on specific node: `kubectl label nodes [node-name] [label-key=label-value Ex: disktye=ssd]`
- Show if label was created: `kubectl get nodes --show-labels | grep disktype=ssd`
- To confirm pod by node: `kubectl get pods -o wide --field-select spec.nodeName=minikube-m03`

## DaemonSet on Specific Nodes without labels(Direct attribution)
You can change de dafault behavior of daemonset and set the nodename instead of labels.

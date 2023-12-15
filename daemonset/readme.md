A Daemonset is a resource that ensures that all NODES have a specific copy of a pod running. When new NODES are added in cluster, 
the DaemonSet ensures automatically that the pods will be running inside the new NODES;
The main purpose is ensure certain tasks will be running in a NODE like: Logging services, Monitoring Services


If you are using minikube. Use `minikube node add` to add new nodes and see the pods creation
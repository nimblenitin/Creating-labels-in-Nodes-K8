# Creating-labels-in-Nodes-K8
Labels can be added to Nodes to rollout pods specific to Nodes.

Simple example to add Label to node and create Pod in that specific node with use of Label.

Steps followed:

*As Root*
```
1. Add Label to Node after finding the Node name.
$ kubectl get nodes 
$ kubectl label nodes <nodename> site=india

2. Create the Pod by using YAML with Node selection mentioned
$ kubectl apply -f node-specific-pod --record

3. Check whether the Pod was created in the correct Node with corresponding Label
$ kubectl get pods -o wide

```
*As Root*

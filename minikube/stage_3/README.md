# Create namespace form manifest 
kubectl apply -f namespace.yaml 

# Applying manifests to create pods
kubectl apply -f pod-red.yaml
kubectl apply -f pod-blue.yaml

# Associate pods to namespace
kubectl apply -f service.yaml 
kubectl apply -f service.yaml -n <name of your namespace>

# To see pods in namespace
kubectl get po -n <name of touyr namespace>

# You can also see the description of enpoints
kubectl -n production describe endpoints
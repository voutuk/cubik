# cubik

`minikube start --cpus=4 --memory=7gb --disk-size=30gb`
`kubectl get nodes`
`kybectl get pods`
`kubectl get componentsinfo`
`kubectl cluster-info`
`kubectl run site2 --image=ubuntu/apache2 --port=80`
`kubectl port-forward site2 8090:80`  (internet:machile)
`nano port-forward.yaml`
``` bash
apiVersion: v1
kind: Service
metadata:
  name: port-forwarding-pod
spec:
  selector: 
    app: site2
  ports:
    - protocol: TCP
      port: 8090
      targetPort: 80
  type: NodePort

```
`kubectl apply -f port-forwarding.yaml`
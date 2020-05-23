## example deploy flux di on k8S
```
smakhloufi@smakhloufi-Lenovo-Y520-15IKBN:~$ kubectl get all -n flux
NAME                                      READY   STATUS    RESTARTS   AGE
pod/flux-7d8b7d9457-klrx6                 1/1     Running   0          43d
pod/flux-helm-operator-7b7fd7dc79-nnk9c   1/1     Running   0          18d
pod/flux-memcached-749f7fddc6-s2wl4       1/1     Running   0          44d

NAME                     TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)     AGE
service/flux             ClusterIP   10.233.27.227   <none>        3030/TCP    276d
service/flux-memcached   ClusterIP   10.233.33.182   <none>        11211/TCP   276d

NAME                                 DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/flux                 1         1         1            1           276d
deployment.apps/flux-helm-operator   1         1         1            1           276d
deployment.apps/flux-memcached       1         1         1            1           276d

NAME                                            DESIRED   CURRENT   READY   AGE
replicaset.apps/flux-57dd59878d                 0         0         0       276d
replicaset.apps/flux-6bfb5c7877                 0         0         0       170d
replicaset.apps/flux-7d8b7d9457                 1         1         1       43d
replicaset.apps/flux-d46875db9                  0         0         0       170d
replicaset.apps/flux-d88979f78                  0         0         0       276d
replicaset.apps/flux-helm-operator-796b86f9     0         0         0       276d
replicaset.apps/flux-helm-operator-7b7fd7dc79   1         1         1       276d
replicaset.apps/flux-memcached-6cd75cbdbc       0         0         0       276d
replicaset.apps/flux-memcached-749f7fddc6       1         1         1       276d
```

#### To set the user credentials
```
kubectl config set-credentials drogo --client-key=/root/drogo.key --client-certificate=/root/drogo.crt
```

#### To create a context 'developer' 
```
kubectl config set-context developer --cluster=kubernetes --user=drogo
```

#### To set the context
```
kubectl config use-context developer
```

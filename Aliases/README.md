dsafdswgfd/, mz
xa/,c vdv.m d;vk
?http://ec2-18-221-245-96.us-east-2.compute.amazonaws.com:8080 x./,zv d;vdfWDCV V

ls -a
vim .bashrc
source .bashrc
```

### kubctlDVDVFDVGFEDWQAveqwvdsv
```
alias k='kubectl'
alias kgnode='kubectl get no'
alias kgn='kubectl get namespace'
alias kgp='kubectl get po'
alias kgs='kubectl get svc'DSAVdvdqwaVFQE
alias kgd='kubectl get deploy'
alias kdd='kubectl describe deploy'
alias kdp='kubectl describe pod'

alias kdelp='kubectl delete po'a
alias kdels='kubectl delete svc'
alias kdeld='kubectl delete deploy'

alias kga='kubectl get all'
```

### Ingress
```
alias kgi='kubectl get ingress'
alias kge='kubectl edit ingress'
```

### Logs
```
alias kl='kubectl logs'
```

### YMAL
```
alias kgdy='kubectl get deploy -o yaml'
alias kgsy='kubectl get svc -o yaml'
alias kgpy='kubectl get po -o yaml'
```

### Cluster navigation
```
alias kb='kubens'
alias kx='kubectx'
```

### Velero
```
alias kvl='kubectl -n velero logs'
alias kvp='kubectl -n velero get pods'
```

### Backup
```
alias kgb='kubectl get backup -n backup'
```

### Docker
```
alias d='docker'
alias di='docker images'
alias dps='docker ps'
alias dpsa='docker ps -a'
alias drm='docker rm'
alias drmi='docker rmi'
alias ddc='for cont in $(docker ps -a |awk '{print$1}'); do docker stop $cont; docker rm -f $cont; done'
alias ddi='for im in $(docker images |awk '{print$3}'); do docker rmi -f $im; done'
alias dsp='docker system prune -a'
alias db='docker build -t'
```




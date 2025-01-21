
# Rancher-Desktop instead of Docker-Desktop 
`export KUBE_CONFIG=/Users/guillaume.tessier/.KUBE/config`

# Github Action locally
Use [act](https://github.com/nektos/act)

## Auth to Kube cluster (local with Rancher-Desktop) : https://github.com/actions-hub/kubectl

Write content of $HOME/.kube/config to an env file
`cat $HOME/.kube/config| base64 > $HOME/kubeconfig``
add `KUBE_CONFIG=` before this string

## Run
run : `act --secret-file $HOME/kubeconfig.env`
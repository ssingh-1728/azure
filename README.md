# Learning Azure

### Installation

1. Install Azure CLI on macOS(will install kubectl as well)
   `brew update && brew install azure-cli`

2. Install kubelogin
   `brew install Azure/kubelogin/kubelogin`

   To upgrade: `brew update && brew upgrade Azure/kubelogin/kubelogin`

3. Login to azure
   `az login`

4. Set cluster subscription
   `az account set --subscription <>`

5. Download cluster credentials
   `az aks get-credentials --resource-group <> --name <> --overwrite-existing`

6. Use kubelogin plugin for authentication
   `kubelogin convert-kubeconfig -l azurecli`


### Sample K8s Commands

1. Find the current context
   `kubectl config current-context`

3. List contexts
   `kubectl config get-contexts`

4. Change/set context
   `kubectl config use-context <context-name>`

   Modify current context
   `kubectl config set-context --current --namespace=<namespace-name>`

6. List pods with details 
   `kubectl get pods -n <namespace> -l k8s-app=<label> -o wide`
   
   `kubectl get pods --all-namespaces -o wide`
   

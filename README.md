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


### Sample Commands

1. List all deployments in all namespaces
   `kubectl get deployments --all-namespaces=true`

2. List all deployments in a specific namespace
   `kubectl get deployments --namespace <>`

3. List details about a specific deployment
   `kubectl describe deployment <> --namespace <>`

4. Get logs for all pods with a specific label
   `kubectl logs -l <label-key>=<label-value>`

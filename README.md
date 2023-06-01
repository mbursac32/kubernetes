# K3s
Install k3s on a local machine: 
'''bash
curl -sfL https://get.k3s.io | sh -
'''  

To install additional agent nodes and add them to the cluster, run the installation script with the K3S_URL and K3S_TOKEN environment variables. Here is an example showing how to join an agent: 
'''bash
curl -sfL https://get.k3s.io | K3S_URL=https://myserver:6443 K3S_TOKEN=mynodetoken sh -
'''  

# Kind  
Install release binary: 
'''bash
[ $(uname -m) = x86_64 ] && curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.19.0/kind-linux-amd64
'''  
CD to kind-cluster folder and run kind cluster: 
'''bash
cd kind-cluster && kind create cluster --name my-cluster --config=config.yaml
'''
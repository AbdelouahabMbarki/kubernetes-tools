The command below will initialise the cluster

kubeadm init  --kubernetes-version $(kubeadm version -o short)

To manage the Kubernetes cluster, the client configuration and certificates are required. This configuration is created when kubeadm initialises the cluster.
The command copies the configuration to the users home directory and sets the environment variable for use with the CLI

kubeadmin $ sudo cp /etc/kubernetes/admin.conf $HOME/
kubeadmin $ sudo chown $(id -u):$(id -g) $HOME/admin.conf
kubeadmin $ export KUBECONFIG=$HOME/admin.conf

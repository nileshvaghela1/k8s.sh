# k8s.sh
apt update
apt install docker docker.io
apt install conntrack
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube /usr/local/bin/minikube
ls -l /usr/local/bin/
echo 
sleep 3
minikube version
minikube --driver=docker  start --force
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
ls
sleep 3
chmod +x kubectl 
mv kubectl /usr/local/bin/
kubectl get pod -n kube-system
sleep 3
kubectl get node
echo ----------------##--------------
echo "Now start working with minikube"
echo ----------------##--------------

Setup Kubernetes on Centos7
https://msunil1204.medium.com/kubernetes-installation-on-linux-using-vagrant-and-ansible-one-click-installation-with-dashboard-1c93c34392c8
git clone https://github.com/msunilkumar/Kubernetes-setup.git
cd Kubernetes-setup
vagrant up
vagrant ssh master
Kubernetes dashboard -> https://192.168.48.10:32324/
get the Kubernetes dashboard service account token code:
[vagrant@k8smaster ~]$ kubectl describe sa dashboard-admin -n kubernetes-dashboard
[vagrant@k8smaster ~]$ kubectl describe secret dashboard-admin-token-bkvq9 -n kubernetes-dashboard

Error: Reinitiate
Everything will vanish -> vagrant destroy -f
Start from the initial step -> vagrant up
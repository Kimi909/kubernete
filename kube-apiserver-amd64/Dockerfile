FROM gcr.io/google_containers/kube-apiserver-amd64:v1.11.4 
MAINTAINER kbp1234


#!/bin/bash
images=(kube-proxy-amd64:v1.11.4 kube-scheduler-amd64:v1.11.4 kube-controller-manager-amd64:v1.11.4 kube-apiserver-amd64:v1.11.4
etcd-amd64:3.2.18 pause:3.1 kubernetes-dashboard-amd64:v1.8.3 coredns:1.1.3)
for image in ${images[@]} ; do
  docker pull kbp1234/$image
  docker tag kbp1234/$image gcr.io/google_containers/$image
  docker rmi kbp1234/$image
done




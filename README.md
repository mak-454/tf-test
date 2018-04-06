# tf-test


Pre-requisites :->
   . kubeflow installed
   . tf-operator running in 'kubeflow' namespace
   . Single node setup as /tmp/results must be shared between 

docker build . -t test/tf-job:v1
mkdir /tmp/tf-results
kubectl create -f tf-job.yaml


Trainig results will be avaialble in /tmp/tf-results directory of host.

kubectl get po -n kubeflow
kubectl get tfjobs -n kubeflow
kubectl get jobs -n kubeflow


========== Happy Training -> will add serving details soon ==========

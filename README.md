# tf-test

[![GitHub Logo](logo-old.png)](www.oneconvergence.com)

http://github.com - automatic!
[GitHub](http://github.com)

Pre-requisites :->
   . kubeflow installed
   . tf-operator running in 'kubeflow' namespace
   . Single node setup as /tmp/results must be shared between 

docker build . -t test/tf-job:v1
mkdir /tmp/tf-results
kubectl create -f tf-job.yaml

This is a distributed tf training model with MASTER, WORKER & PARAMETER SERVER
They need a shared storage, for now run all JOBs in single node. Will add NFS support soon.

Training model is parameterized and the params are taken as ENV variables in tfjob.yaml.

Trainig results will be avaialble in /tmp/tf-results directory of host.

kubectl get po -n kubeflow
kubectl get tfjobs -n kubeflow
kubectl get jobs -n kubeflow


========== Happy Training -> will add serving details soon ==========

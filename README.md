# Kubernetes the Hard Way by ansible

This ansible role can help you to bootstrap your Kubernetes cluster from scratch. Very similar project https://github.com/kelseyhightower/kubernetes-the-hard-way but using ansible.

I used to use it in my production since Kubernetes version 1.8. It gave me a predictable way to upgrade the cluster. In my opinion, kubeadm was unstable at that time.
The latest tested version was 1.22. And currently, this project is not supported anymore.

You can use it in your production or the lab. If you are familiar with ansible, it helps you understand how to create the kubernetes cluster from scratch (the hard way).

It supports 3 types of control-plane deployment
as systemd service (in a case when you want to hide the control-plane) or launch it outside the cluster.
pod static (preferred way)
classic kubernetes deployment

Ansible creates the certificates for the contol-plane. Worker nodes use tokens to join the cluster. The certificates can be stored in ansible-vault or they will be put to the local machine (where ansible was launched).

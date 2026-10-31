# Networking-in-cloud-environment


In this module I focused mainly on the part of the study youtube video that explains networking in the cloud, and here's all I learnt.

## Table of Contents

1. [Containerizing with Docker](#1-containerizing-with-docker)
2. [Container Networking](#2-container-networking)
3. [Kubernetes](#3-kubernetes)
4. [Ingress](#4-ingress)

---

## 1. Containerizing with Docker

A container packages everything an application needs, from the code to the runtime to the libraries and the settings, into one portable package.

---

## 2. Container Networking

In this module I learnt that when containers run on a server, these containers need to talk to each other.

### Bridge Network

Docker creates a bridge network. This bridge network is a private network that exists only on that server, and all containers that are connected to the same bridge network can communicate with each other using just the container name.

### Overlay Network

Along the line, when our servers grow, a Docker overlay network creates a virtual network that makes different servers appear as if they're on the same host. This way Docker makes sure that our application or service is portable and consistent.

---

## 3. Kubernetes

Now here's what I find really interesting. When our servers start to grow rapidly due to consistent deployment, managing such a number of servers becomes manually impossible, because we have to start looking out for several things... and this is where Kubernetes comes in. What Kubernetes does is automate container management.

### Pods

In Kubernetes the basic unit is a POD. A pod is a group of one or more containers, but it's usually 1 pod per container, and each pod gets its own IP address.

Now these pods are temporary, and they can lose their IP address, especially when we move them around. In an environment where we have lots of containers, this can cause confusion.

### Kubernetes Service

In order for this confusion not to happen, we have the KUBERNETES SERVICE. What the Kubernetes Service does is provide a stable IP address and a DNS name that never change, so no matter what happens, our pod still maintains and keeps its IP address.

---

## 4. Ingress

Now when our cloud environment has been fully deployed, we then deploy Ingress. Ingress allows our server to access the internet and allows internet users to access our application in the cluster.

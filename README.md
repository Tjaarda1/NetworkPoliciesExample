# Network Policies Example

This document presents example network policies that can be set up using EngineBPF in a Kubernetes cluster.

In this example, we consider a Kubernetes cluster with multiple IP pools, segmented by namespaces. The scenario models a university operating a cluster with multiple microservices. Computer science students can deploy their lab workloads while consuming selected university-provided services, as illustrated below.

![General cluster configuration](resources/example.png "General configuration")

Depending on the configuration, the institution may choose whether student pods and containers are allowed to communicate with faculty workloads.

[Policy 1](policy1.yaml) demonstrates a configuration where student workloads have access to the internet and most cluster services, except for secured workloads.

![Network Policy 1](resources/net1.png "Network Policy 1")

Alternatively, student workloads can be restricted to communicate only with faculty workloads, excluding secured services and other university-provided services, as shown in [Policy 2](policy2.yaml).

![Network Policy 2](resources/net2.png "Network Policy 2")

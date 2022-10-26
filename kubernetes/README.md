# Demonstration of Okapi clustering on Kubernetes

The manifests in this directory establish a clustered Okapi installation in a Kubernetes namespace. To use, edit as appropriate for your environment and use `kubectl apply` to create the resources on your Kubernetes cluster. The manifests themselves are (lightly) commented. For questions or additional information, feel free to contact us at [info@indexdata.com](mailto:info@indexdata.com).

## Manifests

* [okapi-cluster-demo-namespace.yaml](okapi-cluster-demo-namespace.yaml) -- establishes the namespace within the cluster
* [hazelcast-rbac.yaml](hazelcast-rbac.yaml) -- creates service account and role binding (Role Based Access Control) to allow Okapi to access the Kubernetes API
* [okapi-config-secret.yaml](okapi-config-secret.yaml) -- sample Okapi configuration properties file
* [okapi-log4j2-xml.yaml](okapi-log4j2-xml.yaml) -- sample Okapi log4j2 configuration
* [hazelcast-configmap.yaml](hazelcast-configmap.yaml) -- sample Hazelcast configuration file
* [okapi-statefulset.yaml](okapi-statefulset.yaml) -- creates Okapi stateful set
* [okapi-service.yaml](okapi-service.yaml) -- creates Okapi service
* [nginx-ingress.yaml](nginx-ingress.yaml) -- sample nginx ingress for the namespace, here using AWS EKS integration

## Useful resources

* [Okapi guide and reference](https://github.com/folio-org/okapi/blob/master/doc/guide.md)
* [Okapi source code](https://github.com/folio-org/okapi)
* [Vert.X Hazelcast default configuration](https://github.com/vert-x3/vertx-hazelcast/blob/master/src/main/resources/default-cluster.xml)
* [Hazelcast full config example](https://github.com/hazelcast/hazelcast/blob/4.2.z/hazelcast/src/main/resources/hazelcast-full-example.xml)

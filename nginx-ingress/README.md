# nginx-ingress

If you hate Helm as much as I do, these manifest files will help you out.

These manifest files can be used to have an nginx-based ingress controller in your Kubernetes cluster. It's basically the standard nginx-ingress with some blocked user agents which stressed my apps in the past or which I simply dislike. 

To apply the manifests to your cluster do it in this order:
1. begin with the CRDs, the order doesn't matter 
2. continue with the ingress class 
3. then create the namespace
4. create the service account (sa)
4. everything ready for the cluster role stuff in the nginx-ingress-rbac file now
5. before you can add the deployment you need the TLS secret
6. now add the deployment 
7. time for the loadbalancer (lb)


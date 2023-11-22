# tekton-demo
oc apply -k https://github.com/nreilly-rhn/tekton-demo/ArgoCD/Init

oc wait argocds.argoproj.io -n openshift-gitops openshift-gitops --for jsonpath='{.status.phase}'=Available

gitops_url=https://$(oc get routes.route.openshift.io -n openshift-gitops openshift-gitops-server -ojsonpath='{.status.ingress[].host}')/

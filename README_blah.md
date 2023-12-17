# tekton-demo

oc apply -k https://github.com/nreilly-rhn/tekton-demo/ArgoCD/Init

until oc wait argocds.argoproj.io -n openshift-gitops openshift-gitops --for jsonpath='{.status.phase}'=Available; do sleep 5; done

oc apply -k https://github.com/nreilly-rhn/tekton-demo/ArgoCD/config/apps

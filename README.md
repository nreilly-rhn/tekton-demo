# tekton-demo

oc apply -k https://github.com/nreilly-rhn/tekton-demo/ArgoCD/Init

until oc wait argocds.argoproj.io -n openshift-gitops openshift-gitops --for jsonpath='{.status.phase}'=Available; do sleep 5; done

oc apply -k https://github.com/nreilly-rhn/tekton-demo/ArgoCD/config/apps

cicd-demo.wvqh.p1.openshiftapps.com

82ac177f9f6a1144b66b

97737718401df756ec9bef3b58fe5fb5da17785f

oc create secret generic apac-csa-github --from-literal=clientSecret=97737718401df756ec9bef3b58fe5fb5da17785f -n openshift-config
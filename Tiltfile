# load("../blogarchive/app.tilt", "blogarchive")
# blogarchive("../blogarchive")

load("../front/app.tilt", "front")
front("../front", resource_deps=["infra"])

local_resource(
    "argocd", 
    cmd="echo Password is `kubectl get pods -n argocd -l app.kubernetes.io/name=argocd-server -o name | cut -d'/' -f 2`", 
    serve_cmd="kubectl port-forward svc/argo-argocd-server -n argocd 8081:443",
    resource_deps=["infra"]
)

local_resource("infra", cmd="./setup_infra.sh")
# load("../blogarchive/app.tilt", "blogarchive")
# blogarchive("../blogarchive")

load("../front/app.tilt", "front")
front("../front", resource_deps=["infra"])

local_resource("infra", cmd="./setup_infra.sh")
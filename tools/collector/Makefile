# Target registry
REGISTRY ?= docker.io
# Target repo
REPO ?= openyurt
# The number of concurrent shell script processes
THREAD ?= 4

# Unify ports of the edgex component
DEBUG ?= false

.PHONY: run
run:
	go run main.go --debug=$(DEBUG) --repo=$(REPO)

sync_image:
	chmod +x ./hack/sync_images.sh
	./hack/sync_images.sh $(REGISTRY) $(REPO) $(THREAD)

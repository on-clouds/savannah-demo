PODTATO_NAMESPACE = podtato-kubectl

.PHONY: install
install:
	kubectl apply -f ./templates/secret.yaml
	cat ./templates/manifest.yaml | envsubst | kubectl apply -f - 

.PHONY: init
init:
	if [ -z $${WEBHOOK_URL} ]; then echo "WEBHOOK_URL is not set"; exit 1; fi
	cat ./templates/manifest.yaml | envsubst > manifest.yaml 



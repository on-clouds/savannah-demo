PODTATO_NAMESPACE = podtato-kubectl

.PHONY: install
install:
	helm install release k8sgpt/k8sgpt-operator -n k8sgpt-operator-system --create-namespace
	kubectl apply -f ./templates/secret.yaml

.PHONY: init
init:
	if [ -z $${WEBHOOK_URL} ]; then echo "WEBHOOK_URL is not set"; exit 1; fi
	cat ./templates/manifest.yaml | envsubst > manifest.yaml 



PODTATO_NAMESPACE = podtato-kubectl

.PHONY: install
install:
	helm install release k8sgpt/k8sgpt-operator -n k8sgpt-operator-system --create-namespace
	kubectl apply -f ./templates/secret.yaml

.PHONY: init
init:
	cp ./templates/manifest.yaml .



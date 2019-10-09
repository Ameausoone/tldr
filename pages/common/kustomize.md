# kustomize

> Kustomize is a tool to easily deploy resources for Kubernetes.
> More information: <https://github.com/kubernetes-sigs/kustomize>.

- Create kustomization.yaml file with resources:

`kustomize create --resources deployment.yaml,service.yaml --namespace staging`

- Build a kustomization.yaml file and deploy it with kubectl:

`kustomize build . | kubectl apply -f - `

- Edit kustomization.yaml file to set image:

`kustomize edit set image busybox=alpine:3.6`

- Create kustomization.yaml file based on existing resources:

`kustomize create --autodetect --namesuffix acme-`
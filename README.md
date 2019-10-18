# eks-config

helm repo add fluxcd https://charts.fluxcd.io

helm upgrade -i flux \
--set helmOperator.create=true \
--set helmOperator.createCRD=false \
--set git.url=git@github.com:ardeshir/eks-config \
--namespace flux \
fluxcd/flux

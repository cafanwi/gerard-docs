helm repo add codecentric https://codecentric.github.io/helm-charts
helm repo update


helm pull codecentric/keycloak --untar=true

helm upgrade keycloak -n keycloak .
helm upgrade --install  keycloak codecentric/keycloak -n keycloak

psql -h 10.0.0.36 -U cafanwiiuser -d keycloak

## istio
helm repo add istio https://istio-release.storage.googleapis.com/charts
helm repo update

# kubernetes HPA(horizontal pod autoscaler)
sample files to create a hpa

__Enable addon__
>$ minikube addons enable metrics-server
>$ minikube addons list


>$ kubectl get pods -n kube-system


__create deployment, service and HPA__

>$ kubectl apply -f php-apache.yaml

>$ kubectl apply -f hpa.yaml

>$ kubectl get all
>$ watch -n1 !!

__Load test__

_get minikube service url_
>$ minikube service php-apache --url

>$ while true; do curl minikube_service_url ; done


# hapi-fhir-k8s
Hapi-Fhir Deployment on Kubernetes

Hapi-Fhir
---
    cd hapi-fhir/
    # Create Persistent Volume & Volume Claim
    kubectl apply -f hapi-fhir-volume.yaml
    kubectl get pv -o wide
    kubectl get pvc -o wide

    # Run Hapi Fhir Deployment Pods
    kubectl apply -f hapi-fhir-deployment.yaml
    kubectl get deploy -o wide
    kubectl get pods -o wide
    kubectl describe pods <POD_NAME>

    # Create Hapi Fhir Service [Type NodePort]
    kubectl apply -f hapi-fhir-service.yaml
    kubectl get svc  -o wide



Hapi-Proxy
---
    cd hapi-proxy/
    # Create Persistent Volume & Volume Claim
    kubectl apply -f hapi-proxy-volume.yaml
    kubectl get pv -o wide
    kubectl get pvc -o wide

    # Run Hapi Proxy Deployment Pods
    kubectl apply -f hapi-proxy-deployment.yaml
    kubectl get deploy -o wide
    kubectl get pods -o wide
    kubectl describe pods <POD_NAME>

    # Create Hapi Proxy Service [Type NodePort]
    kubectl apply -f hapi-proxy-service.yaml
    kubectl get svc  -o wide
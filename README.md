# Datadog Helm GEK Deployment

# Requires Community Built Helm Cloudbuilder image
    https://github.com/GoogleCloudPlatform/cloud-builders-community/tree/master/helm

    
# Requries cluster create role binding granted to GKE cluster
    kubectl auth can-i create clusterroles --as=system:serviceaccount:<namespace>:<sa-account>@cloudbuild.gserviceaccount.com

# Set Kube Secret for Datadog API/APP Keys
    kubectl create secret generic datadog-secret --from-literal api-key=<API Key> --from-literal app-key=<App Key>

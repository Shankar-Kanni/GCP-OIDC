# GCP-OIDC

To grant the service account to access the token.

Create a Work identity pool with provide as OIDC and add the github url with required attributes.

Create SA or use the existing SA and add the provider url from the pool and grant below role.

gcloud iam service-accounts add-iam-policy-binding "XXXX@XXXX.iam.gserviceaccount.com" \
  --project="XXXX" \
  --role="roles/iam.workloadIdentityUser" \
  --member="principalSet://iam.googleapis.com/projects/XXXXX/locations/global/workloadIdentityPools/github-actions-sa/attribute.repository/repo_owner/repo"


  #To go inside the container
  
  shankarkanni80@cloudshell:~ (terra-55091)$ kubectl exec -i -t spring-boot-7c74ff77bc-g5l8r /bin/sh

  #To create GKE cluster
  
  shankarkanni80@cloudshell:~ (terra-55091)$ gcloud container clusters create gke-deep-dive --num-nodes=1 --disk-type=pd-standard --disk-size=10 --zone us-central1-a

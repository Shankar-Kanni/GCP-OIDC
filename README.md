# GCP-OIDC

To grant the service account to access the token.

gcloud iam service-accounts add-iam-policy-binding "github@terra-55091.iam.gserviceaccount.com" \
  --project="terra-55091" \
  --role="roles/iam.workloadIdentityUser" \
  --member="principalSet://iam.googleapis.com/projects/1090358368731/locations/global/workloadIdentityPools/github-actions-sa/attribute.repository/Shankar-Kanni/GCP-OIDC"
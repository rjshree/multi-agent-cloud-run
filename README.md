# multi-agent-cloud-run
###  Run the deployment command
```bash
uvx --from google-adk==1.14.0 \
adk deploy cloud_run \
  --project=$PROJECT_ID \
  --region=europe-west1 \
  --service_name=zoo-tour-guide \
  --with_ui \
  . \
  -- \
  --labels=dev-tutorial=codelab-adk \
  --service-account=$SERVICE_ACCOUNT
```
### delete resources:
```bash
gcloud run services delete zoo-tour-guide --region=europe-west1 --quiet
gcloud artifacts repositories delete cloud-run-source-deploy --location=europe-west1 --quiet

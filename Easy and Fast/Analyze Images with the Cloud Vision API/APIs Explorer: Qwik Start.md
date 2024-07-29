## APIs Explorer: Qwik Start  [GSP277]

```
export PROJECT_ID=$(gcloud config get-value project)
gsutil mb -p $PROJECT_ID -c regional -l us-east1 gs://$PROJECT_ID-bucket
curl -L -o demo-image.jpg https://github.com/Sandeepamlan/arcade/blob/main/APIs%20Explorer%3A%20Qwik%20Start/demo-image.jpg
gsutil cp demo-image.jpg gs://$PROJECT_ID-bucket/demo-image.jpg
gsutil acl ch -u allUsers:R gs://$PROJECT_ID-bucket/demo-image.jpg
```

### DONE !!!

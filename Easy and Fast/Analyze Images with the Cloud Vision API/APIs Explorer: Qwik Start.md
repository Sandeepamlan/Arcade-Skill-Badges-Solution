## APIs Explorer: Qwik Start  [GSP277]



```
export PROJECT_ID=$(gcloud config get-value project)
gsutil mb -p $PROJECT_ID -c regional -l us-east1 gs://$PROJECT_ID-bucket
curl -L -o demo-image.jpg https://github.com/Sandeepamlan/Arcade-Skill-Badges-Solution/blob/main/Easy%20and%20Fast/Analyze%20Images%20with%20the%20Cloud%20Vision%20API/demo-image.png
gsutil cp demo-image.jpg gs://$PROJECT_ID-bucket/demo-image.jpg
gsutil acl ch -u allUsers:R gs://$PROJECT_ID-bucket/demo-image.jpg
```

### DONE !!!

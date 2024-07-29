# Detect Labels, Faces, and Landmarks in Images with the Cloud Vision API [GSP037]


* In the GCP Console open the Cloud Shell and enter the following commands:

```
gcloud alpha services api-keys create --display-name="Sandeep" 
KEY_NAME=$(gcloud alpha services api-keys list --format="value(name)" --filter "displayName=Sandeep")
export API_KEY=$(gcloud alpha services api-keys get-key-string $KEY_NAME --format="value(keyString)")
export PROJECT_ID=$(gcloud config list --format 'value(core.project)')
gsutil mb gs://$PROJECT_ID
```

# Note: Go to Bucket and upload all three images then run the following commands
> Donuts.png
> selfie.png
> city.png

```

export PROJECT_NUMBER=$(gcloud projects describe $DEVSHELL_PROJECT_ID --format="value(projectNumber)")


gcloud storage buckets create gs://$DEVSHELL_PROJECT_ID-bucket --project=$DEVSHELL_PROJECT_ID


curl -L -o city.png https://github.com/Sandeepamlan/Arcade-Skill-Badges-Solution/blob/main/Easy%20and%20Fast/Analyze%20Images%20with%20the%20Cloud%20Vision%20API/city.png

curl -Lo donuts.png https://github.com/Sandeepamlan/Arcade-Skill-Badges-Solution/blob/main/Easy%20and%20Fast/Analyze%20Images%20with%20the%20Cloud%20Vision%20API/donuts.png

curl -Lo selfie.png https://github.com/Sandeepamlan/Arcade-Skill-Badges-Solution/blob/main/Easy%20and%20Fast/Analyze%20Images%20with%20the%20Cloud%20Vision%20API/selfie.png


gsutil cp city.png gs://$DEVSHELL_PROJECT_ID-bucket/city.png

gsutil cp donuts.png gs://$DEVSHELL_PROJECT_ID-bucket/donuts.png

gsutil cp selfie.png gs://$DEVSHELL_PROJECT_ID-bucket/selfie.png



gcloud storage objects update gs://$PROJECT_ID/donuts.png --add-acl-grant=entity=AllUsers,role=READER
gcloud storage objects update gs://$PROJECT_ID/selfie.png --add-acl-grant=entity=AllUsers,role=READER
gcloud storage objects update gs://$PROJECT_ID/city.png --add-acl-grant=entity=AllUsers,role=READER
```

## DONE !!! 😄

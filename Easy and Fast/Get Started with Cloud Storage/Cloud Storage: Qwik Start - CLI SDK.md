## Cloud Storage: Qwik Start - CLI SDK  [GSP074]

```

gcloud auth list
gcloud config list project
export PROJECT_ID=$(gcloud config get-value project)

gsutil mb gs://$PROJECT_ID-Sandeep

curl https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Ada_Lovelace_portrait.jpg/800px-Ada_Lovelace_portrait.jpg --output ada.jpg

gsutil cp ada.jpg gs://$PROJECT_ID-Sandeep

rm ada.jpg

gsutil cp -r gs://$PROJECT_ID-Sandeep/ada.jpg .

gsutil cp gs://$PROJECT_ID-Sandeep/ada.jpg gs://$PROJECT_ID-Sandeep/image-folder/

gsutil ls gs://$PROJECT_ID-Sandeep

gsutil ls -l gs://$PROJECT_ID-Sandeep/ada.jpg

gsutil acl ch -u AllUsers:R gs://$PROJECT_ID-Sandeep/ada.jpg

```

### DONE !!!

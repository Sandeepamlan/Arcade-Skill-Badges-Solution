## APIs Explorer: Cloud Storage [GSP421]



```
curl -LO https://github.com/Sandeepamlan/Arcade-Skill-Badges-Solution/blob/main/Easy%20and%20Fast/Get%20Started%20with%20Cloud%20Storage/demo-image1.png
curl -LO https://github.com/Sandeepamlan/Arcade-Skill-Badges-Solution/blob/main/Easy%20and%20Fast/Get%20Started%20with%20Cloud%20Storage/demo-image2.png
curl -LO https://github.com/Sandeepamlan/Arcade-Skill-Badges-Solution/blob/main/Easy%20and%20Fast/Get%20Started%20with%20Cloud%20Storage/demo-image1-copy.png


gcloud alpha services api-keys create --display-name="Sandeep"  
KEY_NAME=$(gcloud alpha services api-keys list --format="value(name)" --filter "displayName=Sandeep") 
export API_KEY=$(gcloud alpha services api-keys get-key-string $KEY_NAME --format="value(keyString)") 
echo $API_KEY

gsutil mb gs://$DEVSHELL_PROJECT_ID

gsutil mb gs://$DEVSHELL_PROJECT_ID-Sandeep

gsutil cp demo-image1.png gs://$DEVSHELL_PROJECT_ID

gsutil cp demo-image2.png gs://$DEVSHELL_PROJECT_ID

gsutil cp demo-image1-copy.png gs://$DEVSHELL_PROJECT_ID-Sandeep

```

### DONE !!!

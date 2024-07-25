## App Engine: Qwik Start - PHP  [GSP071]


### Press 2 and Y
```
export REGION=


gcloud auth list
gcloud config list project
gcloud config set compute/region $REGION

gcloud services enable appengine.googleapis.com

git clone https://github.com/GoogleCloudPlatform/php-docs-samples.git

cd php-docs-samples/appengine/standard/helloworld

gcloud app deploy

gcloud app browse
```

## DONE !!!

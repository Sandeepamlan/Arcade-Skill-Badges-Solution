## Speech to Text Transcription with the Cloud Speech API [GSP048]


### Create API KEY and Then paste below command in SSH 

```
export API_KEY=


cat > request.json <<EOF

{
  "config": {
      "encoding":"FLAC",
      "languageCode": "en-US"
  },
  "audio": {
      "uri":"gs://cloud-samples-data/speech/brooklyn_bridge.flac"
  }
}

EOF

export API_KEY= ${API_KEY}

curl -s -X POST -H "Content-Type: application/json" --data-binary @request.json \
"https://speech.googleapis.com/v1/speech:recognize?key=${API_KEY}" > result.json

sleep 5

cat result.json
```

----------------------------------------------------------------------------------------------------------------------------------------------------

```
rm -f request.json

cat >> request.json <<EOF

 {
  "config": {
      "encoding":"FLAC",
      "languageCode": "fr"
  },
  "audio": {
      "uri":"gs://cloud-samples-data/speech/corbeau_renard.flac"
  }
}

EOF

export API_KEY= ${API_KEY}

curl -s -X POST -H "Content-Type: application/json" --data-binary @request.json \
"https://speech.googleapis.com/v1/speech:recognize?key=${API_KEY}" > result.json

sleep 5

cat result.json
```

### DONE





```

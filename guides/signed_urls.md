## Notes:
+ 4 Hours Validity: The -d 4h parameter specifies a 4-hour validity for the signed URL.
+ Bulk URL Generation: These commands will generate signed URLs for all files in the specified folders and display them in the terminal.
```
# Generate signed URLs for all files in the bigquery folder
for file in $(gsutil ls gs://agent_miguel_looker_bucket/bigquery); do 
    gsutil signurl -d 4h ~/signed-url-key.json $file
done

# Generate signed URLs for all files in the help_docs folder
for file in $(gsutil ls gs://agent_miguel_looker_bucket/help_docs); do 
    gsutil signurl -d 4h ~/signed-url-key.json $file
done

# Generate signed URLs for all files in the looker_studio folder
for file in $(gsutil ls gs://agent_miguel_looker_bucket/looker_studio); do 
    gsutil signurl -d 4h ~/signed-url-key.json $file
done

# Generate signed URL for the DoIT Looker agent app zip file
gsutil signurl -d 4h ~/signed-url-key.json gs://agent_miguel_looker_bucket/doit_looker_agent_bucket/app.zip

# Generate signed URL for the tickets CSV file
gsutil signurl -d 4h ~/signed-url-key.json gs://agent_miguel_looker_bucket/tickets/tickets.csv
```

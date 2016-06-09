# gcutil
Google Cloud Utils in Go

## Setup
1. Download pemission json file from google cloud console and save it to
   ~/.config/gcloud/application_default_credentials.json, see
   https://godoc.org/golang.org/x/oauth2/google#DefaultTokenSource
1. Enable storage JSON API

## Test Setup
1. Create project, dataset and storage bucket, set in bqclient_test.go.

## Operations
1. Run bq queries and export data to local disk.
```
go run pipeline.go --jobs_path=jobs/*.yml  --project=950350008903 \
  --dataset=test_gcutil --bucket=test_gcutil \
  --dst_dir=results
```

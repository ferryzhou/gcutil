# gcutil

Google Cloud Utils in Go

## Setup

1. Download pemission json file from google cloud console and save it to ~/.config/gcloud/application_default_credentials.json, see <https://godoc.org/golang.org/x/oauth2/google#DefaultTokenSource>
2. Enable storage JSON API

## Test Setup

1. Create project, dataset and storage bucket, set in bqclient_test.go.

## Operations

1. Run bq queries and export data to local disk. dataset and bucket needs to be created before running this

  ```
  cd pipeline/
  go run pipeline.go --jobs_path=../bqclient/testdata/goodjobs01/*.yml  \
    --project=950350008903 --dst_dir=results --dataset=bqclient_test \
    --bucket=bqclient_test
  ```

# Developer Guide

examples:

https://github.com/google/google-api-go-client/tree/master/examples
https://cloud.google.com/storage/docs/json_api/v1/json-api-go-samples

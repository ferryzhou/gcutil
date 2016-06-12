# gcutil

Google Cloud Utils in Go

## Usage

1. Download pemission json file from google cloud console and save it to ~/.config/gcloud/application_default_credentials.json, see <https://godoc.org/golang.org/x/oauth2/google#DefaultTokenSource>

1. Enable storage JSON API.

1. Setup bigquery project, dataset and storage bucket.

1. Create job config files, see bqclient/testdata/goodjobs01/ for example

1. Run bq queries and export data to local disk

  ```
  cd bqrun && go build && \
  ./bqrun --jobs_path=../bqclient/testdata/goodjobs01/*.yml --dst_dir=results \
    --project=950350008903 --dataset=bqclient_test --bucket=bqclient_test
  ```

## Test Setup

  1. Create project, dataset and storage bucket, set in bqclient_test.go.

# Developer Guide

examples:

https://github.com/google/google-api-go-client/tree/master/examples
https://cloud.google.com/storage/docs/json_api/v1/json-api-go-samples

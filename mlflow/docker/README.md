# Docker Image for MLflow Tracking Server with s3 compatible object storage

MLflow Tracking Server with s3 compatible object storage

## Supported Tags

Tag name means `<python-version>-<mlflow-version>-<image-version>`. For example, `3.7-1.22.0-v1.0.0` means mlflow-tracking server is based on python 3.7, mlflow==1.22.0 and such image was publised as v1.0.0

- `3.7-1.22.0-*`
- `3.7-1.21.0-*`
- `3.7-1.20.0-*`

## Quick Start

First, prepare s3 compatible object storage.

Second, change following env variables for your own object storage and run following command:

```
docker run -it --rm -e AWS_BUCKET=mlflow -e AWS_ACCESS_KEY_ID=minio -e AWS_SECRET_ACCESS_KEY=minio123 -e MLFLOW_S3_ENDPOINT_URL=http://your-minio-domain -p 5000:5000 ghcr.io/mlops-for-all/mlflow-tracking-server:3.7-1.22.0-v1.0.0
```

Now you could access mlflow tracking server on localhost:5000.


## Configuration

You could customize following mlflow tracking server's configuration. These are environment variables that could be configured by runtime, and default values are as follows:

```
ENV AWS_BUCKET mlflow
ENV AWS_ACCESS_KEY_ID s3_access_key_id
ENV AWS_SECRET_ACCESS_KEY s3_secret_access_key
ENV MLFLOW_S3_ENDPOINT_URL http://minio-service.kubeflow.svc.cluster.local:9000
ENV PORT 5000
ENV MLFLOW_BACKEND_STORE_URI file:///tmp/mlflow 
```

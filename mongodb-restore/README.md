# MongoDB Restore Helm Chart

## Chart Details

This chart implements kubernetes jobs api to run the `mongorestore` command on kubernetes which restores S3 backup snapshot to a running MongoDB replicaset in kubernetes

## Installing the Chart

To install the chart with the release name `my-release`:

``` console
helm install --name my-release .
```

## Configuration
The following table lists the configurable parameters of the mongodb chart and their default values.

| Parameter                           | Description                                                               | Default                                             |
| ----------------------------------- | ------------------------------------------------------------------------- | --------------------------------------------------- |
| `image`                          | Image to run backup and restore commands                                     | `3`                                                 |
| `s3Path`                    | The S3 location where snapshot is to be stored or retrieved from                                               | `NA`                                               |
| `iam.amazonaws.com/role`               | IAM Role with write access to S3                                                     | `NA`                                                |
| `restoreMongoConnectionString`                  | Mongo connection string where restore is to be done                                       | `NA`                                               |

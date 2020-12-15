# MongoDB Replicaset with backup and restore for Kubernetes on AWS
This helps you run a production ready highly-available MongoDB with capabilities of backup and restore to support disaster recovery, in this repository you will find 2 helm charts
1. MongoDB Replicaset with S3 backup (mongodb-replicaset)
2. Restore a snapshot (mongodb-restore)

## Don't have a running MongoDB replicaset

If you want to run a MongoDB on kube visit StackPointCloud stable trusted [helm charts](https://github.com/StackPointCloud/trusted-charts/tree/master/stable/mongodb-replicaset)

## Chart Details
This chart implements makes use of StackPointCloud stable trusted [helm charts](https://github.com/StackPointCloud/trusted-charts/tree/master/stable/mongodb-replicaset) to run mongodb and a [docker image](https://hub.docker.com/r/lgatica/mongodump-s3) which has AWS CLI and Mongo cli installed along with Kubernetes Batch [Job](https://kubernetes.io/docs/concepts/workloads/controllers/job/) and [CronJob](https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/) API to regularly take backups and run a restore on demand.

To install any of the chart goto the root chart directory and run below command or open them to read more details around the same

`helm install --name <release_name> .`

## Additional Resources
Using above we deployed a production ready mongo db on kubernetes for more details on the details of the same you can refer to this medium article  - [How we achieved HA and DR for MongoDB using Kubernetes and AWS](https://medium.com/miq-tech-and-analytics/how-we-achieved-ha-and-dr-for-mongodb-using-kubernetes-and-aws-c029c3f1eb41)
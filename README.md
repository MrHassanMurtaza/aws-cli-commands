# aws-cli-commands
Some Common AWS CLI Commands

## AWS S3 CLI Commands
Command to Sync On Premises Files to S3 Bucket:
```
aws s3 sync mydirectory s3://mybucketname
```

To sync deleted files:
```
aws s3 sync mydirectory s3://mybucketname --delete
```

To make syncing files public:
```
aws s3 sync mydirectory s3://mybucketname --delete --acl public-read
```

To list all files recursively:
```
aws s3 ls --recursive s3://mybucketname
```

To copy data from one bucket to another:
```
aws s3 sync s3://mybucketnam1 s3://mybucketname2 --region destinationregion
```

Cross account bucket data transfer:
```
aws s3 sync s3://mybucketname1 s3://mybucketname2 --acl bucket-owner-full-control --region destinationregion
```

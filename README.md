# cfn-guard-rules
Rules for CloudFormation Guard

# Ignoring rules
Some rules can be ignored by adding Metadata to the resource, for example:

```yaml
Resources:
  Bucket1:
    Type: AWS::S3::Bucket
    Metadata:
      CfnGuard:
        Ignore: [s3_intelligent_tiering]
```

These rules are:

location | rule name | reason
--- | --- | ---
cost/s3 | s3_intelligent_tiering | If you know the storage class you want, you don't need intelligent tiering. 

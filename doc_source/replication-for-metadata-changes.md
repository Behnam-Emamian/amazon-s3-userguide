# Replicating metadata changes with Amazon S3 replica modification sync<a name="replication-for-metadata-changes"></a>

Amazon S3 replica modification sync can help you keep object metadata such as tags, ACLs, and Object Lock settings replicated between replicas and source objects\. By default, Amazon S3 replicates metadata from the source objects to the replicas only\. When replica modification sync is enabled, Amazon S3 replicates metadata changes made to the replica copies back to the source object, making the replication bidirectional\.

## Enabling replica modification sync<a name="enabling-replication-for-metadata-changes"></a>

You can use Amazon S3 replica modification sync with new or existing replication rules\. You can apply it to an entire S3 bucket or to Amazon S3 objects that have a specific prefix\.

To enable replica modification sync using the Amazon S3 console, see [Walkthroughs: Examples for configuring replication](replication-example-walkthroughs.md)\. This topic provides instructions for enabling replica modification sync in your replication configuration when buckets are owned by the same or different AWS accounts\.

To enable replica modification sync using the AWS Command Line Interface \(AWS CLI\), you must add a replication configuration to the bucket containing the replicas with `ReplicaModifications` enabled\. To set up two\-way replication, create a replication rule from the source bucket \(*DOC\-EXAMPLE\-BUCKET1*\) to the bucket containing the replicas \(*DOC\-EXAMPLE\-BUCKET2*\)\. Then, create a second replication rule from the bucket containing the replicas \(*DOC\-EXAMPLE\-BUCKET2*\) to the source bucket \(*DOC\-EXAMPLE\-BUCKET1*\)\. Buckets can be in the same, or in different, AWS Regions\.

**Note**  
You must enable replica modification sync on both buckets to replicate replica metadata changes like object access control lists \(ACLs\), object tags, or Object Lock settings on the replicated objects\. Like all replication rules, these rules can either be applied to the entire Amazon S3 bucket or a subset of Amazon S3 objects filtered by prefix or object tags\.

In the following example configuration, Amazon S3 replicates metadata changes under the prefix *Tax* to the bucket *DOC\-EXAMPLE\-BUCKET*, which would contain the source objects\.

```
{
    "Rules": [
        {
            "Status": "Enabled",
            "Filter": {
                "Prefix": "Tax"
            },
            "SourceSelectionCriteria": {
                "ReplicaModifications":{
                    "Status": "Enabled"
                }
            },
            "Destination": {
                "Bucket": "arn:aws:s3:::DOC-EXAMPLE-BUCKET"
            },
            "Priority": 1
        }
    ],
    "Role": "IAM-Role-ARN"
}
```

For full instructions on creating replication rules using the AWS CLI, see [Configuring replication for source and destination buckets owned by the same account](replication-walkthrough1.md)\.
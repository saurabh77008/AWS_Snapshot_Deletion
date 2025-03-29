AWS Lambda Function for Deleting Unused EBS Snapshots

✅ Project Description

This AWS Lambda function is designed to automatically identify and delete unused Amazon Elastic Block Store (EBS) snapshots. The goal is to optimize storage costs by removing stale snapshots that are no longer associated with any active EC2 volumes or running instances.



🔥 Features


Automated Cleanup: Identifies and deletes EBS snapshots that are not linked to any volume or are linked to deleted volumes.
Cost Optimization: Frees up unused storage, reducing unnecessary costs.
Efficient Execution: Uses AWS Lambda to run on a schedule (e.g., using Amazon EventBridge) for periodic cleanup.
Error Handling: Handles exceptions gracefully, including deleted or missing volumes.



🛠️ Prerequisites


1-Before deploying this Lambda function, ensure you have the following:

2-AWS CLI configured with appropriate permissions.

3-IAM Role with the following permissions:

    a-ec2:DescribeSnapshots

    b-ec2:DescribeInstances

    c-ec2:DescribeVolumes

    d-ec2:DeleteSnapshot

4-Boto3 library installed (comes pre-installed in AWS Lambda runtime).


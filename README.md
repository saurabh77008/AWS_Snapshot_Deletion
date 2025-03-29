# AWS Lambda Function for Deleting Unused EBS Snapshots

## ✅ Project Description
This AWS Lambda function is designed to automatically identify and delete unused Amazon Elastic Block Store (EBS) snapshots. The goal is to optimize storage costs by removing stale snapshots that are no longer associated with any active EC2 volumes or running instances.

## 🔥 Features

- **Automated Cleanup**: Identifies and deletes EBS snapshots that are not linked to any volume or are linked to deleted volumes.
- **Cost Optimization**: Frees up unused storage, reducing unnecessary costs.
- **Efficient Execution**: Uses AWS Lambda to run on a schedule (e.g., using Amazon EventBridge) for periodic cleanup.
- **Error Handling**: Handles exceptions gracefully, including deleted or missing volumes.

## 🛠️ Prerequisites

Before deploying this Lambda function, ensure you have the following:

1. **AWS CLI** configured with appropriate permissions.
2. **IAM Role** with the following permissions:
    - `ec2:DescribeSnapshots`
    - `ec2:DescribeInstances`
    - `ec2:DescribeVolumes`
    - `ec2:DeleteSnapshot`
3. **Boto3 library** installed (comes pre-installed in AWS Lambda runtime).

## 🚀 Deployment Steps

1. **Create an IAM Role** with the required permissions and attach it to your Lambda function.
2. **Create the Lambda Function**:
   - Open AWS Lambda Console.
   - Click on "Create Function" → "Author from scratch".
   - Choose Python as the runtime.
   - Assign the created IAM role.
3. **Upload or Paste the Code**:
   - Use the AWS Lambda console or AWS CLI to upload the function.
4. **Test the Function**:
   - Execute the Lambda function manually to verify snapshot deletion.
5. **Schedule the Lambda Function**:
   - Use Amazon EventBridge to trigger the Lambda function periodically (e.g., daily or weekly).

## 📜 Usage

Once deployed, this Lambda function will automatically run on the defined schedule and delete stale EBS snapshots. Logs can be monitored in **Amazon CloudWatch**.



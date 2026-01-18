---
name: aws
description: AWS comprehensive integration with documentation and best practices (Official)
---

# AWS Integration

AWS comprehensive integration with documentation and best practices (Official)

## Configuration

### Environment Variables

```bash
export AWS_ACCESS_KEY_ID="your-value"
export AWS_SECRET_ACCESS_KEY="your-value"
export AWS_REGION="your-value"
```

Get credentials: https://console.aws.amazon.com/iam/home#/security_credentials

## Commands

### List S3 buckets

```bash
aws s3 ls
```

### List bucket contents

```bash
aws s3 ls s3://bucket-name/
```

### Upload file to S3

```bash
aws s3 cp file.txt s3://bucket-name/
```

### List EC2 instances

```bash
aws ec2 describe-instances
```

### List Lambda functions

```bash
aws lambda list-functions
```

### Invoke Lambda

```bash
aws lambda invoke --function-name myFunc output.json
```

---

## Author

AWS

## Version

1.2.0

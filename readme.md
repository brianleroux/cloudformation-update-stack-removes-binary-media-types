steps to repoduce

1.) Package code with SAM:

```
sam package --template-file sam0.json --output-template-file out.yaml --s3-bucket [S3 bucket]
```

2.) Deploy the CloudFormation stack:

```
sam deploy --template-file out.yaml --stack-name [Stack Name] --s3-bucket [S3 bucket] --capabilities CAPABILITY_IAM
```

3.) Verify hello world from generated API Gateway output

4.) Update the template:

```
sam package --template-file sam1.json --output-template-file out.yaml --s3-bucket [S3 bucket]
```

5.) Deploy the CloudFormation stack:

```
sam deploy --template-file out.yaml --stack-name [Stack Name] --s3-bucket [S3 bucket] --capabilities CAPABILITY_IAM
```

6.) Notice how binary media types is now missing

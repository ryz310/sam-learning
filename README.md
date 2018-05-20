# sam-learning

See: https://github.com/awslabs/serverless-application-model/blob/develop/HOWTO.md

## Installing

See: https://github.com/awslabs/aws-sam-cli#installation

```
$ pip install --user aws-sam-cli
$ sam --version
```

## Building

See: https://github.com/awslabs/serverless-application-model/blob/develop/HOWTO.md#packing-artifacts

```
$ aws cloudformation package \
    --template-file template.yml  \
    --s3-bucket {s3-backet-name}  \
    --output-template-file packaged-template.yml
```

## Deploying

See: https://github.com/awslabs/serverless-application-model/blob/develop/HOWTO.md#deploying-to-aws-cloudformation

```
$ aws cloudformation deploy \
    --template-file packaged-template.yml \
    --stack-name sam-learning-stack
```

### IAM Requirements

- AWSCloudFormationDescribeStacks
- AWSCloudFormationCreateChangeSet

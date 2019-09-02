```bash
name=lambda-hello-world
```

### Validate Template

```bash
aws cloudformation validate-template --template-body file://${name}.yml
```

### Create Stack

```bash
aws cloudformation create-stack --stack-name ${name} --template-body file://${name}.yml --capabilities CAPABILITY_IAM
```

### Update Stack

```
aws cloudformation update-stack --stack-name ${name} --template-body file://${name}.yml --capabilities CAPABILITY_IAM
```

### Delete Stack

```bash
aws cloudformation delete-stack --stack-name ${name}
```

### Describe Stack

```bash
aws cloudformation describe-stacks --stack-name ${name}
aws cloudformation describe-stacks --stack-name ${name} --query "Stacks[].Outputs"
```

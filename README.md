# AWS AMI for CSYE 6225

## Team Information

| Name | NEU ID | Email Address |
| --- | --- | --- |
| Nithin Muvva | 001440858 | muvva.n@husky.neu.edu |
| Kiran Kumar Kathiresan | 001427809 | kathiresan.k@husky.neu.edu |
| Akhil Prasad | 001449445 | prasad.ak@husky.neu.edu |


## Validate Template

```
packer validate ubuntu-ami.json
packer validate centos-ami-template.json
```

## Build AMI


```
packer build \
    -var 'aws_access_key=REDACTED' \
    -var 'aws_secret_key=REDACTED' \
    -var 'aws_region=us-east-1' \
    -var 'subnet_id=REDACTED' \
    centos-ami-template.json
```

```
packer build \
    -var 'aws_access_key=REDACTED' \
    -var 'aws_secret_key=REDACTED' \
    -var 'aws_region=us-east-1' \
    -var 'subnet_id=REDACTED' \
    ubuntu-ami.json
```


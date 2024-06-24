![](https://img.shields.io/github/commit-activity/t/subhamay-bhattacharyya/0104-lupin-cft)&nbsp;![](https://img.shields.io/github/last-commit/subhamay-bhattacharyya/0104-lupin-cft)&nbsp;![](https://img.shields.io/github/release-date/subhamay-bhattacharyya/0104-lupin-cft)&nbsp;![](https://img.shields.io/github/repo-size/subhamay-bhattacharyya/0104-lupin-cft)&nbsp;![](https://img.shields.io/github/directory-file-count/subhamay-bhattacharyya/0104-lupin-cft)&nbsp;![](https://img.shields.io/github/actions/workflow/status/subhamay-bhattacharyya/0104-lupin-cft/deploy-stack.yaml)&nbsp;![](https://img.shields.io/github/issues/subhamay-bhattacharyya/0104-lupin-cft)&nbsp;![](https://img.shields.io/github/languages/top/subhamay-bhattacharyya/0104-lupin-cft)&nbsp;![](https://img.shields.io/github/commit-activity/m/subhamay-bhattacharyya/0104-lupin-cft)&nbsp;![](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/bsubhamay/b21a193b71079cfd71034ff303e7cae9/raw/0104-lupin-cft.json?)

# Project Tarius: AWS Serverless Real Time Data Load to DynamoDB.

Creating a custom VPC with public and private subnets and nat gateway to access internet from private subnet. Create VPC endpoint for S3 and KMS and create EC2 instances in the public and private subnets and test the connectivity.

## Description

This repo creates a custom VPC with four public and private subnets in four different availability zones. The CloudFormation template has a parameter to enable IPV6 CI/CD block. Internet connectivity is enabled in the private subnets are using Nat Gateway. Two EC2 instances and spinned up in piblic and private subnets.

![Project Lupin - Design Diagram](https://github.com/subhamay-bhattacharyya/0104-lupin-cft/architecture-diagram/lupin-architecture-diagram.jpg)


### Services Used
```mermaid
mindmap
  root((1 -  AWS CloudFormation ))
    2
        AWS Custom VPC, Subnets and Route table
    3
        Internet Gateway
    4
        Nat Gateway 
    5
        Custom Network Access List 
    6
        Security Group
    7   
        VPC Endpoint
    8   
        AWS Key Management Service
    9
        AWS EC2
        
```


* Repository Directory Structure
```
tarius-repo/
├─ .git
├─ .github/
│  ├─ workflows/
│  │  ├─ delete-stack.yaml  (**created by the template)
│  │  ├─ deploy-stack.yaml  (**created by the template)
├─ architecture-diagram/
│  ├─ project-architecture-diagram.png
├─ cft/
│  ├─ project-root-stack.yaml
│  ├─ nested-stacks/
│  │  ├─ service1-nested-stack.yaml  (service names are lambda, s3,sns..etc)
│  │  ├─ service2-nested-stack.yaml
│  │  ├─ service3-nested-stack.yaml
├─ src/
│  ├─ lambda-function-base-name.py
├─ kms-policy/
│  ├─ kms-key-policy.json (required for documentation purpose only)
├─ params/
│  ├─ cfn-parameters.json
├─ .gitignore
├─ README.md

```

## Authors

Contributors names and contact info

Subhamay Bhattacharyya  - [subhamay.aws@gmail.com]

## Version History

* 0.1
    * Initial Release

## License

This project is licensed under Subhamay Bhattacharyya. All Rights Reserved.

## Acknowledgments


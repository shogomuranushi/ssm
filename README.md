# usm
usm(Useful Session Manager) is useful extended interface for AWS Session Manager.

## Demo
usm interactively specifies an EC2 and accesses EC2 via AWS Session Manager.

## Why use usm?
### Security
- The operation history is all recorded in S3 or CloudWatch Logs by AWS Session Manager. (Setting required)
- Record all logged in users in CloudTrail.
- It is not necessary to open the ssh port of SecurityGroup.
- It is not necessary to started the ssh service.

### Simple
- You can easily switch between AWS profiles. (Option)
- You can log-in to EC2 just by selecting EC2 from the CLI.

## Required
### Local
- [AWS CLI](https://docs.aws.amazon.com/ja_jp/cli/latest/userguide/installing.html)
  - [Session Manager Plugin for the AWS CLI](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/session-manager-working-with-install-plugin.html)
- [peco](https://github.com/peco/peco)

### Server
- [Install ssm agent 2.3.12+](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/sysman-manual-agent-install.html)
- [Attach the IAM role of `AmazonEC2RoleforSSM` to EC2](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/systems-manager-access.html)
- Access from the EC2 to the Internet is permitted

## Install
- Set up the local. Install required [AWS CLI](https://docs.aws.amazon.com/ja_jp/cli/latest/userguide/installing.html) and [Session Manager Plugin for the AWS CLI](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/session-manager-working-with-install-plugin.html) and [peco](https://github.com/peco/peco).
- Set up the server. Install required [ssm agent](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/sysman-manual-agent-install.html) and [Attach the IAM role of `AmazonEC2RoleforSSM` to EC2](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/systems-manager-access.html)

- Install ssm
```
sudo curl -o /usr/local/bin/ssm -L https://xx && sudo chmod +x /usr/local/bin/ssm
```

## Option
- [awsp](https://github.com/johnnyopao/awsp)

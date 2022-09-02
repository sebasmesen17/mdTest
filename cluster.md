# 1. AWS Policies
- EKS All Access
- IAM Limited Access

> [AWS docs](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html)

# 2. Group: EKS
Policies:
- EksAllAccess (Customer Managed Policy)
- IamLimitedAccess (Customer Managed Policy)
- AmazonEC2FullAccess (AWS Managed Policy)
- AWSCloudFormationFullAccess (AWS Managed Policy)

# 3. User: eksctl
- Group: EKS

## 3.1. eksctl credentials
```
KEY: xxxxxxx
SECRET: xxxxx.xxxxxxxxx
```
# 4. AWS CLI
> [Install](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
# 5. AWS Profile
```vim
aws configure --profile eksctl_lab
aws sts get-caller-identity --profile eksctl_lab
```

# 6. EKSCTL CLI
> [docs](https://eksctl.io/introduction/#installation)
```vi
brew tap weaveworks/tap
brew install weaveworks/tap/eksctl
```

# 7. Cluster Config
```vim
eksctl create cluster -f eks_config.yaml --profile eksctl_lab

# eliminar cluster
eksctl delete cluster -f eks_config.yaml --profile eksctl_lab
```




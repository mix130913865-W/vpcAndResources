# Terraform AWS Ubuntu Web Server

## 專案介紹
使用 Terraform 在 AWS 上建立 Ubuntu EC2 Web Server，包含：
- 最新 Ubuntu 22.04 AMI
- VPC 與subnet
- Security Group (SSH + HTTP)
- Key Pair（使用者提供 public key）
- 自動部署範例網頁 (Apache)

###
```terraform-aws-ubuntu-web/         # 專案根目錄
├── README.md                     # 專案說明
├── .gitignore                     # 忽略私鑰與 state
├── backend.tf                     # Terraform S3 backend 設定
├── provider.tf                    # AWS Provider 設定
├── vars.tf                        # 變數定義（region、zone、AMI 等）
├── InstID.tf                      # 取得最新 Ubuntu AMI
├── Instance.tf                     # EC2 instance 定義與 provisioner
├── keypair.tf                      # Key Pair 定義（public key）
├── SecGrp.tf                       # Security Group 定義
├── vpc.tf                          # VPC 與子網、IGW、Route Table
└── web.sh                          # 部署 Web Server 的 shell 腳本
```

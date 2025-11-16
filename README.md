# AWS EC2 Windows Server 2025 Deployment

A hands-on project demonstrating the deployment and configuration of a Microsoft Windows Server 2025 instance on Amazon EC2.

## 🎯 Project Overview

This project showcases the ability to provision and configure Windows Server infrastructure in AWS cloud environment, demonstrating practical cloud computing skills and Windows Server administration knowledge.

## 🎥 Video Walkthrough

Watch the complete deployment process:

[![AWS EC2 Windows Server Deployment](https://cdn.loom.com/sessions/thumbnails/0160c5671e2c4e0083bdafea839316f2-with-play.gif)](https://www.loom.com/share/0160c5671e2c4e0083bdafea839316f2)

**[▶️ Click here to watch the full video demonstration](https://www.loom.com/share/0160c5671e2c4e0083bdafea839316f2)**

*This video demonstrates the complete EC2 instance creation process from start to finish.*

## 🏗️ Architecture

**Cloud Provider**: Amazon Web Services (AWS)  
**Service**: Elastic Compute Cloud (EC2)  
**Operating System**: Microsoft Windows Server 2025  
**Instance Type**: t3.xlarge  
**Region**: [Your AWS Region]

## 📋 Deployment Process

### Step 1: AWS Console Access
- Navigated to AWS Management Console
- Accessed EC2 service dashboard
- Prepared for instance creation

### Step 2: Amazon Machine Image (AMI) Selection
- **Selected AMI**: Microsoft Windows Server 2025
- **Image Type**: Official AWS Windows Server AMI
- **Architecture**: 64-bit (x86)
- **Virtualization**: HVM

### Step 3: Instance Type Configuration
- **Instance Type**: t3.xlarge
- **vCPUs**: 4
- **Memory**: 16 GiB RAM
- **Network Performance**: Up to 5 Gigabit
- **EBS-Optimized**: Yes

**Rationale**: The t3.xlarge instance type provides sufficient compute resources for Windows Server workloads while maintaining cost-effectiveness.

### Step 4: Security Configuration
- Created new key pair for secure instance access
- **Key Pair Type**: RSA or ED25519
- **Format**: .pem (for OpenSSH) or .ppk (for PuTTY)
- **Purpose**: Secure RDP connection authentication

### Step 5: Instance Verification
- Verified instance successfully created
- Confirmed instance status: **Running**
- Validated instance health checks
- Confirmed public IP assignment

## 🔧 Technical Specifications

### Instance Details
```
Instance Type:     t3.xlarge
vCPUs:            4
Memory:           16 GiB
Storage:          EBS-backed
Network:          Enhanced networking
Platform:         Windows Server 2025
```

### Security Configuration
- **Key Pair**: Created for secure access
- **Security Group**: Default or custom (RDP port 3389)
- **IAM Role**: Optional (if configured)

## 🚀 Connection Methods

### Remote Desktop Protocol (RDP)
```
1. Retrieve Windows Administrator password using key pair
2. Open Remote Desktop Connection
3. Enter Public IP or DNS name
4. Authenticate with Administrator credentials
5. Connect to Windows Server desktop
```

### AWS Systems Manager Session Manager
```
Alternative connection method without opening RDP port:
- Use AWS Systems Manager for secure shell access
- No inbound ports required
- Audit trail in CloudTrail
```

## 📊 Instance Monitoring

### CloudWatch Metrics
- **CPU Utilization**: Monitor compute usage
- **Network In/Out**: Track data transfer
- **Disk Read/Write**: Storage performance
- **Status Checks**: System and instance health

### Cost Management
- **Instance Hours**: Track running time
- **Data Transfer**: Monitor bandwidth usage
- **EBS Storage**: Storage costs
- **Elastic IP**: If assigned

## 🔐 Security Best Practices

### Network Security
- ✅ Restrict RDP access to specific IP addresses
- ✅ Use Security Groups as virtual firewalls
- ✅ Enable VPC Flow Logs for network monitoring
- ✅ Consider using AWS Systems Manager instead of RDP

### Access Management
- ✅ Secure key pair storage
- ✅ Rotate passwords regularly
- ✅ Use IAM roles for AWS service access
- ✅ Enable CloudTrail for audit logging

### System Hardening
- ✅ Apply Windows Updates regularly
- ✅ Enable Windows Firewall
- ✅ Install antivirus/antimalware
- ✅ Implement least privilege access

## 💰 Cost Optimization

### Instance Management
- **Stop instances** when not in use (pay only for storage)
- **Use Reserved Instances** for long-term workloads
- **Consider Spot Instances** for flexible workloads
- **Right-size instances** based on actual usage

### Estimated Monthly Cost
```
t3.xlarge On-Demand (us-east-1):
- Instance: ~$150/month (730 hours)
- Storage: ~$10/month (100 GB EBS)
- Data Transfer: Variable
Total: ~$160+/month
```

## 🎯 Use Cases

This Windows Server instance can be used for:

- **Active Directory Domain Controller**
- **Microsoft SQL Server Database**
- **IIS Web Server Hosting**
- **File Server (SMB/CIFS)**
- **Application Server (.NET applications)**
- **Remote Desktop Services (RDS)**
- **Development/Testing Environment**

## 📈 Skills Demonstrated

### AWS Cloud Services
- ✅ EC2 instance provisioning
- ✅ AMI selection and configuration
- ✅ Instance type optimization
- ✅ Security group management
- ✅ Key pair generation and management

### Windows Server Administration
- ✅ Windows Server 2025 deployment
- ✅ Remote access configuration
- ✅ Server resource planning
- ✅ Security best practices

### Cloud Architecture
- ✅ Infrastructure planning
- ✅ Cost optimization strategies
- ✅ Security implementation
- ✅ Monitoring and management

## 🔄 Next Steps

### Immediate Actions
1. **Connect to Instance** - Use RDP with key pair
2. **Apply Updates** - Install Windows Updates
3. **Configure Firewall** - Set up Windows Firewall rules
4. **Install Software** - Deploy required applications

### Advanced Configuration
- **Join to Domain** - Active Directory integration
- **Configure Backup** - AWS Backup or snapshots
- **Set Up Monitoring** - CloudWatch alarms
- **Implement Auto Scaling** - For high availability

## 📚 AWS Services Used

- **Amazon EC2** - Virtual server hosting
- **Amazon EBS** - Block storage volumes
- **Amazon VPC** - Virtual private cloud networking
- **AWS IAM** - Identity and access management
- **Amazon CloudWatch** - Monitoring and logging

## 🛠️ Management Commands

### AWS CLI Commands
```bash
# Describe instance
aws ec2 describe-instances --instance-ids i-xxxxxxxxxxxxx

# Get Windows password
aws ec2 get-password-data --instance-id i-xxxxxxxxxxxxx --priv-launch-key /path/to/key.pem

# Stop instance
aws ec2 stop-instances --instance-ids i-xxxxxxxxxxxxx

# Start instance
aws ec2 start-instances --instance-ids i-xxxxxxxxxxxxx

# Terminate instance
aws ec2 terminate-instances --instance-ids i-xxxxxxxxxxxxx
```

### PowerShell (from within instance)
```powershell
# Check Windows version
Get-ComputerInfo | Select-Object WindowsProductName, WindowsVersion

# View system information
systeminfo

# Check network configuration
Get-NetIPConfiguration
```

## 📸 Project Documentation

### Key Screenshots to Include
- AWS EC2 Dashboard showing running instance
- Instance details page with specifications
- Security group configuration
- Remote Desktop connection
- Windows Server desktop

## 🎓 Learning Outcomes

This project demonstrates:
- **Cloud Infrastructure Deployment** - Hands-on AWS experience
- **Windows Server Administration** - Enterprise OS management
- **Security Configuration** - Best practices implementation
- **Cost Management** - Resource optimization awareness
- **Technical Documentation** - Professional project presentation

## 👨‍💻 Author

**Keenan Kelly**

This project showcases practical AWS cloud computing skills and Windows Server infrastructure deployment capabilities.

## 📄 Additional Resources

- [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2/)
- [Windows Server 2025 Documentation](https://docs.microsoft.com/windows-server/)
- [AWS Best Practices](https://aws.amazon.com/architecture/well-architected/)
- [EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/)

---

*Built on AWS Cloud Infrastructure - Demonstrating enterprise Windows Server deployment and management*
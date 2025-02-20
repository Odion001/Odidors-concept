# Odidors-concept
## How to Launch an EC2 Instance

## Prerequisites
- An AWS account
- IAM user with necessary permissions to launch an EC2 instance

### 1. Sign in to AWS Console
1. Go to [AWS Management Console](https://aws.amazon.com/console/)
2. Sign in with your AWS credentials.
3. Navigate to the **EC2 Dashboard** by searching for "EC2" in the AWS Console search bar.

### 2. Launch a New Instance
1. Click on **Instances** (under the "Instances" section) in the EC2 Dashboard.
2. Click the **Launch Instances** button.

![alt text](<Create an ec2 instance.png>)

### 3. Configure the Instance
1. **Name and Tags**
   - Provide a name for your instance.
2. **Choose an Amazon Machine Image (AMI)**
   - Select an AMI (e.g., Amazon Linux, Ubuntu, Windows Server, etc.).
3. **Choose an Instance Type**
   - Select an instance type based on your requirements (e.g., `t2.micro` for free-tier eligible instances).
4. **Key Pair (Login Authentication)**
   - Choose an existing key pair or create a new one for SSH access.
   - Download the private key (`.pem` file) and keep it secure.
5. **Network Settings**
   - Choose a VPC and subnet.
   - Configure security groups to allow necessary inbound/outbound traffic (e.g., SSH for Linux or RDP for Windows).
6. **Storage**
   - Specify the storage volume (default is usually 8GB for general-purpose AMIs).

![
](<Name the Instance.png>)

![alt text](<Choose your OS and Software (AMI).png>)
Choose the OS and Software

![alt text](<Choose your hardware .png>)
Choose the Hardware

![alt text](<Create a Keypair.png>)
Create a Key pair

![alt text](<Configure network to enable internet access.png>)

### 4. Launch the Instance
1. Review all configurations.
2. Click **Launch Instance**.
3. Wait for the instance to initialize (you can check the status in the "Instances" tab).

### 5. Connect to Your Instance
- **For Linux instances:**
  - Use SSH with the command:
    ```sh
    ssh -i /path/to/your-key.pem ec2-user@your-instance-public-ip
    ```
- **For Windows instances:**
  - Use RDP by downloading the Remote Desktop file from the AWS Console.

### 6. Manage and Monitor the Instance
- Use **CloudWatch** for monitoring.
- Manage instance state (Start, Stop, Terminate) from the EC2 dashboard.

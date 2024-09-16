# Launching-EC2-Instance
A step-by-step guide to launching and connecting to your first Amazon EC2 instance. Perfect for beginners getting started with AWS.

# Launching Your First EC2 Instance

This repository provides a step-by-step guide to launching your first Amazon EC2 instance.

## Prerequisites

- An AWS account. If you don’t have one, sign up at [AWS Free Tier](https://aws.amazon.com/free/).

## Steps to Launch an EC2 Instance

1. **Sign In to AWS Management Console**:
   - Go to the [AWS Management Console](https://aws.amazon.com/console/).
   - Sign in with your AWS account credentials.

2. **Open EC2 Dashboard**:
   - From the AWS Management Console, select **EC2** from the Services menu.

3. **Launch Instance**:
   - Click on **Launch Instance**.
   - Choose an Amazon Machine Image (AMI). For a basic setup, select the **Amazon Linux 2 AMI** or **Ubuntu**.
   - Choose an Instance Type. For a free tier, select the **t2.micro** instance.
   - Configure Instance Details. You can use default settings for a basic setup.
   - Add Storage. The default settings are typically sufficient.
   - Add Tags (optional). You can add tags for better organization.
   - Configure Security Group. Create a new security group and allow **SSH (port 22)** for remote access. Add other rules as needed.
   - Review and Launch. Click **Launch** and select an existing key pair or create a new one. Ensure you download and save the key pair (PEM file) securely.

4. **Connect to Your EC2 Instance**:
   - Go back to the **Instances** section in the EC2 dashboard.
   - Select your newly launched instance.
   - Click **Connect** and follow the instructions to connect using SSH.

     ## Connect Using MobaXterm

1. **Obtain Public IP Address**:
   - Go to the **Instances** section in the EC2 dashboard.
   - Select your newly launched instance and note its **Public IPv4 address**.
2. **Open MobaXterm**:
   - Launch MobaXterm on your computer.

3. **Start a New SSH Session**:
   - Click on **Session** in the toolbar.
   - Select **SSH**.

4. **Enter Connection Details**:
   - In the **Remote host** field, enter the **Public IPv4 address** of your EC2 instance.
   - Select **Specify username** and enter your EC2 instance’s username (e.g., `ec2-user` for Amazon Linux, `ubuntu` for Ubuntu).

5. **Load Your Private Key**:
   - Click on the **Advanced SSH settings** tab.
   - In the **Use private key** field, click **Browse** and select your PEM key file. You may need to convert it to PPK format using PuTTYgen if MobaXterm does not accept PEM files directly.

6. **Connect**:
   - Click **OK** to save the session settings.
   - Click on the saved session to connect to your EC2 instance.

## Additional Resources

- [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2/index.html)
- [Connecting to Your Instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ConnectToInstance.html)
- [MobaXterm Documentation](https://mobaxterm.mobatek.net/)

Feel free to reach out if you have any questions or need further assistance!

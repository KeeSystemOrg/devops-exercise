# DevOps Applicant Exercise: Secure Windows VM Configuration with Ansible

## Objective
Configure and secure a Windows Server environment using Ansible, demonstrating proficiency in automation, Windows administration, and advanced security practices.

## Requirements

### 1. Environment Setup
- Provision a Windows Server 2019 or later VM
  - You can use a cloud provider (e.g., AWS, Azure, GCP) or set up a VM locally using VirtualBox or similar virtualization software
- (Optional) Provision a second VM to act as an Active Directory Domain Controller

### 2. Ansible Playbook
Create an Ansible playbook that accomplishes the following tasks:

a) Basic Configuration
- Set the hostname of the Windows Server
- Configure time zone settings
- Install common utilities (your choice, but consider what a typical server might need)
- Configure SSH for Ansible connectivity

b) Security
- Configure Windows Firewall with appropriate rules for a web server environment
- Ensure necessary ports are open for server maintenance and updates
- Implement user and group management best practices:
  - Create appropriate local users and groups for segregation of duties
  - Consider the principle of least privilege when assigning permissions
  - Set up any necessary service or functional accounts
  - Implement a logical group structure that facilitates easy management and scalability
- Implement additional security measures using available Windows security tools

c) Web Server
- Install and configure IIS
- Create and deploy a simple "Hello World" HTML file that will be rendered when connecting to the VM's IP address or hostname

d) PowerShell Script
- Write a PowerShell script that checks the status of the IIS service and logs it to a file
- Use Ansible to deploy this script to the Windows Server and schedule it to run every 5 minutes using Task Scheduler

e) Package Management
- Install at least three additional software packages of your choice
- Use a declarative approach to ensure idempotency

### 3. (Optional) Active Directory Integration
If you've set up the second VM as a Domain Controller, you may use Active Directory for user and group management instead of local accounts. In this case:
- Join the Windows Server to the Active Directory domain
- Create appropriate AD users and groups that mirror the local user/group strategy described in section 2b
- Ensure proper delegation of privileges and access controls using AD

### 4. (Optional) CI/CD Pipeline
- Create a Git repository (GitHub, GitLab, or your preferred platform) for your Ansible code
- Set up a CI/CD pipeline that:
  - Lints your Ansible playbooks
  - Runs a syntax check on your playbooks
  - (Bonus) Automatically applies the playbook to a test environment when changes are pushed to the main branch

### 5. Security Self-Assessment
After completing the configuration, perform a self-assessment of the server's security posture:
- Identify potential vulnerabilities or attack vectors
- Evaluate the effectiveness of implemented security measures
- Consider whether an attacker would have a difficult time intruding into the server
- Suggest any additional security improvements that could be made

## Evaluation Criteria
- Code quality and organization
- Adherence to Ansible best practices
- Effectiveness of Windows configuration and security measures
- Creativity in solving problems and implementing security features
- Depth and breadth of security tool usage
- Thoroughness of security self-assessment
- (If applicable) Proper use of CI/CD practices

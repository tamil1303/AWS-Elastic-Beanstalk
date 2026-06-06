# Experiment: AWS Elastic Beanstalk
## AIM

* To access the AWS Elastic Beanstalk environment.
* To deploy a sample application to Elastic Beanstalk.
* To explore the AWS resources created and managed by Elastic Beanstalk.

---

# PROBLEM STATEMENT

AWS Elastic Beanstalk is a Platform as a Service (PaaS) that simplifies the deployment and management of web applications. It automatically handles infrastructure provisioning, load balancing, auto scaling, monitoring, and application deployment. This experiment demonstrates how to create an Elastic Beanstalk environment, deploy a sample application, and examine the AWS resources supporting the application.

---

# ALGORITHM

### Step 1:

Log in to the AWS Management Console and open the Elastic Beanstalk service.

### Step 2:

Click **Create Application** and enter the application name.

### Step 3:

Choose the platform (e.g., Python, Node.js, Java, PHP) and upload or select a sample application.

### Step 4:

Create an environment and wait for Elastic Beanstalk to provision the required AWS resources.

### Step 5:

Access the application URL, verify successful deployment, and explore the associated AWS resources such as EC2 instances, Load Balancer, Auto Scaling Group, and Security Groups.

---

# COMMANDS

### AWS CLI Command to Create Application

```bash
aws elasticbeanstalk create-application \
--application-name SampleWebApp
```

### Create Environment

```bash
aws elasticbeanstalk create-environment \
--application-name SampleWebApp \
--environment-name SampleWebApp-env \
--solution-stack-name "64bit Amazon Linux 2023 v4.3.1 running Python 3.11"
```

### View Environment Status

```bash
aws elasticbeanstalk describe-environments
```

### List Application Versions

```bash
aws elasticbeanstalk describe-application-versions \
--application-name SampleWebApp
```

---

# OUTPUT

## Application Details

| Property         | Value            |
| ---------------- | ---------------- |
| Application Name | SampleWebApp     |
| Environment Name | SampleWebApp-env |
| Platform         | Python 3.11      |
| Status           | Ready            |
| Health           | Green            |

---

## AWS Console Output

### Elastic Beanstalk Dashboard

```text
Application Name : SampleWebApp
Environment Name : SampleWebApp-env
Status           : Ready
Health           : Green
URL              : http://samplewebapp-env.elasticbeanstalk.com
```

---

### Environment Overview

```text
Environment Health : Green
Platform           : Python 3.11
Instances Running  : 1
Load Balancer      : Active
Auto Scaling       : Enabled
```

---

### Resources Created by Elastic Beanstalk

```text
EC2 Instance
Elastic Load Balancer
Auto Scaling Group
Security Groups
CloudWatch Alarms
S3 Bucket
```

---

### Sample Application Output

When the environment URL is opened:

```html
Congratulations!

Your AWS Elastic Beanstalk application is now running successfully.
```

---

# SCREENSHOTS TO INCLUDE

<img width="1375" height="449" alt="image" src="https://github.com/user-attachments/assets/0b63faf0-9201-4773-ba08-b63fd3e44e29" />


<img width="1370" height="466" alt="image" src="https://github.com/user-attachments/assets/e48fb6ef-482f-4d42-b26a-dc71bc534b92" />


# RESULT

The AWS Elastic Beanstalk environment was successfully created, and a sample application was deployed. The application was accessed through the generated URL, and the supporting AWS resources such as EC2 Instance, Load Balancer, Auto Scaling Group, and Security Groups were explored successfully. Thus, the objectives of deploying and managing an application using AWS Elastic Beanstalk were achieved.

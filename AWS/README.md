
Amazon Web Services Security Control Mappings to MITRE ATT&CK®
==============================================================


These mappings of the Amazon Web Services (AWS) security controls to MITRE ATT&CK® are designed to empower organizations with independent data on which native AWS security controls are most useful in defending against the adversary TTPs that they care about. These mappings are part of a collection of mappings of native product security controls to ATT&CK based on a common methodology, scoring rubric, data model, and tool set. This full set of resources is available on the Center’s project [page](https://ctid.mitre-engenuity.org/our-work/security-stack-mappings-aws/).

[Aggregate Navigator Layer For All Controls (JSON)](layers/platform.json)

# <a name='contents'>Contents</a>

* Controls
    * [1. AWS Artifact](#aws-artifact)
    * [2. AWS Audit Manager](#aws-audit-manager)
    * [3. AWS Certificate Manager](#aws-certificate-manager)
    * [4. AWS CloudEndure Disaster Recovery](#aws-cloudendure-disaster-recovery)
    * [5. AWS CloudHSM](#aws-cloudhsm)
    * [6. AWS CloudTrail](#aws-cloudtrail)
    * [7. AWS CloudWatch](#aws-cloudwatch)
    * [8. AWS Config](#aws-config)
    * [9. AWS Directory Service](#aws-directory-service)
    * [10. AWS Firewall Manager](#aws-firewall-manager)
    * [11. AWS Identity and Access Management](#aws-identity-and-access-management)
    * [12. AWS IoT Device Defender](#aws-iot-device-defender)
    * [13. AWS Key Management Service](#aws-key-management-service)
    * [14. AWS Network Firewall](#aws-network-firewall)
    * [15. AWS Organizations](#aws-organizations)
    * [16. AWS RDS](#aws-rds)
    * [17. AWS Resource Access Manager](#aws-resource-access-manager)
    * [18. AWS S3](#aws-s3)
    * [19. AWS Secrets Manager](#aws-secrets-manager)
    * [20. AWS Security Hub](#aws-security-hub)
    * [21. AWS Shield](#aws-shield)
    * [22. AWS Single Sign-On](#aws-single-sign-on)
    * [23. AWS Web Application Firewall](#aws-web-application-firewall)
    * [24. Amazon Cognito](#amazon-cognito)
    * [25. Amazon Detective](#amazon-detective)
    * [26. Amazon GuardDuty](#amazon-guardduty)
    * [27. Amazon Inspector](#amazon-inspector)
    * [28. Amazon Macie](#amazon-macie)
    * [29. Amazon Virtual Private Cloud](#amazon-virtual-private-cloud)
* Control Tags
    * [1. Auditing](#tag-auditing)
    * [2. Credentials](#tag-credentials)
    * [3. Database](#tag-database)
    * [4. Denial of Service](#tag-denial-of-service)
    * [5. Identity](#tag-identity)
    * [6. Internet of Things](#tag-internet-of-things)
    * [7. IoT](#tag-iot)
    * [8. Metrics](#tag-metrics)
    * [9. Network](#tag-network)
    * [10. Not Mappable](#tag-not-mappable)
    * [11. Reports](#tag-reports)
    * [12. Storage](#tag-storage)

# Controls
<a name='aws-artifact'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 1. AWS Artifact



AWS Artifact is a central resource that provides on-demand access to AWS's security and compliance reports and online agreements. Available reports include Service Organization Control (SOC) reports, Payment Card Industry (PCI) reports, and certifications from accreditation bodies across geographies and compliance verticals that validate the implementation and operating effectiveness of AWS security controls. Agreements available include the Business Associate Addendum (BAA) and the Nondisclosure Agreement (NDA).

- [Mapping File](AWSArtifact.yaml) ([YAML](AWSArtifact.yaml))
- [Navigator Layer](layers/AWSArtifact.json) ([JSON](layers/AWSArtifact.json))

### Mapping Comments


This control was not mapped because AWS Artifact provides access to reports and information but does not protect against any ATT&CK techniques. All protections against ATT&CK techniques are provided by the lower-level services evaluated by and referenced in those reports.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
  


### Tags
- [Not Mappable](#tag-not-mappable)
  


### References
- <https://aws.amazon.com/artifact>
- <https://docs.aws.amazon.com/artifact>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-audit-manager'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 2. AWS Audit Manager



AWS Audit Manager automates evidence collection from other services (notably AWS Config, AWS Security Hub, AWS API calls, and AWS CloudTrail) for evaluation against compliance frameworks/regulations and transformation into audit-friendly reports.

- [Mapping File](AWSAuditManager.yaml) ([YAML](AWSAuditManager.yaml))
- [Navigator Layer](layers/AWSAuditManager.json) ([JSON](layers/AWSAuditManager.json))

### Mapping Comments


This control was not mapped because AWS Audit Manager is used to aggregate evidence from other services in order to produce audit-ready reports, not provide protection against any ATT&CK techniques or adversary behaviors. All protections against ATT&CK techniques are provided by the lower-level services used for the evidence collection, which are assessed in different mappings.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
  


### Tags
- [Auditing](#tag-auditing)
- [Not Mappable](#tag-not-mappable)
- [Reports](#tag-reports)
  


### References
- <https://aws.amazon.com/audit-manager>
- <https://docs.aws.amazon.com/audit-manager>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-certificate-manager'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 3. AWS Certificate Manager



AWS Certificate Manager is an Amazon service that supports the creation, storage, and renewal of public and private SSL/TLS X.509 certificates and keys that protect AWS websites and applications.

- [Mapping File](AWSCertificateManager.yaml) ([YAML](AWSCertificateManager.yaml))
- [Navigator Layer](layers/AWSCertificateManager.json) ([JSON](layers/AWSCertificateManager.json))

### Mapping Comments


This control was not mapped because AWS Certificate Manager simply issues certificates for use in other AWS services such as Elastic Load Balancing, Amazon CloudFront, AWS Elastic Beanstalk, Amazon API Gateway, AWS Nitro Enclaves, and AWS CloudFormation. It does not inherently protect against any ATT&CK techniques as it cannot be used to deploy certificates to other AWS services. That must be done either manually or with services integrated into AWS Certificate Manager.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
  


### Tags
- [Credentials](#tag-credentials)
- [Not Mappable](#tag-not-mappable)
  


### References
- <https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html>
- <https://aws.amazon.com/certificate-manager/faqs/?nc=sn&loc=5>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-cloudendure-disaster-recovery'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 4. AWS CloudEndure Disaster Recovery



AWS CloudEndure Disaster Recovery enables the replication and recovery of physical, virtual, and cloud-based servers into AWS Cloud including public regions, AWS GovCloud, and AWS Outposts. AWS CloudEndure continuously replicates servers and can launch fully provisioned machines within minutes in the event that a disaster such as data center failures, server corruption, or cyber attacks occur.



- [Mapping File](AWSCloudEndure.yaml) ([YAML](AWSCloudEndure.yaml))
- [Navigator Layer](layers/AWSCloudEndure.json) ([JSON](layers/AWSCloudEndure.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1190 - Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)|Respond|Significant|AWS CloudEndure Disaster Recovery enables the replication and recovery of servers into AWS Cloud. In the event that a public-facing application or server is compromised, AWS CloudEndure can be used to provision an instance of the server from a previous point in time within minutes. As a result, this mapping is given a score of Significant.|
|[T1485 - Data Destruction](https://attack.mitre.org/techniques/T1485/)|Respond|Significant|AWS CloudEndure Disaster Recovery enables the replication and recovery of servers into AWS Cloud. In the event that data on servers is destroyed, AWS CloudEndure can be used to provision an instance of the server from a previous point in time within minutes. As a result, this mapping is given a score of Significant.|
|[T1486 - Data Encrypted for Impact](https://attack.mitre.org/techniques/T1486/)|Respond|Significant|AWS CloudEndure Disaster Recovery enables the replication and recovery of servers into AWS Cloud. In the event that data on servers is encrypted (e.g., ransomware), AWS CloudEndure can be used to provision an instance of the server from a previous point in time within minutes. As a result, this mapping is given a score of Significant.<br/>|
|[T1490 - Inhibit System Recovery](https://attack.mitre.org/techniques/T1490/)|Respond|Significant|AWS CloudEndure Disaster Recovery enables the replication and recovery of servers into AWS Cloud. In the event that servers are modified to disrupt recovery, AWS CloudEndure can be used to provision an instance of the server from a previous point in time within minutes. As a result, this mapping is given a score of Significant.|
|[T1491 - Defacement](https://attack.mitre.org/techniques/T1491/)|Respond|Significant|AWS CloudEndure Disaster Recovery enables the replication and recovery of servers into AWS Cloud. In the event that servers are defaced, AWS CloudEndure can be used to provision an instance of the server from a previous point in time within minutes. This mapping is given a score of Significant because it supports all of the sub-techniques (2 of 2).|
|[T1561 - Disk Wipe](https://attack.mitre.org/techniques/T1561/)|Respond|Significant|AWS CloudEndure Disaster Recovery enables the replication and recovery of servers into AWS Cloud. In the event that server disks are wiped, AWS CloudEndure can be used to provision an instance of the server from a previous point in time within minutes. This mapping is given a score of Significant because it supports all of the sub-techniques (2 of 2).|
|[T1565 - Data Manipulation](https://attack.mitre.org/techniques/T1565/)|Respond|Minimal|AWS CloudEndure Disaster Recovery enables the replication and recovery of servers into AWS Cloud. In the event that data on servers is manipulated, AWS CloudEndure can be used to provision an instance of the server from a previous point in time within minutes. This mapping is given a score of Minimal because it only supports a subset (1 of 3) of the sub-techniques.<br/>|
  


### References
- <https://aws.amazon.com/cloudendure-disaster-recovery/>
- <https://docs.cloudendure.com/#Configuring_and_Running_Disaster_Recovery/Configuring_and_Running_Disaster_Recovery.htm>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-cloudhsm'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 5. AWS CloudHSM



AWS CloudHSM provides hardware security modules (HSM) in the AWS Cloud.  Using this service allows generating, storing, importing, exporting, and managing cryptographic keys, including symmetric keys and asymmetric key pairs.

- [Mapping File](AWSCloudHSM.yaml) ([YAML](AWSCloudHSM.yaml))
- [Navigator Layer](layers/AWSCloudHSM.json) ([JSON](layers/AWSCloudHSM.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1552 - Unsecured Credentials](https://attack.mitre.org/techniques/T1552/)|Protect|Minimal|This control's protection is specific to a minority of this technique's sub-techniques and procedure examples resulting in a Minimal Coverage score and consequently an overall score of Minimal.|
|[T1553 - Subvert Trust Controls](https://attack.mitre.org/techniques/T1553/)|Protect|Partial|This service provides protection against sub-techniques involved with stealing credentials, certificates, and keys from the organization.|
|[T1588 - Obtain Capabilities](https://attack.mitre.org/techniques/T1588/)|Protect|Partial|This service provides protection against sub-techniques involved with stealing credentials, certificates, keys from the organization.|
  


### Tags
- [Credentials](#tag-credentials)
  


### References
- <https://aws.amazon.com/cloudhsm/>
- <https://docs.aws.amazon.com/cloudhsm/latest/userguide/use-cases.html>
- <https://docs.aws.amazon.com/cloudhsm/latest/userguide/introduction.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-cloudtrail'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 6. AWS CloudTrail



AWS CloudTrail is an AWS service that helps you enable governance, compliance, and operational and risk auditing of your AWS account. Actions taken by a user, role, or an AWS service are recorded as events in CloudTrail.

- [Mapping File](AWSCloudTrail.yaml) ([YAML](AWSCloudTrail.yaml))
- [Navigator Layer](layers/AWSCloudTrail.json) ([JSON](layers/AWSCloudTrail.json))

### Mapping Comments


This control is not mappable because it does not provide any detection of malicious techniques. It primarily provides a way to log and record events within AWS which then can be piped to other security controls to determine if malicious activity has occurred.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
  


### Tags
- [Not Mappable](#tag-not-mappable)
  


### References
- <https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-cloudwatch'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 7. AWS CloudWatch



AWS CloudWatch monitors resources, applications, and services to collect and track metrics in real-time. These metrics provide visibility into resource utilization, performance, and health. AWS CloudWatch integrates with over 70 AWS services including Amazon EC2, Amazon S3, and Amazon ECS among others. 


- [Mapping File](AWSCloudWatch.yaml) ([YAML](AWSCloudWatch.yaml))
- [Navigator Layer](layers/AWSCloudWatch.json) ([JSON](layers/AWSCloudWatch.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1040 - Network Sniffing](https://attack.mitre.org/techniques/T1040/)|Protect|Significant|AWS CloudWatch uses TLS/SSL connections to communicate with other AWS resources which protects against network sniffing attacks. As a result, this mapping is given a score of Significant.|
|[T1496 - Resource Hijacking](https://attack.mitre.org/techniques/T1496/)|Detect|Partial|AWS CloudWatch provides various metrics including CPU utilization, connections, disk space, memory, bytes sent/received, and the number of running containers among others. The following metrics (not an exhaustive list) could be used to detect if the usage of a resource has increased such as when an adversary hijacks a resource to perform intensive tasks.<br/>Linux/Mac OS ------------- cpu_time_active cpu_time_guest cpu_usage_active cpu_usage_guest disk_free disk_total disk_used ethtool_bw_in_allowance_exceeded ethtool_bw_out_allowance_exceeded ethtool_conntrack_allowance_exceeded mem_active mem_available_percent mem_free net_bytes_recv net_bytes_sent net_packets_sent net_packets_recv netstat_tcp_established netstat_tcp_listen processes_running processes_total swap_free swap_used<br/>Containers ---------- CpuUtilized MemoryUtilized NetworkRxBytes NetworkTxBytes node_cpu_usage_total node_cpu_utilization node_filesystem_utilization node_memory_utilization<br/>This mapping is given a score of Partial because it is not possible to differentiate between an authorized and unauthorized increase in resource utilization.|
|[T1610 - Deploy Container](https://attack.mitre.org/techniques/T1610/)|Detect|Partial|AWS CloudWatch provides various metrics including CPU utilization, connections, disk space, memory, bytes sent/received, and the number of running containers among others. The following metric could be used to detect if an adversary deployed a new container in the environment. <br/>node_number_of_running_containers<br/>This mapping is given a score of Partial because it is not possible to differentiate between an authorized and unauthorized deployment of a new container.|
  


### Tags
- [Metrics](#tag-metrics)
  


### References
- <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-config'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 8. AWS Config



AWS Config rules evaluate the configuration settings of AWS resources in order to detect resources that are out of compliance with internal policies and best practices.

- [Mapping File](AWSConfig.yaml) ([YAML](AWSConfig.yaml))
- [Navigator Layer](layers/AWSConfig.json) ([JSON](layers/AWSConfig.json))

### Mapping Comments


Mappings are based on the set of AWS managed rules provided by AWS Config, which are predefined rules that AWS Config uses to test for compliance with common best practices.
AWS Config rules can be set to one of two types, "configuration changes" and "periodic", which are evaluated upon configuration changes and at a user-defined period, respectively.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1020 - Automated Exfiltration](https://attack.mitre.org/techniques/T1020/)|Protect|Minimal|This control provides partial coverage for this technique's only sub-technique, but without specific coverage for its procedures, resulting in an overall score of Minimal.|
|[T1040 - Network Sniffing](https://attack.mitre.org/techniques/T1040/)|Protect|Partial|The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure SSL/TLS encryption is enabled to protect network traffic: "acm-certificate-expiration-check" for nearly expired certificates in AWS Certificate Manager (ACM); "alb-http-to-https-redirection-check" for Application Load Balancer (ALB) HTTP listeners; "api-gw-ssl-enabled" for API Gateway REST API stages; "cloudfront-custom-ssl-certificate", "cloudfront-sni-enabled", and "cloudfront-viewer-policy-https", for Amazon CloudFront distributions; "elb-acm-certificate-required", "elb-custom-security-policy-ssl-check", "elb-predefined-security-policy-ssl-check", and "elb-tls-https-listeners-only" for Elastic Load Balancing (ELB) Classic Load Balancer listeners; "redshift-require-tls-ssl" for Amazon Redshift cluster connections to SQL clients; "s3-bucket-ssl-requests-only" for requests for S3 bucket contents; and "elasticsearch-node-to-node-encryption-check" for Amazon ElasticSearch Service node-to-node communications.<br/>The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure that private traffic is routed securely and only within VPCs rather than on the public Internet: "api-gw-endpoint-type-check" for Amazon API Gateway APIs, "elasticsearch-in-vpc-only" for Amazon ElasticSearch Service domains, and "redshift-enhanced-vpc-routing-enabled" for Amazon Redshift cluster traffic.<br/>All of these are run on configuration changes except "alb-http-to-https-redirection-check" and "elasticsearch-in-vpc-only", which are run periodically. Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services and can only mitigate behavior for adversaries who are unable to decrypt the relevant traffic and/or do not have access to traffic within the relevant VPCs, resulting in an overall score of Partial.|
|[T1053 - Scheduled Task/Job](https://attack.mitre.org/techniques/T1053/)|Protect|Minimal|This control provides partial coverage for one of this technique's sub-techniques, resulting in an overall score of Minimal.|
|[T1068 - Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068/)|Protect|Partial|The "ec2-managedinstance-applications-blacklisted" managed rule verifies that a pre-defined list of applications are not installed on specified managed instances. It can be used to identify the presence of vulnerable applications (prompting removal before they can be exploited) and/or to identify the presence of allowed packages below a minimum version (prompting updates before they can be exploited). The "ec2-managedinstance-platform-check" managed rule verifies that managed instances are running desired platform types, including using a desired version (as opposed to an out-of-date one). Both can reduce instances' attack surface for adversary exploitation, including for privilege escalation.<br/>The "ecs-task-definition-user-for-host-mode-check" managed rule can identify Amazon Elastic Container Service (ECS) task definitions for containers with host networking mode and 'privileged' or 'user' container definitions, which may enable adversaries to break out of containers and gain access to the underlying host, increasing their access and privileges.<br/>All of these are run on configuration changes. Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services and will only protect against certain forms of identifiable exploitation, resulting in an overall score of Partial.|
|[T1078 - Valid Accounts](https://attack.mitre.org/techniques/T1078/)|Protect|Minimal|This control provides significant coverage for one of this technique's sub-techniques, resulting in an overall score of Minimal.|
|[T1098 - Account Manipulation](https://attack.mitre.org/techniques/T1098/)|Protect|Minimal|This control provides significant coverage for one of this technique's sub-techniques, resulting in an overall score of Minimal.|
|[T1110 - Brute Force](https://attack.mitre.org/techniques/T1110/)|Protect|Significant|This control provides significant coverage for all of this technique's sub-techniques, resulting in an overall score of Significant.|
|[T1119 - Automated Collection](https://attack.mitre.org/techniques/T1119/)|Protect|Minimal|The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure that storage volumes are encrypted, which may mitigate adversary attempts to automate collection within cloud environments: "ec2-ebs-encryption-by-default" which is run periodically and "encrypted-volumes" which is run on configuration changes.<br/>Coverage factor is minimal for these rules, since they are specific to EBS volumes and will only prevent certain forms of collection since adversaries with access to mounted volumes may be able to decrypt their contents, resulting in an overall score of Minimal.|
|[T1136 - Create Account](https://attack.mitre.org/techniques/T1136/)|Protect|Minimal|This control provides partial coverage for one of this technique's sub-techniques, resulting in an overall score of Minimal.|
|[T1190 - Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)|Protect|Partial|The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure that applications intended for internal use cannot be accessed externally for exploitation: "api-gw-endpoint-type-check" can ensure that Amazon API Gateway APIs are private and can only be accessed from within VPCs, "elasticsearch-in-vpc-only" can ensure that Amazon ElasticSearch Service (Amazon ES) domains are in the same VPC and the domain endpoint is not public, "lambda-function-public-access-prohibited" can verify that AWS Lambda functions are not publicly available, and "ec2-instance-no-public-ip" can verify whether EC2 instances have public IP addresses.<br/>The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure that insecure applications are not installed and installed packages are kept updated, reducing the likelihood of adversary exploitation: the "ec2-managedinstance-applications-blacklisted" managed rule verifies that a pre-defined list of applications are not installed on specified managed instances. It can be used to identify the presence of vulnerable applications (prompting removal before they can be exploited) and/or to identify the presence of allowed packages below a minimum version (prompting updates before they can be exploited). The "ec2-managedinstance-platform-check" managed rule verifies that managed instances are running desired platform types, including using a desired version (as opposed to an out-of-date one). Both can reduce instances' attack surface for adversary exploitation. "rds-automatic-minor-version-upgrade-enabled" can verify that Amazon RDS is being patched, and "elastic-beanstalk-managed-updates-enabled" can verify that Elastic Beanstalk is being patched.<br/>Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services that can be used to host public-facing applications and will only protect against certain forms of identifiable exploitation, resulting in an overall score of Partial.|
|[T1203 - Exploitation for Client Execution](https://attack.mitre.org/techniques/T1203/)|Protect|Partial|The "ec2-managedinstance-applications-blacklisted" managed rule verifies that a pre-defined list of applications are not installed on specified managed instances. It can be used to identify the presence of vulnerable applications (prompting removal before they can be exploited) and/or to identify the presence of allowed packages below a minimum version (prompting updates before they can be exploited). The "ec2-managedinstance-platform-check" managed rule verifies that managed instances are running desired platform types, including using a desired version (as opposed to an out-of-date one). Both can reduce instances' attack surface for adversary exploitation, including for client execution.<br/>All of these are run on configuration changes. Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services and will only protect against certain forms of identifiable exploitation, resulting in an overall score of Partial.|
|[T1204 - User Execution](https://attack.mitre.org/techniques/T1204/)|Detect|Minimal|This control provides significant coverage for one of this technique's sub-techniques, resulting in an overall score of Minimal.|
|[T1210 - Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210/)|Protect|Partial|The "ec2-managedinstance-applications-blacklisted" managed rule verifies that a pre-defined list of applications are not installed on specified managed instances. It can be used to identify the presence of vulnerable applications (prompting removal before they can be exploited) and/or to identify the presence of allowed packages below a minimum version (prompting updates before they can be exploited), both of which can reduce instances' attack surface for adversary exploitation, including via those applications' exposed remote services. The "ec2-instance-no-public-ip" managed rule identifies EC2 instances with public IP associations, which should be removed unless necessary to avoid exposing services publicly for adversary access.<br/>All of these are run on configuration changes. Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services and will only protect against certain forms of identifiable exploitation, resulting in an overall score of Partial.|
|[T1211 - Exploitation for Defense Evasion](https://attack.mitre.org/techniques/T1211/)|Protect|Partial|The "ec2-managedinstance-applications-blacklisted" managed rule verifies that a pre-defined list of applications are not installed on specified managed instances. It can be used to identify the presence of vulnerable applications (prompting removal before they can be exploited) and/or to identify the presence of allowed packages below a minimum version (prompting updates before they can be exploited). The "ec2-managedinstance-platform-check" managed rule verifies that managed instances are running desired platform types, including using a desired version (as opposed to an out-of-date one). Both can reduce instances' attack surface for adversary exploitation, including for defense evasion.<br/>All of these are run on configuration changes. Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services and will only protect against certain forms of identifiable exploitation, resulting in an overall score of Partial.|
|[T1212 - Exploitation for Credential Access](https://attack.mitre.org/techniques/T1212/)|Protect|Partial|The "ec2-managedinstance-applications-blacklisted" managed rule verifies that a pre-defined list of applications are not installed on specified managed instances. It can be used to identify the presence of vulnerable applications (prompting removal before they can be exploited) and/or to identify the presence of allowed packages below a minimum version (prompting updates before they can be exploited). The "ec2-managedinstance-platform-check" managed rule verifies that managed instances are running desired platform types, including using a desired version (as opposed to an out-of-date one).Both can reduce instances' attack surface for adversary exploitation, including for credential access.<br/>All of these are run on configuration changes. Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services and will only protect against certain forms of identifiable exploitation, resulting in an overall score of Partial.|
|[T1485 - Data Destruction](https://attack.mitre.org/techniques/T1485/)|Protect|Partial|The following AWS Config managed rules can identify configuration problems that should be fixed in order to prevent malicious write access to data within Amazon Simple Storage Service (S3) storage, which may include data destruction: "s3-bucket-blacklisted-actions-prohibited" checks whether bucket policies prohibit disallowed actions (including S3:DeleteObject) for principals from other AWS accounts, "s3-bucket-default-lock-enabled" checks whether a bucket that should be locked in write-once-read-many (WORM) mode is configured to prevent modification, and "s3-bucket-public-write-prohibited" checks whether a bucket is configured to allow public access and modification. All of these controls are run on configuration changes.<br/>The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure backups and redundancy are in place which can mitigate the effects of data destruction: "aurora-mysql-backtracking-enabled" for data in Aurora MySQL; "db-instance-backup-enabled" and "rds-in-backup-plan" for Amazon Relational Database Service (RDS) data; "dynamodb-in-backup-plan" and "dynamodb-pitr-enabled" for Amazon DynamoDB table contents; "ebs-in-backup-plan" for Elastic Block Store (EBS) volumes; "efs-in-backup-plan" for Amazon Elastic File System (EFS) file systems; "elasticache-redis-cluster-automatic-backup-check" for Amazon ElastiCache Redis cluster data; "redshift-backup-enabled" and "redshift-cluster-maintenancesettings-check" for Redshift; "s3-bucket-replication-enabled" and "s3-bucket-versioning-enabled" for S3 storage; and "cloudfront-origin-failover-enabled" for CloudFront.<br/>The following AWS Config managed rules provide specific detections for configuration problems that should be fixed in order to prevent malicious deletion of specific data: "elb-deletion-protection-enabled" for Elastic Block Store (EBS) volumes, and "rds-cluster-deletion-protection-enabled" and "rds-instance-deletion-protection-enabled" for RDS data.<br/>Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services and will only protect certain types of data against destruction, resulting in an overall score of Partial.|
|[T1486 - Data Encrypted for Impact](https://attack.mitre.org/techniques/T1486/)|Protect|Partial|The following AWS Config managed rules can identify configuration problems that should be fixed in order to prevent malicious changes to data encryption within Amazon Simple Storage Service (S3) storage: "s3-bucket-blacklisted-actions-prohibited" checks whether bucket policies prohibit disallowed actions (including encryption configuration changes) for principals from other AWS accounts, "s3-bucket-default-lock-enabled" checks whether a bucket that should be locked in write-once-read-many (WORM) mode is configured to prevent modification, and "s3-bucket-public-write-prohibited" checks whether a bucket is configured to allow public access and modification. All of these controls are run on configuration changes.<br/>The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure backups and redundancy are in place which can mitigate the effects of malicious changes to data encryption: "aurora-mysql-backtracking-enabled" for data in Aurora MySQL; "db-instance-backup-enabled" and "rds-in-backup-plan" for Amazon Relational Database Service (RDS) data; "dynamodb-in-backup-plan" and "dynamodb-pitr-enabled" for Amazon DynamoDB table contents; "ebs-in-backup-plan" for Elastic Block Store (EBS) volumes; "efs-in-backup-plan" for Amazon Elastic File System (EFS) file systems; "elasticache-redis-cluster-automatic-backup-check" for Amazon ElastiCache Redis cluster data; "redshift-backup-enabled" and "redshift-cluster-maintenancesettings-check" for Redshift; "s3-bucket-replication-enabled" and "s3-bucket-versioning-enabled" for S3 storage; and "cloudfront-origin-failover-enabled" for CloudFront.<br/>Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services and will only protect certain types of data against malicious encryption changes, resulting in an overall score of Partial.|
|[T1491 - Defacement](https://attack.mitre.org/techniques/T1491/)|Protect|Significant|This control provides significant coverage for all of this technique's sub-techniques, resulting in an overall score of Significant.|
|[T1496 - Resource Hijacking](https://attack.mitre.org/techniques/T1496/)|Detect|Partial|The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure alarms exist for spikes in resource utilization, which help to identify malicious use of resources within a cloud environment: "cloudwatch-alarm-action-check", "cloudwatch-alarm-resource-check", "cloudwatch-alarm-settings-check", "desired-instance-tenancy", "desired-instance-type", "dynamodb-autoscaling-enabled", "dynamodb-throughput-limit-check", "ec2-instance-detailed-monitoring-enabled", and "rds-enhanced-monitoring-enabled".<br/>Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services and will only detect resource hijacking that results in a change in utilization that is significant enough to trigger alarms, resulting in an overall score of Partial.|
|[T1498 - Network Denial of Service](https://attack.mitre.org/techniques/T1498/)|Protect|Minimal|This control provides minimal coverage for this technique's sub-techniques as well as its procedures, resulting in an overall score of Minimal.|
|[T1499 - Endpoint Denial of Service](https://attack.mitre.org/techniques/T1499/)|Protect|Minimal|This control provides minimal coverage for this technique's sub-techniques as well as its procedures, resulting in an overall score of Minimal.|
|[T1525 - Implant Internal Image](https://attack.mitre.org/techniques/T1525/)|Detect|Minimal|The following AWS Config managed rules can identify running instances that are not using AMIs within a specified allow list: "approved-amis-by-id" and "approved-amis-by-tag", both of which are run on configuration changes. This does not provide detection of the image implanting itself, but does provide detection for any subsequent use of images that are implanted and not present within the allow list, resulting in a score of Minimal.|
|[T1530 - Data from Cloud Storage Object](https://attack.mitre.org/techniques/T1530/)|Protect|Significant|The following AWS Config managed rules can identify configuration problems that should be fixed in order to prevent malicious access of data within Amazon Simple Storage Service (S3) storage: "s3-account-level-public-access-blocks", "s3-bucket-level-public-access-prohibited", "s3-bucket-public-read-prohibited", "s3-bucket-policy-not-more-permissive", "cloudfront-origin-access-identity-enabled", and "cloudfront-default-root-object-configured" identify objects that are publicly available or subject to overly permissive access policies; "s3-bucket-blacklisted-actions-prohibited" checks whether bucket policies prohibit disallowed actions for principals from other AWS accounts; and "s3-bucket-policy-grantee-check" checks whether bucket policies appropriately control which AWS principals, federated users, service principals, IP addresses, and VPCs have access. All of these controls are run on configuration changes.<br/>The following AWS Config managed rules can identify configuration problems that should be fixed in order to prevent malicious access of data from other AWS services: "dms-replication-not-public" for AWS Database Migration Service; "emr-master-no-public-ip" for Amazon Elastic MapReduce (EMR); "rds-cluster-iam-authentication-enabled", "rds-instance-iam-authentication-enabled", "rds-instance-public-access-check" and "rds-snapshots-public-prohibited" for Amazon Relational Database Service; "redshift-cluster-public-access-check" for Amazon Redshift; and "sagemaker-notebook-no-direct-internet-access" for SageMaker.<br/>The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure that cloud storage data are encrypted to prevent malicious access: "dax-encryption-enabled", "dynamodb-table-encrypted-kms", and "dynamodb-table-encryption-enabled" for Amazon DynamoDB table contents; "efs-encrypted-check" for Amazon Elastic File System (EFS) file systems; "elasticsearch-encrypted-at-rest" for Elasticsearch Service (ES) domains; "rds-snapshot-encrypted" and "rds-storage-encrypted" for Amazon Relational Database Service; "s3-bucket-server-side-encryption-enabled" and "s3-default-encryption-kms" for S3 storage; "sns-encrypted-kms" for Amazon Simple Notification Service (SNS); "redshift-cluster-configuration-check" and "redshift-cluster-kms-enabled" for Redshift clusters; "sagemaker-endpoint-configuration-kms-key-configured" and "sagemaker-notebook-instance-kms-key-configured" for SageMaker.<br/>These rules provide a wide range of coverage for many AWS services, especially those most significant to procedures for this technique, resulting in an overall score of Significant.|
|[T1538 - Cloud Service Dashboard](https://attack.mitre.org/techniques/T1538/)|Protect|Significant|The "mfa-enabled-for-iam-console-access" managed rule checks whether multi-factor authentication is enabled for all AWS IAM users that use a console password, protecting against misuse of those accounts' dashboard access. It is run periodically, and provides significant coverage, resulting in an overall score of Significant.|
|[T1552 - Unsecured Credentials](https://attack.mitre.org/techniques/T1552/)|Protect|Partial|The following AWS Config managed rules can identify insecure plaintext credentials within specific parts of a cloud environment: "codebuild-project-envvar-awscred-check" for credentials (AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY) stored within environment variables, "codebuild-project-source-repo-url-check" for personal access tokens and/or credentials within source repository URLs.<br/>The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure that the contents of secrets in AWS Secrets Manager (including credentials) are properly secured to avoid adversary access: "secretsmanager-rotation-enabled-check", "secretsmanager-scheduled-rotation-success-check", "secretsmanager-secret-periodic-rotation", and "secretsmanager-using-cmk".<br/>This control provides partial coverage for a minority of this technique's sub-techniques, in addition to the parent coverage above, resulting in an overall score of Partial.|
|[T1557 - Man-in-the-Middle](https://attack.mitre.org/techniques/T1557/)|Protect|Minimal|The following AWS Config managed rules can identify configuration problems that should be fixed in order to ensure SSL/TLS encryption is enabled to protect network traffic: "acm-certificate-expiration-check" for nearly expired certificates in AWS Certificate Manager (ACM); "alb-http-to-https-redirection-check" for Application Load Balancer (ALB) HTTP listeners; "api-gw-ssl-enabled" for API Gateway REST API stages; "cloudfront-custom-ssl-certificate", "cloudfront-sni-enabled", and "cloudfront-viewer-policy-https", for Amazon CloudFront distributions; "elb-acm-certificate-required", "elb-custom-security-policy-ssl-check", "elb-predefined-security-policy-ssl-check", and "elb-tls-https-listeners-only" for Elastic Load Balancing (ELB) Classic Load Balancer listeners; "redshift-require-tls-ssl" for Amazon Redshift cluster connections to SQL clients; "s3-bucket-ssl-requests-only" for requests for S3 bucket contents; and "elasticsearch-node-to-node-encryption-check" for Amazon ElasticSearch Service node-to-node communications.<br/>All of these are run on configuration changes except "alb-http-to-https-redirection-check", which is run periodically. Coverage factor is partial for these rules, since they are specific to a subset of the available AWS services and can only mitigate behavior for adversaries who are unable to decrypt the relevant traffic. This control does not provide specific coverage for this technique's sub-techniques, resulting in an overall score of Minimal.|
|[T1562 - Impair Defenses](https://attack.mitre.org/techniques/T1562/)|Detect|Minimal|This control provides significant coverage for a minority of this technique's sub-techniques, resulting in an overall score of Minimal.|
|[T1609 - Container Administration Command](https://attack.mitre.org/techniques/T1609/)|Protect|Partial|The "eks-endpoint-no-public-access" managed rule can identify whether Amazon Elastic Kubernetes Service (Amazon EKS) endpoints are misconfigured to allow public endpoint access, which should be fixed in order to prevent malicious external access to the Kubernetes API server, including malicious attempts to execute commands via the API. It is run periodically and only provides partial coverage because it is specific to public access, resulting in an overall score of Partial.|
|[T1610 - Deploy Container](https://attack.mitre.org/techniques/T1610/)|Protect|Partial|The "eks-endpoint-no-public-access" managed rule can identify whether Amazon Elastic Kubernetes Service (Amazon EKS) endpoints are misconfigured to allow public endpoint access, which should be fixed in order to prevent malicious external access to the Kubernetes API server, including malicious attempts to deploy containers. It is run periodically and only provides partial coverage because it is specific to public access, resulting in an overall score of Partial.|
|[T1611 - Escape to Host](https://attack.mitre.org/techniques/T1611/)|Protect|Partial|The "ecs-task-definition-user-for-host-mode-check" managed rule can identify Amazon Elastic Container Service (ECS) task definitions for containers with host networking mode and 'privileged' or 'user' container definitions, which may enable adversaries to break out of containers and gain access to the underlying host. It is run on configuration changes. Coverage is partial, since adversaries may find other means to escape a container to the underlying host, resulting in an overall score of Partial.|
|[T1613 - Container and Resource Discovery](https://attack.mitre.org/techniques/T1613/)|Protect|Partial|The "eks-endpoint-no-public-access" managed rule can identify whether Amazon Elastic Kubernetes Service (Amazon EKS) endpoints are misconfigured to allow public endpoint access, which should be fixed in order to prevent malicious external access to the Kubernetes API server, including malicious attempts to discover containers and other resources. It is run periodically and only provides partial coverage because it is specific to public access, resulting in an overall score of Partial.|
  


### References
- <https://docs.aws.amazon.com/config>
- <https://docs.aws.amazon.com/config/latest/developerguide>
- <https://docs.aws.amazon.com/config/latest/developerguide/managed-rules-by-aws-config.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-directory-service'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 9. AWS Directory Service



AWS Directory Service for Microsoft Active Directory, also known as AWS Managed Microsoft Active Directory (AD), enables your directory-aware workloads and AWS resources to use managed Active Directory (AD) in AWS.

- [Mapping File](AWSDirectoryService.yaml) ([YAML](AWSDirectoryService.yaml))
- [Navigator Layer](layers/AWSDirectoryService.json) ([JSON](layers/AWSDirectoryService.json))

### Mapping Comments


This control was not mapped because it is primarily acting as a connector for Microsoft Active Directory with AWS services and does not provide any security functions other than allowing use of other AWS security controls.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
  


### Tags
- [Identity](#tag-identity)
- [Not Mappable](#tag-not-mappable)
  


### References
- <https://docs.aws.amazon.com/directory-service/index.html#lang/en_us>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-firewall-manager'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 10. AWS Firewall Manager



AWS Firewall Manager is a security management service that allows you to configure and manage rules and security groups for AWS WAF, AWS Shield, AWS VPC, AWS Network Firewall, and Amazon Route 53 Resolvers DNS Firewall across multiple AWS accounts and resources.  

- [Mapping File](AWSFirewallManager.yaml) ([YAML](AWSFirewallManager.yaml))
- [Navigator Layer](layers/AWSFirewallManager.json) ([JSON](layers/AWSFirewallManager.json))

### Mapping Comments


This control was not mapped because AWS Firewall Manager is simply a management service for other AWS security services. It does not inherently protect against any ATT&CK (sub-)techniques. All protections against ATT&CK (sub-)techniques are provided by the lower-level services that it manages (e.g., AWS WAF, AWS Network Firewall, etc.).  This is evident by the fact that to use firewall rules or security groups, they must first be configured in the respective lower-level services.   


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
  


### Tags
- [Network](#tag-network)
- [Not Mappable](#tag-not-mappable)
  


### References
- <https://docs.aws.amazon.com/waf/latest/developerguide/fms-chapter.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-identity-and-access-management'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 11. AWS Identity and Access Management



AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.

- [Mapping File](AWSIAM.yaml) ([YAML](AWSIAM.yaml))
- [Navigator Layer](layers/AWSIAM.json) ([JSON](layers/AWSIAM.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1078 - Valid Accounts](https://attack.mitre.org/techniques/T1078/)|Detect|Partial||
|[T1078 - Valid Accounts](https://attack.mitre.org/techniques/T1078/)|Protect|Partial||
|[T1098 - Account Manipulation](https://attack.mitre.org/techniques/T1098/)|Detect|Minimal|This control may generate logs for creation and manipulation of accounts but the relevant security information would be handled by another security control.|
|[T1110 - Brute Force](https://attack.mitre.org/techniques/T1110/)|Protect|Significant||
|[T1528 - Steal Application Access Token](https://attack.mitre.org/techniques/T1528/)|Protect|Minimal|This control may mitigate against application access token theft if the application is configured to retrieve temporary security credentials using an IAM role. This recommendation is a best practice for IAM but must be explicitly implemented by the application developer.|
|[T1550 - Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550/)|Protect|Minimal||
  


### Tags
- [Credentials](#tag-credentials)
- [Identity](#tag-identity)
  


### References
- <https://docs.aws.amazon.com/iam/index.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-iot-device-defender'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 12. AWS IoT Device Defender



AWS IoT Device Defender is a security service that allows users to audit the configuration of their Internet of Things (IoT) devices, monitor connected devices to detect abnormal behavior, and mitigate security risks. It provides the ability to enforce consistent security policies across AWS IoT device fleets and respond when devices are compromised.

- [Mapping File](AWSIOTDeviceDefender.yaml) ([YAML](AWSIOTDeviceDefender.yaml))
- [Navigator Layer](layers/AWSIOTDeviceDefender.json) ([JSON](layers/AWSIOTDeviceDefender.json))

### Mapping Comments


Mappings for AWS IoT Device Defender audit are based on the current set of AWS IoT Device Defender audit checks that can be enabled. AWS IoT Device Defender's predefined mitigation actions are also included for those audit checks that support them. Audit checks can be run as needed (on-demand audits) or scheduled to be run periodically (scheduled audits), so temporal scoring factors are uniformly high for this control, based on the assumption that checks are run (at minimum) on a frequent basis. Audit check and mitigation names are identified in quotes throughout this mapping.
Mappings for AWS IoT Device Defender detect are based on the current set of AWS IoT Device Defender device-side and cloud-side detection metrics. Cloud-side detection alarms are triggered when set thresholds are exceeded, and device-side detection metrics are published on a chosen interval with a minimum value of 5 minutes, so temporal scoring factors are uniformly high for this control, based on the assumption that thresholds are set to sensible values that detect suspicious values quickly and device-side metric publishing is not set to an unreasonably large interval. Detect metric names are identified in quotes throughout this mapping.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1020 - Automated Exfiltration](https://attack.mitre.org/techniques/T1020/)|Protect|Minimal|This control provides partial coverage for this technique's only sub-technique, but without specific coverage for its procedures, resulting in an overall score of Minimal.|
|[T1040 - Network Sniffing](https://attack.mitre.org/techniques/T1040/)|Protect|Partial|The following AWS IoT Device Defender audit checks and corresponding mitigation actions can identify and resolve configuration problems that should be fixed in order to ensure SSL/TLS encryption is enabled and secure to protect network traffic to/from IoT devices: "CA certificate expiring" ("CA_CERTIFICATE_EXPIRING_CHECK" in the CLI and API), "CA certificate key quality" ("CA_CERTIFICATE_KEY_QUALITY_CHECK" in the CLI and API), and "CA certificate revoked but device certificates still active" ("REVOKED_CA_CERTIFICATE_STILL_ACTIVE_CHECK" in the CLI and API) can identify problems with certificate authority (CA) certificates being used for signing and support the "UPDATE_CA_CERTIFICATE" mitigation action which can resolve them. "Device certificate expiring" ("DEVICE_CERTIFICATE_EXPIRING_CHECK" in the CLI and API), "Device certificate key quality" ("DEVICE_CERTIFICATE_KEY_QUALITY_CHECK" in the CLI and API), "Device certificate shared" ("DEVICE_CERTIFICATE_SHARED_CHECK" in the CLI and API), and "Revoked device certificate still active" ("REVOKED_DEVICE_CERTIFICATE_STILL_ACTIVE_CHECK" in the CLI and API) can identify problems with IoT devices' certificates and support the "UPDATE_DEVICE_CERTIFICATE" and "ADD_THINGS_TO_THING_GROUP" mitigation actions which can resolve them.<br/>Coverage factor is partial for these checks and mitigations, since they are specific to IoT device communication and can only mitigate behavior for adversaries who are unable to decrypt the relevant traffic, resulting in an overall score of Partial.|
|[T1041 - Exfiltration Over C2 Channel](https://attack.mitre.org/techniques/T1041/)|Detect|Partial|The following AWS IoT Device Defender device-side detection metrics can detect indicators that an adversary may be exfiltrating collected data from compromised AWS IoT devices using an established command and control channel to/from those devices: "Destination IPs" ("aws:destination-ip-addresses") outside of expected IP address ranges may suggest that a device is communicating with unexpected parties. "Bytes in" ("aws:all-bytes-in"), "Bytes out" ("aws:all-bytes-out"), "Packets in" ("aws:all-packets-in"), and "Packets out" ("aws:all-packets-out") values outside of expected norms may indicate that the device is sending and/or receiving non-standard traffic, which may include exfiltration of stolen data. "Listening TCP ports" ("aws:listening-tcp-ports"), "Listening TCP port count" ("aws:num-listening-tcp-ports"), "Established TCP connections count" ("aws:num-established-tcp-connections"), "Listening UDP ports" ("aws:listening-udp-ports"), and "Listening UDP port count" ("aws:num-listening-udp-ports") values outside of expected norms may indicate that devices are communicating via unexpected ports/protocols, which may include exfiltration of data over command and control channels.<br/>Coverage factor is partial, since these metrics are limited to exfiltration from IoT devices, resulting in an overall score of Partial.|
|[T1046 - Network Service Scanning](https://attack.mitre.org/techniques/T1046/)|Detect|Partial|The following AWS IoT Device Defender device-side detection metrics can detect indicators that an adversary may be leveraging compromised AWS IoT devices to search their networks for other hosts and their running services, possibly to subsequently carry out lateral movement techniques: "Destination IPs" ("aws:destination-ip-addresses") outside of expected IP address ranges may suggest that a device is communicating with unexpected devices. "Bytes in" ("aws:all-bytes-in"), "Bytes out" ("aws:all-bytes-out"), "Packets in" ("aws:all-packets-in"), and "Packets out" ("aws:all-packets-out") values outside of expected norms may indicate that the device is sending and/or receiving non-standard traffic, which may traffic used to discover other hosts/services. "Listening TCP ports" ("aws:listening-tcp-ports"), "Listening TCP port count" ("aws:num-listening-tcp-ports"), "Established TCP connections count" ("aws:num-established-tcp-connections"), "Listening UDP ports" ("aws:listening-udp-ports"), and "Listening UDP port count" ("aws:num-listening-udp-ports") values outside of expected norms may indicate that devices are communicating via unexpected ports/protocols that may suggest scanning is taking place.<br/>Coverage factor is partial, since these metrics are limited to IoT device communication and detection is only based on network traffic, resulting in an overall score of Partial.|
|[T1048 - Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048/)|Detect|Partial|This control provides partial coverage for this technique and all of its sub-techniques, resulting in an overall score of Partial.|
|[T1071 - Application Layer Protocol](https://attack.mitre.org/techniques/T1071/)|Detect|Minimal|The following AWS IoT Device Defender cloud-side detection metrics can detect indicators that an adversary may be leveraging compromised AWS IoT devices and application layer protocols - especially the Message Queuing Telemetry Transport (MQTT) protocol - to communicate for command and control purposes: "Source IP" ("aws:source-ip-address") values outside of expected IP address ranges may suggest that a device has been stolen. "Messages sent" ("aws:num-messages-sent"), "Messages received" ("aws:num-messages-received"), and "Message size" ("aws:message-byte-size") values outside of expected norms may indicate that devices are sending and/or receiving non-standard traffic, which may include command and control traffic.<br/>The following AWS IoT Device Defender device-side detection metrics can detect indicators that an adversary may be leveraging compromised AWS IoT devices and application layer protocols - especially the Message Queuing Telemetry Transport (MQTT) protocol - to communicate for command and control purposes: "Destination IPs" ("aws:destination-ip-addresses") outside of expected IP address ranges may suggest that a device is communicating with unexpected parties. "Bytes in" ("aws:all-bytes-in"), "Bytes out" ("aws:all-bytes-out"), "Packets in" ("aws:all-packets-in"), and "Packets out" ("aws:all-packets-out") values outside of expected norms may indicate that the device is sending and/or receiving non-standard traffic, which may include command and control traffic. "Listening TCP ports" ("aws:listening-tcp-ports"), "Listening TCP port count" ("aws:num-listening-tcp-ports"), "Established TCP connections count" ("aws:num-established-tcp-connections"), "Listening UDP ports" ("aws:listening-udp-ports"), and "Listening UDP port count" ("aws:num-listening-udp-ports") values outside of expected norms may indicate that devices are communicating via unexpected ports/protocols that may suggest application layer command and control traffic.<br/>Coverage factor is minimal, since these metrics are limited to IoT device communication and none of this technique's sub-techniques are addressed, resulting in an overall score of Minimal.|
|[T1078 - Valid Accounts](https://attack.mitre.org/techniques/T1078/)|Detect|Minimal|This control provides partial detection capability for one of this technique's sub-techniques and a few of its procedure examples resulting in an overall Minimal protection score.|
|[T1078 - Valid Accounts](https://attack.mitre.org/techniques/T1078/)|Protect|Minimal|This control provides partial protection for one of this technique's sub-techniques and a few of its procedure examples resulting in an overall Minimal protection score.|
|[T1095 - Non-Application Layer Protocol](https://attack.mitre.org/techniques/T1095/)|Detect|Minimal|The following AWS IoT Device Defender cloud-side detection metrics can detect indicators that an adversary may be leveraging compromised AWS IoT devices and non-application layer protocols - especially TCP and UDP - to communicate for command and control purposes: "Source IP" ("aws:source-ip-address") values outside of expected IP address ranges may suggest that a device has been stolen. "Messages sent" ("aws:num-messages-sent"), "Messages received" ("aws:num-messages-received"), and "Message size" ("aws:message-byte-size") values outside of expected norms may indicate that devices are sending and/or receiving non-standard traffic, which may include command and control traffic.<br/>The following AWS IoT Device Defender device-side detection metrics can detect indicators that an adversary may be leveraging compromised AWS IoT devices and non-application layer protocols - especially TCP and UDP - to communicate for command and control purposes: "Destination IPs" ("aws:destination-ip-addresses") outside of expected IP address ranges may suggest that a device is communicating with unexpected parties. "Bytes in" ("aws:all-bytes-in"), "Bytes out" ("aws:all-bytes-out"), "Packets in" ("aws:all-packets-in"), and "Packets out" ("aws:all-packets-out") values outside of expected norms may indicate that the device is sending and/or receiving non-standard traffic, which may include command and control traffic. "Listening TCP ports" ("aws:listening-tcp-ports"), "Listening TCP port count" ("aws:num-listening-tcp-ports"), "Established TCP connections count" ("aws:num-established-tcp-connections"), "Listening UDP ports" ("aws:listening-udp-ports"), and "Listening UDP port count" ("aws:num-listening-udp-ports") values outside of expected norms may indicate that devices are communicating via TCP and/or UDP on unexpected ports that may suggest command and control traffic.<br/>Coverage factor is minimal, since these metrics are limited to IoT device communication and none of this technique's sub-techniques are addressed, resulting in an overall score of Minimal.|
|[T1496 - Resource Hijacking](https://attack.mitre.org/techniques/T1496/)|Detect|Partial|The following AWS IoT Device Defender device-side detection metrics can detect indicators that an adversary may be leveraging compromised AWS IoT devices' resources to perform resource-intensive operations like mining cryptocurrency or performing denial of service attacks on other environments: "Destination IPs" ("aws:destination-ip-addresses") outside of expected IP address ranges may suggest that a device is communicating with unexpected parties. "Bytes in" ("aws:all-bytes-in"), "Bytes out" ("aws:all-bytes-out"), "Packets in" ("aws:all-packets-in"), and "Packets out" ("aws:all-packets-out") values outside of expected norms may indicate that the device is sending and/or receiving non-standard traffic, which may include traffic related to resource hijacking activities. "Listening TCP ports" ("aws:listening-tcp-ports"), "Listening TCP port count" ("aws:num-listening-tcp-ports"), "Established TCP connections count" ("aws:num-established-tcp-connections"), "Listening UDP ports" ("aws:listening-udp-ports"), and "Listening UDP port count" ("aws:num-listening-udp-ports") values outside of expected norms may indicate that devices are communicating via unexpected ports/protocols which may include traffic related to resource hijacking activities.<br/>Coverage factor is partial, since these metrics are limited to IoT device hijacking, resulting in an overall score of Partial.|
|[T1530 - Data from Cloud Storage Object](https://attack.mitre.org/techniques/T1530/)|Detect|Partial|The following AWS IoT Device Defender cloud-side detection metrics can detect indicators that an adversary may be leveraging compromised AWS IoT devices and the Message Queuing Telemetry Transport (MQTT) protocol for unauthorized data transfer from cloud-side data sources: "Source IP" ("aws:source-ip-address") values outside of expected IP address ranges may suggest that a device has been stolen. "Messages sent" ("aws:num-messages-sent"), "Messages received" ("aws:num-messages-received"), and "Message size" ("aws:message-byte-size") values outside of expected norms may indicate that devices are sending and/or receiving non-standard traffic, which may include data retrieved from cloud storage.<br/>The following AWS IoT Device Defender device-side detection metrics can detect indicators that an adversary may be leveraging compromised AWS IoT devices and the Message Queuing Telemetry Transport (MQTT) protocol for unauthorized data transfer from cloud-side data sources: "Bytes in" ("aws:all-bytes-in"), "Bytes out" ("aws:all-bytes-out"), "Packets in" ("aws:all-packets-in"), and "Packets out" ("aws:all-packets-out") values outside of expected norms may indicate that devices are sending and/or receiving non-standard traffic, which may include data retrieved from cloud storage.<br/>Coverage factor is partial, since these metrics are limited to IoT device-based collection, resulting in an overall score of Partial.|
|[T1552 - Unsecured Credentials](https://attack.mitre.org/techniques/T1552/)|Detect|Minimal|This control provides partial coverage for a minority of this technique's sub-techniques, resulting in an overall score of Minimal.|
|[T1557 - Man-in-the-Middle](https://attack.mitre.org/techniques/T1557/)|Protect|Minimal|The following AWS IoT Device Defender audit checks and corresponding mitigation actions can identify and resolve configuration problems that should be fixed in order to ensure SSL/TLS encryption is enabled and secure to protect network traffic to/from IoT devices: "CA certificate expiring" ("CA_CERTIFICATE_EXPIRING_CHECK" in the CLI and API), "CA certificate key quality" ("CA_CERTIFICATE_KEY_QUALITY_CHECK" in the CLI and API), and "CA certificate revoked but device certificates still active" ("REVOKED_CA_CERTIFICATE_STILL_ACTIVE_CHECK" in the CLI and API) can identify problems with certificate authority (CA) certificates being used for signing and support the "UPDATE_CA_CERTIFICATE" mitigation action which can resolve them. "Device certificate expiring" ("DEVICE_CERTIFICATE_EXPIRING_CHECK" in the CLI and API), "Device certificate key quality" ("DEVICE_CERTIFICATE_KEY_QUALITY_CHECK" in the CLI and API), "Device certificate shared" ("DEVICE_CERTIFICATE_SHARED_CHECK" in the CLI and API), and "Revoked device certificate still active" ("REVOKED_DEVICE_CERTIFICATE_STILL_ACTIVE_CHECK" in the CLI and API) can identify problems with IoT devices' certificates and support the "UPDATE_DEVICE_CERTIFICATE" and "ADD_THINGS_TO_THING_GROUP" mitigation actions which can resolve them.<br/>Coverage factor is partial for these checks and mitigations, since they are specific to IoT device communication and can only mitigate behavior for adversaries who are unable to decrypt the relevant traffic, resulting in an overall score of Partial. This control does not provide specific coverage for this technique's sub-techniques, resulting in an overall score of Minimal.|
|[T1562 - Impair Defenses](https://attack.mitre.org/techniques/T1562/)|Detect|Minimal|This control provides partial coverage for a minority of this technique's sub-techniques, resulting in an overall score of Minimal.|
|[T1562 - Impair Defenses](https://attack.mitre.org/techniques/T1562/)|Respond|Minimal|This control provides partial coverage for a minority of this technique's sub-techniques, resulting in an overall score of Minimal.|
  


### Tags
- [Internet of Things](#tag-internet-of-things)
- [IoT](#tag-iot)
  


### References
- <https://aws.amazon.com/iot-device-defender/>
- <https://docs.aws.amazon.com/iot-device-defender>
- <https://docs.aws.amazon.com/iot/latest/developerguide/dd-mitigation-actions>
- <https://docs.aws.amazon.com/iot/latest/developerguide/dd-detect-security-use-cases>
- <https://docs.aws.amazon.com/iot/latest/developerguide/detect-cloud-side-metrics>
- <https://docs.aws.amazon.com/iot/latest/developerguide/detect-device-side-metrics>
- <https://docs.aws.amazon.com/iot/latest/developerguide/device-defender>
- <https://docs.aws.amazon.com/iot/latest/developerguide/device-defender-audit>
- <https://docs.aws.amazon.com/iot/latest/developerguide/device-defender-detect>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-key-management-service'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 13. AWS Key Management Service



AWS Key Management Service (KMS) allows you to create and manage cryptographic keys and control their usage across a wide range of AWS services and in your applications. It uses hardware security modules that have been validated under FIPS 140-2.

- [Mapping File](AWSKeyManagementService.yaml) ([YAML](AWSKeyManagementService.yaml))
- [Navigator Layer](layers/AWSKeyManagementService.json) ([JSON](layers/AWSKeyManagementService.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1552 - Unsecured Credentials](https://attack.mitre.org/techniques/T1552/)|Protect|Minimal|This control's protection is specific to a minority of this technique's sub-techniques and procedure examples resulting in a Minimal Coverage score and consequently an overall score of Minimal.|
|[T1588 - Obtain Capabilities](https://attack.mitre.org/techniques/T1588/)|Protect|Partial|Provides protection against sub-techniques involved with stealing credentials, certificates, and keys from the organization. As documented, access can be provisioned and monitored.|
  


### Tags
- [Credentials](#tag-credentials)
  


### References
- <https://aws.amazon.com/kms/>
- <https://docs.aws.amazon.com/kms/latest/developerguide/overview.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-network-firewall'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 14. AWS Network Firewall



The AWS Network Firewall provides a stateful network firewall and intrusion detection and prevention system (via Suricata) at the perimeter of virtual private clouds (VPCs). It is able to filter traffic going to and coming from an internet gateway, NAT gateway, VPN, or AWS  Direct Connect.

- [Mapping File](AWSNetworkFirewall.yaml) ([YAML](AWSNetworkFirewall.yaml))
- [Navigator Layer](layers/AWSNetworkFirewall.json) ([JSON](layers/AWSNetworkFirewall.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1008 - Fallback Channels](https://attack.mitre.org/techniques/T1008/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block communication with known fallback channels by filtering based on known bad IP addresses and domains. This mapping is given a score of Partial because it only protects against known fallback channels and not channels yet to be identified.|
|[T1018 - Remote System Discovery](https://attack.mitre.org/techniques/T1018/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block adversaries from discovering endpoints behind the firewall. This mapping is given a score of Partial because it does not protect against discovering endpoints within the network and behind the firewall.|
|[T1021 - Remote Services](https://attack.mitre.org/techniques/T1021/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to only allow remote services from trusted hosts (i.e., only allow remote access traffic from certain hosts). This mapping is given a score of Partial because even though it can restrict remote services traffic from untrusted hosts for most of the sub-techniques (5 of 6), it cannot protect against an adversary using a trusted host that is permitted to use remote services as part of an attack.|
|[T1041 - Exfiltration Over C2 Channel](https://attack.mitre.org/techniques/T1041/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block adversaries from accessing resources from which to exfiltrate data as well as prevent resources from communicating with known-bad IP addresses and domains that might be used to receive exfiltrated data. This mapping is given a score of Partial because the known-bad IP addresses and domains would need to be known in advance.|
|[T1046 - Network Service Scanning](https://attack.mitre.org/techniques/T1046/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to restrict access to the endpoints within the virtual private cloud and protect against network service scanning. This mapping is given a score of Partial because it only protects against network service scanning attacks that originate from outside the firewall and not from within network protected by the firewall.|
|[T1048 - Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block adversaries from accessing resources from which to exfiltrate data as well as prevent resources from communicating with known-bad IP addresses and domains that might be used to receive exfiltrated data. This mapping is given a score of Partial because the known-bad IP addresses and domains would need to be known in advance and AWS Network Firewall wouldn't have deep packet inspection visibility into encrypted non-C2 protocols.|
|[T1071 - Application Layer Protocol](https://attack.mitre.org/techniques/T1071/)|Protect|Significant|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block malicious or unwanted traffic leveraging application layer protocols. Given this supports all sub-techniques, the mapping is given a score of Significant.|
|[T1090 - Proxy](https://attack.mitre.org/techniques/T1090/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block traffic from known bad IP addresses and to known bad domains that serve as proxies for adversaries. This mapping is given a score of partial because it only supports a subset of the sub-techniques (2 of 4) and because it only blocks known bad IP addresses and domains and does not protect against unknown ones.|
|[T1095 - Non-Application Layer Protocol](https://attack.mitre.org/techniques/T1095/)|Protect|Significant|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block malicious or unwanted traffic leveraging non-application layer protocols. Given this, the mapping is given a score of Significant.|
|[T1104 - Multi-Stage Channels](https://attack.mitre.org/techniques/T1104/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block communication with known command and control channels by filtering based on known bad IP addresses and domains. This mapping is given a score of Partial because it only protects against known channels and not channels yet to be identified.|
|[T1133 - External Remote Services](https://attack.mitre.org/techniques/T1133/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to only allow certain remote services to be available. Futhermore, it can enforce restrictions such that remote services are only from trusted hosts (i.e., only allow remote access traffic from certain hosts). This mapping is given a score of Partial because while it can limit which external remote services and hosts can be used to access the network, it cannot protect against the misuse of legitimate external remote services (e.g., it cannot protect against an adversary using a trusted host that is permitted to use remote services as part of an attack).|
|[T1187 - Forced Authentication](https://attack.mitre.org/techniques/T1187/)|Protect|Significant|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block SMB and WebDAV traffic from exiting the network which can protect against adversaries from forcing authentication over SMB and WebDAV. This mapping is given a score of Significant because AWS Network Firewall can block this traffic or restrict where it can go to.|
|[T1205 - Traffic Signaling](https://attack.mitre.org/techniques/T1205/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block traffic to unused ports from reaching hosts on the network which may help protect against traffic signaling from external systems. This mapping is given a score of partial because the AWS Network Firewall does not do anything to protect against traffic signaling among hosts within the network and behind the firewall.|
|[T1219 - Remote Access Software](https://attack.mitre.org/techniques/T1219/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to only allow remote access software from trusted hosts (i.e., only allow remote access traffic from certain hosts). This mapping is given a score of Partial because even though it can restrict remote access software traffic from untrusted hosts, it cannot protect against an adversary using a trusted host that is permitted to use remote access software as part of an attack.|
|[T1498 - Network Denial of Service](https://attack.mitre.org/techniques/T1498/)|Protect|Minimal|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block the sources of smaller-scale network denial of service attacks. While AWS Network Firewall supports both all sub-techniques (2 of 2), this mapping is given a score of Minimal because often times it is necessary to block the traffic at an Internet Service Provider or Content Provider Network level.|
|[T1499 - Endpoint Denial of Service](https://attack.mitre.org/techniques/T1499/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block adversaries from carrying out denial of service attacks by implementing restrictions on which IP addresses and domains can access the resources (e.g., allow lists) as well as which protocol traffic is permitted. That is, the AWS Network Firewall could block the source of the denial of service attack. This mapping is given a score of Partial because it only supports a subset of the sub-techniques (3 of 4) and because the source of the attack would have to be known before rules could be put in place to protect against it.|
|[T1530 - Data from Cloud Storage Object](https://attack.mitre.org/techniques/T1530/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block adversaries from accessing resources such as cloud storage objects by implementing restrictions on which IP addresses and domains can access the resources (e.g., allow lists). However, since cloud storage objects are located outside the virtual private cloud where the AWS Network Firewall protects, the mapping is only given a score of Partial.|
|[T1542 - Pre-OS Boot](https://attack.mitre.org/techniques/T1542/)|Protect|Minimal|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block traffic over known TFTP ports. This mapping is given a score of Minimal because AWS Network Firewall only supports a subset of sub-techniques (1 of 5) and it does not do anything to protect against TFTP booting among hosts within the network and behind the firewall.|
|[T1571 - Non-Standard Port](https://attack.mitre.org/techniques/T1571/)|Protect|Significant|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to restrict which protocols and port numbers are allowed through the firewall and prevent adversaries from using non-standard ports. As a result, this mapping is given a score of Significant.|
|[T1572 - Protocol Tunneling](https://attack.mitre.org/techniques/T1572/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to block traffic from known bad IP addresses and domains which could protect against protocol tunneling by adversaries. This mapping is given a score of partial because it only blocks known bad IP addresses and domains and does not protect against unknown ones.|
|[T1590 - Gather Victim Network Information](https://attack.mitre.org/techniques/T1590/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to restrict access to the endpoints within the virtual private cloud and protect against adversaries gathering information about the network. While this mapping supports most of the sub-techniques (4 of 6), it is only given a score of Partial because it only protects against attempts to gather information via scanning that originate from outside the firewall and it does not protect against phishing.|
|[T1595 - Active Scanning](https://attack.mitre.org/techniques/T1595/)|Protect|Partial|AWS Network Firewall has the ability to pass, drop, or alert on traffic based on the network protocol as well as perform deep packet inspection on the payload. This functionality can be used to restrict access to the endpoints within the virtual private cloud and protect against active scanning. While this mapping supports al sub-techniques (2 of 2), this mapping is given a score of Partial because it only protects against active scanning attacks that originate from outside the firewall and not from within network protected by the firewall.|
  


### Tags
- [Network](#tag-network)
  


### References
- <https://docs.aws.amazon.com/network-firewall/latest/developerguide/what-is-aws-network-firewall.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-organizations'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 15. AWS Organizations



AWS Organizations is an account management service that enables you to consolidate multiple AWS accounts into an organization that you create and centrally manage. AWS Organizations is integrated with other AWS services so you can define central configurations, security mechanisms, and resource sharing across accounts in your organization.

- [Mapping File](AWSOrganizations.yaml) ([YAML](AWSOrganizations.yaml))
- [Navigator Layer](layers/AWSOrganizations.json) ([JSON](layers/AWSOrganizations.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1078 - Valid Accounts](https://attack.mitre.org/techniques/T1078/)|Protect|Partial|This control may protect against malicious use of cloud accounts but may not mitigate exploitation of local, domain, or default accounts present within deployed resources.|
|[T1087 - Account Discovery](https://attack.mitre.org/techniques/T1087/)|Protect|Minimal|This control may protect against cloud account discovery but does not mitigate against other forms of account discovery.|
|[T1538 - Cloud Service Dashboard](https://attack.mitre.org/techniques/T1538/)|Protect|Partial|This control may protect against cloud service dashboard abuse by segmenting accounts into separate organizational units and restricting dashboard access by least privilege.|
|[T1580 - Cloud Infrastructure Discovery](https://attack.mitre.org/techniques/T1580/)|Protect|Partial|This control may protect against cloud infrastructure discovery by segmenting accounts into separate organizational units and restricting infrastructure access by least privilege.|
  


### Tags
- [Identity](#tag-identity)
  


### References
- <https://docs.aws.amazon.com/organizations/latest/userguide/orgs_introduction.html>
- <https://aws.amazon.com/organizations/getting-started/best-practices/>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-rds'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 16. AWS RDS



AWS Relational Database Service (RDS) is a service that simplifies the setup, operation, and scaling of relational databases in AWS. AWS RDS manages backups, software patching, automatic failure detection, and recovery of databases. AWS RDS supports MySQL, MariaDB, PostgreSQL, Oracle, and Microsoft SQL Server instances.

- [Mapping File](AWSRDS.yaml) ([YAML](AWSRDS.yaml))
- [Navigator Layer](layers/AWSRDS.json) ([JSON](layers/AWSRDS.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1040 - Network Sniffing](https://attack.mitre.org/techniques/T1040/)|Protect|Significant|AWS RDS and AWS RDS Proxy support TLS/SSL connections to database instances which protects against network sniffing attacks. As a result, this mapping is given a score of Significant.|
|[T1190 - Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)|Protect|Partial|AWS RDS supports the automatic patching of minor versions of database instances. This can result in security flaws in the database instances being fixed before they can be exploited. This mapping is given a score of Partial because it does not protect against misconfigured database instances which may be susceptible to exploitation.|
|[T1190 - Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)|Respond|Significant|AWS RDS supports the replication and recovery of database instances. In the event that a database instance is compromised, AWS RDS can be used to restore the database instance to a previous point in time. As a result, this mapping is given a score of Significant.|
|[T1210 - Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210/)|Protect|Partial|AWS RDS supports the automatic patching of minor versions of database instances. This can result in security flaws in the database instances being fixed before they can be exploited. This mapping is given a score of Partial because it does not protect against misconfigured database instances which may be susceptible to exploitation.|
|[T1210 - Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210/)|Respond|Significant|AWS RDS supports the replication and recovery of database instances. In the event that a database instance is compromised, AWS RDS can be used to restore the database instance to a previous point in time. As a result, this mapping is given a score of Significant.|
|[T1485 - Data Destruction](https://attack.mitre.org/techniques/T1485/)|Detect|Partial|AWS RDS generates events for database instances and includes the following events that may indicate that an adversary has destroyed the database instance.<br/>RDS-EVENT-0003: The DB instance has been deleted RDS-EVENT-0041: A DB snapshot has been deleted<br/>This mapping is given a score of Partial because it can't differentiate between an authorized and unauthorized deletion.<br/>|
|[T1485 - Data Destruction](https://attack.mitre.org/techniques/T1485/)|Protect|Significant|AWS RDS provides deletion protection which prevents any user from deleting a database instance. If applied, the setting may mitigate attempts to delete a database instance. As a result, this mapping is given a score of Significant.|
|[T1485 - Data Destruction](https://attack.mitre.org/techniques/T1485/)|Respond|Significant|AWS RDS supports the replication and recovery of database instances. In the event that a database instance is deleted, AWS RDS can be used to restore the database instance to a previous point in time. As a result, this mapping is given a score of Significant.|
|[T1486 - Data Encrypted for Impact](https://attack.mitre.org/techniques/T1486/)|Respond|Significant|AWS RDS supports the replication and recovery of database instances. In the event that a database instance is encrypted by an adversary (e.g., ransomware), AWS RDS can be used to restore the database instance to a previous point in time. As a result, this mapping is given a score of Significant.|
|[T1489 - Service Stop](https://attack.mitre.org/techniques/T1489/)|Detect|Partial|AWS RDS generates events for database instances and includes the following event that may indicate that an adversary has attempted to stop a database instance.<br/>RDS-EVENT-0087: The DB instance has been stopped<br/>This mapping is given a score of Partial because it can't differentiate between an authorized and unauthorized stopping of the database instance.<br/>|
|[T1490 - Inhibit System Recovery](https://attack.mitre.org/techniques/T1490/)|Detect|Partial|AWS RDS generates events for database instances and includes the following event that may indicate that an adversary has attempted to inhibit system recovery.<br/>RDS-EVENT-0028: Automatic backups for this DB instance have been disabled<br/>This mapping is given a score of Partial because it can't differentiate between an authorized and unauthorized disabling of automatic backups.<br/>|
|[T1490 - Inhibit System Recovery](https://attack.mitre.org/techniques/T1490/)|Respond|Significant|AWS RDS supports the replication and recovery of database instances. In the event that a database instance is compromised and modified to disrupt recovery, AWS RDS can be used to restore the database instance to a previous point in time. As a result, this mapping is given a score of Significant.|
|[T1529 - System Shutdown/Reboot](https://attack.mitre.org/techniques/T1529/)|Detect|Partial|AWS RDS generates events for database instances and includes the following events that may indicate that an adversary has shutdown or rebooted the database instance. <br/>RDS-EVENT-0006: The DB instance restarted, RDS-EVENT-0004: The DB instance shutdown, RDS-EVENT-0022: An error has occurred while restarting MySQL or MariaDB<br/>This mapping is given a score of Partial because it can't differentiate between an authorized and unauthorized shutdown/reboot.|
|[T1530 - Data from Cloud Storage Object](https://attack.mitre.org/techniques/T1530/)|Protect|Significant|AWS RDS supports the encryption of the underlying storage for database instances, backups, read replicas, and snapshots using the AES-256 encryption algorithm. This can protect against an adversary from gaining access to a database instance in the event they get access to the underlying system where the database instance is hosted or to S3 where the backups are stored. Furthermore, with AWS RDS, there is a setting that specifies whether or not a database instances is publicly accessible. When public accessibility is turned off, the database instance will not be available outside the VPC in which it was created. As a result, this mapping is given a score of Significant.|
|[T1557 - Man-in-the-Middle](https://attack.mitre.org/techniques/T1557/)|Protect|Significant|AWS RDS and AWS RDS Proxy support TLS/SSL connections to database instances which protects against man-in-the-middle attacks. However, given that it does not support any sub-techniques, the mapping is given a score of Partial.|
|[T1561 - Disk Wipe](https://attack.mitre.org/techniques/T1561/)|Respond|Minimal|AWS RDS supports the replication and recovery of database instances. In the event that a database instance is deleted during a disk wipe, AWS RDS can be used to restore the database instance to a previous point in time. However, this mapping is only given a score of Minimal because AWS RDS only provides a backup of the database instance and not the underlying system that it is hosted on.|
|[T1565 - Data Manipulation](https://attack.mitre.org/techniques/T1565/)|Protect|Partial|AWS RDS supports the encryption of database instances using the AES-256 encryption algorithm. This can protect database instances from being modified at rest. Furthermore, AWS RDS supports TLS/SSL connections which protect data from being modified during transit. This mapping is given a score of Partial because it only supports a subset of the sub-techniques (2 of 3).|
|[T1565 - Data Manipulation](https://attack.mitre.org/techniques/T1565/)|Respond|Significant|AWS RDS supports the replication and recovery of database instances. In the event that data is manipulated, AWS RDS can be used to restore the database instance to a previous point in time. As a result, this mapping is given a score of Significant.|
  


### Tags
- [Database](#tag-database)
  


### References
- <https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-resource-access-manager'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 17. AWS Resource Access Manager



AWS RAM lets you share your resources with an organization or organizational units (OUs) in AWS Organizations, and AWS accounts. For supported resource types, you can also share resources with IAM roles and IAM users.

- [Mapping File](AWSResourceAccessManager.yaml) ([YAML](AWSResourceAccessManager.yaml))
- [Navigator Layer](layers/AWSResourceAccessManager.json) ([JSON](layers/AWSResourceAccessManager.json))

### Mapping Comments


This control is not mappable because it does not provide any security capabilities other than allowing for use of security features contained within AWS Organizations and AWS Identity and Access Management.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
  


### Tags
- [Not Mappable](#tag-not-mappable)
  


### References
- <https://docs.aws.amazon.com/ram/latest/userguide/what-is.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-s3'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 18. AWS S3



Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.  Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web.

- [Mapping File](AWSS3.yaml) ([YAML](AWSS3.yaml))
- [Navigator Layer](layers/AWSS3.json) ([JSON](layers/AWSS3.json))

### Mapping Comments


The S3 server access logging feature was not mapped because it was deemed to be a data source that can be used with other detective controls rather than a security control in of itself.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1485 - Data Destruction](https://attack.mitre.org/techniques/T1485/)|Protect|Significant|AWS S3 may protect against data destruction through application of several best practices. Multi-factor authentication can be enabled for delete operations and for changing the versioning state of a bucket. Versioning can be enabled to revert objects to a previous state after malicious destruction or corruption. S3 Object Lock can help prevent objects from being deleted or overwritten for a fixed amount of time or indefinitely.  In addition, S3 Cross Region Replication can be used to replicate S3 buckets to another AWS region for add protection.|
|[T1530 - Data from Cloud Storage Object](https://attack.mitre.org/techniques/T1530/)|Protect|Significant|S3 provides full control of access via Identity and Access Management (IAM) policies and with its access control lists (ACLs). The S3 Block Public Access feature allows for policies limiting public access to Amazon S3 resources that are enforced regardless of how the resources are created or associated IAM policies. Server-side encryption can be enabled for data at rest and allows for use of S3-managed keys, AWS Key Management Service managed keys, or customer-provided keys.|
  


### Tags
- [Storage](#tag-storage)
  


### References
- <https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-secrets-manager'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 19. AWS Secrets Manager



AWS Secrets Manager helps you protect secrets needed to access your applications, services, and IT resources. The service enables you to easily rotate, manage, and retrieve database credentials, API keys, and other secrets throughout their lifecycle.

- [Mapping File](AWSSecretsManager.yaml) ([YAML](AWSSecretsManager.yaml))
- [Navigator Layer](layers/AWSSecretsManager.json) ([JSON](layers/AWSSecretsManager.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1212 - Exploitation for Credential Access](https://attack.mitre.org/techniques/T1212/)|Protect|Partial|This control may protect against exploitation for credential access by removing credentials and secrets from applications that can be exploited and requiring authenticated API calls to retrieve those credentials and secrets.|
|[T1528 - Steal Application Access Token](https://attack.mitre.org/techniques/T1528/)|Protect|Partial|This control may prevent theft of application access tokens by replacing those tokens with authenticated and encrypted API calls to AWS Secrets Manager. This control is relevant for credentials stored in applications or configuration files but not credentials entered directly by a user.|
|[T1552 - Unsecured Credentials](https://attack.mitre.org/techniques/T1552/)|Protect|Partial|This control is relevant for credentials stored in applications or configuration files but not credentials entered directly by a user.|
|[T1555 - Credentials from Password Stores](https://attack.mitre.org/techniques/T1555/)|Protect|Partial|This control may prevent harvesting of credentials from password stores by providing a secure, finely controlled location for secrets storage. This control is only relevant for credentials that would be used from application and configuration files and not those entered directly by an end user.|
  


### Tags
- [Credentials](#tag-credentials)
  


### References
- <https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html>
- <https://docs.aws.amazon.com/secretsmanager/latest/userguide/best-practices.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-security-hub'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 20. AWS Security Hub



AWS Security Hub is a tool that supports the aggregation, organization, and prioritization of security alerts and findings from multiple services including Amazon GuardDuty, Amazon Inspector, Amazon Macie, AWS Identity and Access Management (IAM) Access Analyzer, AWS Systems Manager, AWS Firewall Manager, and AWS Partner Network (APN) solutions. To do this, AWS Security Hub relies on managed insights which are collections of findings that identify security areas that need to be addressed as well as custom checks for different detections. While AWS Security Hub supports  custom insights and numerous AWS Config checks, this mapping focuses only on the managed insights  and the custom Security Hub checks provided by Amazon. Custom managed insights and AWS Config checks are considered out of scope for this mapping as the custom managed insights will vary from organization  to organization and AWS Config has its own mapping. 


- [Mapping File](AWSSecurityHub.yaml) ([YAML](AWSSecurityHub.yaml))
- [Navigator Layer](layers/AWSSecurityHub.json) ([JSON](layers/AWSSecurityHub.json))

### Mapping Comments


Managed Insights: AWS Security Hub reports on collections of related findings which are known as managed insights. When possible, these managed insights are mapped to ATT&CK techniques (e.g., "S3 buckets with public write or read permissions"). It should be noted that not all managed insights have the level of detail to be able to map them to ATT&CK techniques and are not included in the mapping (e.g., "EC2 instances involved in known Tactics, Techniques, and Procedures (TTPs)"). 
AWS Config: AWS Security Hub supports reporting on findings from AWS Config (e.g., for CIS AWS Foundations Benchmark controls among others). Given that AWS Config is its own service, these findings will not be mapped to ATT&CK. The only controls that will be included in this mapping  are those for which Security Hub implements custom logic. It should also be noted that there will  be a future CTID project that maps specific CIS Benchmarks to ATT&CK techniques. 
  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1068 - Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068/)|Detect|Partial|AWS Security Hub reports on EC2 instances that are missing security patches for vulnerabilities which could enable an adversary to exploit vulnerabilities through the attack lifecycle. AWS Security Hub provides this detection with the following managed insight.<br/>EC2 instances that have missing security patches for important vulnerabilities<br/>This is scored as Partial because the checks associated with Security Hub would only report on missing patches for known vulnerabilities. It doesn't not cover zero-day vulnerabilities.|
|[T1078 - Valid Accounts](https://attack.mitre.org/techniques/T1078/)|Detect|Minimal|AWS Security Hub detects suspicious activity by AWS accounts which could indicate valid accounts being leveraged by an adversary. AWS Security Hub provides these detections with the following managed insights.<br/>AWS principals with suspicious access key activity Credentials that may have leaked AWS resources with unauthorized access attempts IAM users with suspicious activity<br/>AWS Security Hub also performs checks from the AWS Foundations CIS Benchmark and PCI-DSS security  standard that, if implemented, would help towards detecting the misuse of valid accounts. AWS  Security Hub provides these detections with the following checks.<br/>3.1 Ensure a log metric filter and alarm exist for unauthorized API calls 3.2 Ensure a log metric filter and alarm exist for Management Console sign-in without MFA 3.3 Ensure a log metric filter and alarm exist for usage of "root" account  3.4 Ensure a log metric filter and alarm exist for IAM policy changes 3.6 Ensure a log metric filter and alarm exist for AWS Management Console authentication failures [PCI.CW.1] A log metric filter and alarm should exist for usage of the "root" user<br/>By monitoring the root account, activity where accounts make unauthorized API calls, and changes to IAM permissions among other things, it may be possible to detect valid accounts that  are being misused and are potentially compromised.<br/>This is scored as Minimal because it only supports a subset of the sub-techniques (1 of 4).|
|[T1098 - Account Manipulation](https://attack.mitre.org/techniques/T1098/)|Detect|Minimal|AWS Security Hub performs a check from the AWS Foundations CIS Benchmark that, if implemented, would help towards detecting the manipulation of accounts. AWS Security Hub provides this detection with the following check.<br/>3.4 Ensure a log metric filter and alarm exist for IAM policy changes <br/>This is scored as Minimal because it only supports a subset of the sub-techniques (1 of 4).|
|[T1110 - Brute Force](https://attack.mitre.org/techniques/T1110/)|Detect|Minimal|AWS Security Hub performs a check from the AWS Foundations CIS Benchmark that, if implemented, would help towards detecting the brute forcing of accounts. AWS Security Hub provides this detection with the following checks.<br/>3.6 Ensure a log metric filter and alarm exist for AWS Management Console authentication failures<br/>This is scored as Minimal because it only applies to the AWS Management Console and not other access mechanisms (e.g., CLI, SDK, etc.) and it only supports a subset of the sub-techniques (3 of 4). Furthermore, it does not detect brute-forcing methods for other components such as EC2 instances.|
|[T1190 - Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)|Detect|Partial|AWS Security Hub reports on EC2 instances that are missing security patches for vulnerabilities which could enable an adversary to exploit vulnerabilities through the attack lifecycle. AWS Security Hub provides this detection with the following managed insight.<br/>EC2 instances that have missing security patches for important vulnerabilities<br/>This is scored as Partial because the checks associated with Security Hub would only report on missing patches for known vulnerabilities. It doesn't not cover zero-day vulnerabilities.|
|[T1203 - Exploitation for Client Execution](https://attack.mitre.org/techniques/T1203/)|Detect|Partial|AWS Security Hub reports on EC2 instances that are missing security patches for vulnerabilities which could enable an adversary to exploit vulnerabilities through the attack lifecycle. AWS Security Hub provides this detection with the following managed insight.<br/>EC2 instances that have missing security patches for important vulnerabilities<br/>This is scored as Partial because the checks associated with Security Hub would only report on missing patches for known vulnerabilities. It doesn't not cover zero-day vulnerabilities.|
|[T1210 - Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210/)|Detect|Partial|AWS Security Hub reports on EC2 instances that are missing security patches for vulnerabilities which could enable an adversary to exploit vulnerabilities through the attack lifecycle. AWS Security Hub provides this detection with the following managed insight.<br/>EC2 instances that have missing security patches for important vulnerabilities<br/>This is scored as Partial because the checks associated with Security Hub would only report on missing patches for known vulnerabilities. It doesn't not cover zero-day vulnerabilities.|
|[T1211 - Exploitation for Defense Evasion](https://attack.mitre.org/techniques/T1211/)|Detect|Partial|AWS Security Hub reports on EC2 instances that are missing security patches for vulnerabilities which could enable an adversary to exploit vulnerabilities through the attack lifecycle. AWS Security Hub provides this detection with the following managed insight.<br/>EC2 instances that have missing security patches for important vulnerabilities<br/>This is scored as Partial because the checks associated with Security Hub would only report on missing patches for known vulnerabilities. It doesn't not cover zero-day vulnerabilities.|
|[T1212 - Exploitation for Credential Access](https://attack.mitre.org/techniques/T1212/)|Detect|Partial|AWS Security Hub reports on EC2 instances that are missing security patches for vulnerabilities which could enable an adversary to exploit vulnerabilities through the attack lifecycle. AWS Security Hub provides this detection with the following managed insight.<br/>EC2 instances that have missing security patches for important vulnerabilities<br/>This is scored as Partial because the checks associated with Security Hub would only report on missing patches for known vulnerabilities. It doesn't not cover zero-day vulnerabilities.|
|[T1485 - Data Destruction](https://attack.mitre.org/techniques/T1485/)|Detect|Minimal|AWS Security Hub performs a check from the AWS Foundations CIS Benchmark that, if implemented, would help towards detecting the scheduled destruction of Customer Master Keys (CMKs) which are critical for being able to decrypt data. AWS Security Hub provides this detection with the following check.<br/>Ensure a log metric filter and alarm exist for disabling or scheduled deletion of customer created CMKs<br/>This is scored as Minimal because CMKs only represent one type of data that could be destroyed by an adversary.|
|[T1530 - Data from Cloud Storage Object](https://attack.mitre.org/techniques/T1530/)|Detect|Partial|AWS Security Hub detects improperly secured data from S3 buckets such as public read and write access that may result in an adversary getting access to data in cloud storage. AWS Security Hub provides this detection with the following managed insight.<br/>S3 buckets with public write or read permissions<br/>AWS Security Hub also performs checks from the AWS Foundations CIS Benchmark that, if implemented, would help towards detecting improperly secured S3 buckets which could result in them being discovered. AWS Security Hub provides this detection with the following check.<br/>3.8 Ensure a log metric filter and alarm exist for S3 bucket policy changes <br/>This is scored as Partial because it only detects when S3 buckets have public read or write access  and doesn't detect improperly secured data in other storage types (e.g., DBs, NFS, etc.).|
|[T1531 - Account Access Removal](https://attack.mitre.org/techniques/T1531/)|Detect|Partial|AWS Security Hub performs a check from the AWS Foundations CIS Benchmark that, if implemented, would help towards detecting the modification of accounts. AWS Security Hub provides this detection with the following check.<br/>3.4 Ensure a log metric filter and alarm exist for IAM policy changes <br/>This is scored as Partial because it only supports the monitoring of changes to AWS IAM accounts and not the accounts on instances of operating systems.|
|[T1562 - Impair Defenses](https://attack.mitre.org/techniques/T1562/)|Detect|Partial|AWS Security Hub performs checks from the AWS Foundations CIS Benchmark that, if implemented, would help towards detecting changes to key AWS services. AWS Security Hub provides these detections with the following checks.<br/>3.5 Ensure a log metric filter and alarm exist for CloudTrail configuration changes 3.9 Ensure a log metric filter and alarm exist for AWS Config configuration changes 3.10 Ensure a log metric filter and alarm exist for security group changes 3.11 Ensure a log metric filter and alarm exist for changes to Network Access Control Lists (NACL)  3.12 Ensure a log metric filter and alarm exist for changes to network gateways  3.13 Ensure a log metric filter and alarm exist for route table changes 3.14 Ensure a log metric filter and alarm exist for VPC changes<br/>This is scored as Partial because it only supports a subset of the sub-techniques (3 of 8).|
|[T1580 - Cloud Infrastructure Discovery](https://attack.mitre.org/techniques/T1580/)|Detect|Partial|AWS Security Hub detects improperly secured data from S3 buckets such as public read and write access as well as accessible EC2 instances that may result in an adversary learning  about cloud infrastructure used by the organization. AWS Security Hub provides these detections  with the following managed insights.<br/>S3 buckets with public write or read permissions EC2 instances that have ports accessible from the Internet EC2 instances that are open to the Internet<br/>AWS Security Hub also performs checks from the AWS Foundations CIS Benchmark that, if implemented, would help towards detecting improperly secured S3 buckets which could result in them being discovered. AWS Security Hub provides this detection with the following check.<br/>3.8 Ensure a log metric filter and alarm exist for S3 bucket policy changes <br/>This is scored as Partial because S3 and EC2 only represent a subset of available cloud infrastructure components.|
|[T1589 - Gather Victim Identity Information](https://attack.mitre.org/techniques/T1589/)|Detect|Minimal|AWS Security Hub detects improperly secured data from S3 buckets such as public read and write access that may result in an adversary getting access to information that could be used during targeting. AWS Security Hub provides these detections with the following managed insights.<br/>S3 buckets with public write or read permissions S3 buckets with sensitive data<br/>This is scored as Minimal because S3 only represents one of many available sources of information that an adversary could use for targeting.|
|[T1590 - Gather Victim Network Information](https://attack.mitre.org/techniques/T1590/)|Detect|Minimal|AWS Security Hub detects improperly secured data from S3 buckets such as public read and write access that may result in an adversary getting access to information that could be used during targeting. AWS Security Hub provides these detections with the following managed insights.<br/>S3 buckets with public write or read permissions S3 buckets with sensitive data<br/>This is scored as Minimal because S3 only represents one of many available sources of information that an adversary could use for targeting.|
|[T1591 - Gather Victim Org Information](https://attack.mitre.org/techniques/T1591/)|Detect|Minimal|AWS Security Hub detects improperly secured data from S3 buckets such as public read and write access that may result in an adversary getting access to information that could be used during targeting. AWS Security Hub provides these detections with the following managed insights.<br/>S3 buckets with public write or read permissions S3 buckets with sensitive data<br/>This is scored as Minimal because S3 only represents one of many available sources of information that an adversary could use for targeting.|
|[T1592 - Gather Victim Host Information](https://attack.mitre.org/techniques/T1592/)|Detect|Minimal|AWS Security Hub detects improperly secured data from S3 buckets such as public read and write access that may result in an adversary getting access to information that could be used during targeting. AWS Security Hub provides these detections with the following managed insights.<br/>S3 buckets with public write or read permissions S3 buckets with sensitive data<br/>This is scored as Minimal because S3 only represents one of many available sources of information that an adversary could use for targeting.|
  


### References
- <https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-shield'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 21. AWS Shield



AWS Shield is a service that protects against Distributed Denial of Service attacks. There are two tiers for this service Standard and Advanced.
AWS Shield Standard defends against most common, frequently occurring network and transport (Layer 3 and 4 attacks) layer DDoS attacks that target your web site or applications.
AWS Shield Advanced adds on to standard by providing additional detection and mitigation against large and sophisticated DDoS attacks. There is near real-time visibility into attacks. AWS Shield Advanced also comes with 24x7 access to the AWS DDoS Response Team (DRT).

- [Mapping File](AWSShield.yaml) ([YAML](AWSShield.yaml))
- [Navigator Layer](layers/AWSShield.json) ([JSON](layers/AWSShield.json))

### Mapping Comments


There is not much documentation that lends itself useful to scoring the accuracy of this control although offerings such as Shield Advanced protection groups and the AWS Shield Response Team (SRT) can be leveraged to improve the accuracy of this control. The control states that DDOS attacks can be mitigated in real time (temporal factor) and not increase cause latency for impacted services.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1498 - Network Denial of Service](https://attack.mitre.org/techniques/T1498/)|Respond|Significant||
|[T1499 - Endpoint Denial of Service](https://attack.mitre.org/techniques/T1499/)|Respond|Significant||
  


### Tags
- [Denial of Service](#tag-denial-of-service)
- [Network](#tag-network)
  


### References
- <https://aws.amazon.com/shield/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc>
- <https://aws.amazon.com/shield/features/>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-single-sign-on'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 22. AWS Single Sign-On



AWS Single Sign-On is a cloud-based single sign-on (SSO) service that makes it easy to centrally manage SSO access to all your AWS accounts and cloud applications. Specifically, it helps you manage SSO access and user permissions across all your AWS accounts in AWS Organizations. AWS SSO also helps you manage access and permissions to commonly used third-party software as a service (SaaS) applications, AWS SSO-integrated applications as well as custom applications that support Security Assertion Markup Language (SAML) 2.0.

- [Mapping File](AWSSSO.yaml) ([YAML](AWSSSO.yaml))
- [Navigator Layer](layers/AWSSSO.json) ([JSON](layers/AWSSSO.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1078 - Valid Accounts](https://attack.mitre.org/techniques/T1078/)|Protect|Partial||
|[T1110 - Brute Force](https://attack.mitre.org/techniques/T1110/)|Protect|Partial|This control may not provide any mitigation against password cracking.|
|[T1133 - External Remote Services](https://attack.mitre.org/techniques/T1133/)|Protect|Significant|This control may protect against abuse of external remote services by requiring multi-factor authentication for single sign-on accounts.|
  


### Tags
- [Credentials](#tag-credentials)
- [Identity](#tag-identity)
  


### References
- <https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='aws-web-application-firewall'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 23. AWS Web Application Firewall



The AWS Web Application Firewall (WAF) protects web applications and Application Programmer Interfaces (APIs) from exploits and bots that may impact the availability and security of resources by filtering out unwanted or malicious web traffic based on a set of rules. AWS WAF can be configured to control how Amazon CloudFront, Amazon API Gateway REST API, Application Load Balancer, and AWS AppSync GraphQL API respond to web requests. This mapping focuses on the AWS Managed Rules rule groups currently available. It does not cover paid solutions from Amazon or managed rules from Amazon Marketplace. 

- [Mapping File](AWSWebApplicationFirewall.yaml) ([YAML](AWSWebApplicationFirewall.yaml))
- [Navigator Layer](layers/AWSWebApplicationFirewall.json) ([JSON](layers/AWSWebApplicationFirewall.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1046 - Network Service Scanning](https://attack.mitre.org/techniques/T1046/)|Protect|Partial|AWS WAF protects against bots that run scans against web applications such as Nessus (vulnerability assessments) and Nmap (IP address and port scans) among others. AWS WAF does this by blocking malicious traffic that indicate bad bots such as those listed above (e.g., via User-Agent values). AWS WAF uses the following rule sets to provide this protection.<br/>AWSManagedRulesCommonRuleSet  AWSManagedRulesBotControlRuleSet<br/>This is scored as Partial because the rule sets, while they block malicious traffic  in near real-time, only protect web applications against scans performed by bots.|
|[T1059 - Command and Scripting Interpreter](https://attack.mitre.org/techniques/T1059/)|Protect|Partial|The AWS WAF protects web applications from injection attacks that leverage command and scripting interpreters. AWS WAF provides this protection via the following rule sets that block malicious traffic across a variety of operating systems and applications.<br/>AWSManagedRulesCommonRuleSet AWSManagedRulesSQLiRuleSet  AWSManagedRulesUnixRuleSet  AWSManagedRulesWindowsRuleSet AWSManagedRulesPHPRuleSet  AWSManagedRulesWordPressRuleSet<br/>This is given a score of Partial (instead of Minimal) because while it only protects against a subset of sub-techniques (3 out of 8), it does provide protections for command and scripting interpreters that do not have sub-techniques (SQL, PHP, etc.). Furthermore, it blocks the malicious content in near real-time.|
|[T1071 - Application Layer Protocol](https://attack.mitre.org/techniques/T1071/)|Protect|Minimal|AWS WAF protects against this by inspecting incoming requests and blocking malicious traffic. AWS WAF uses the following rule sets to provide this protection.<br/>AWSManagedRulesCommonRuleSet  AWSManagedRulesAdminProtectionRuleSet AWSManagedRulesKnownBadInputsRuleSet  AWSManagedRulesSQLiRuleSet AWSManagedRulesLinuxRuleSet  AWSManagedRulesUnixRuleSet  AWSManagedRulesWindowsRuleSet AWSManagedRulesPHPRuleSet  AWSManagedRulesWordPressRuleSet  AWSManagedRulesBotControlRuleSet<br/>This is scored as Minimal because the rule sets only protect against a subset of the sub-techniques (1 of 4).|
|[T1090 - Proxy](https://attack.mitre.org/techniques/T1090/)|Protect|Partial|The AWS WAF protects web applications from access by adversaries that leverage tools that obscure their identity (e.g., VPN, proxies, Tor, hosting providers). AWS WAF provides this protection via the following rule set that blocks incoming traffic from IP addresses known to anonymize connection information or be less likely to source end user traffic.<br/>AWSManagedRulesAnonymousIpList<br/>This is given a score of Partial because it provides protections for only a subset of the sub-techniques (2 out of 4) and is based only on known IP addresses. Furthermore, it blocks the malicious content in near real-time.|
|[T1189 - Drive-by Compromise](https://attack.mitre.org/techniques/T1189/)|Protect|Significant|AWS WAF protects against drive-by compromises by blocking malicious traffic that contains cross-site scripting patterns with the following rule set.<br/>AWSManagedRulesCommonRuleSet<br/>This is scored as Significant because the rule set is broadly applicable to web applications and blocks the malicious traffic in near real-time.|
|[T1190 - Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)|Protect|Significant|The AWS WAF protects public-facing applications against a range of vulnerabilities including those listed in the OWASP Top 10. AWS WAF provides this protection via the following rule sets that block malicious traffic across a variety of operating systems and applications.<br/>AWSManagedRulesCommonRuleSet  AWSManagedRulesKnownBadInputRuleSet AWSManagedRulesSQLiRuleSet  AWSManagedRulesLinuxRuleSet  AWSManagedRulesUnixRuleSet AWSManagedRulesWindowsRuleSet  AWSManagedRulesPHPRuleSet  AWSManagedRulesWordPressRuleSet<br/>This is given a score of Significant because it protects against vulnerabilities across multiple operating systems (Windows, Linux, POSIX) and technologies (JavaScript, SQL, PHP, WordPress). Furthermore, it blocks the malicious content in near real-time.|
|[T1203 - Exploitation for Client Execution](https://attack.mitre.org/techniques/T1203/)|Protect|Significant|AWS WAF protects against exploitation for client execution (browser-based exploitation) by blocking malicious traffic that contains cross-site scripting patterns with the following rule set.<br/>AWSManagedRulesCommonRuleSet<br/>This is scored as Significant because the rule set is broadly applicable to web applications and blocks the malicious traffic in near real-time.|
|[T1595 - Active Scanning](https://attack.mitre.org/techniques/T1595/)|Protect|Partial|AWS WAF protects against bots that run scans against web applications such as Nessus (vulnerability assessments) and Nmap (IP address and port scans) among others. AWS WAF does this by blocking malicious traffic that indicates bad bots such as those listed above (e.g., via User-Agent values). AWS WAF uses the following rule sets to provide this protection.<br/>AWSManagedRulesCommonRuleSet  AWSManagedRulesBotControlRuleSet<br/>This is scored as Partial because the rule sets, while they block malicious traffic in near real-time, only protect web applications against scans performed by bots.|
  


### Tags
- [Network](#tag-network)
  


### References
- <https://aws.amazon.com/waf/>
- <https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html>
- <https://docs.aws.amazon.com/waf/latest/APIReference/Welcome.html>
- <https://docs.aws.amazon.com/waf/latest/developerguide/aws-managed-rule-groups-list.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='amazon-cognito'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 24. Amazon Cognito



Amazon Cognito is a service that provides user management for web and mobile apps. The service establishes authentication and authorization for its registered users. 

- [Mapping File](AmazonCognito.yaml) ([YAML](AmazonCognito.yaml))
- [Navigator Layer](layers/AmazonCognito.json) ([JSON](layers/AmazonCognito.json))

### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1078 - Valid Accounts](https://attack.mitre.org/techniques/T1078/)|Protect|Minimal|This control provides partial protection for one of this technique's sub-techniques and a few of its procedure examples resulting in an overall Minimal protection score.|
|[T1110 - Brute Force](https://attack.mitre.org/techniques/T1110/)|Protect|Significant|Amazon Cognito's MFA capability provides significant protection against password compromises, requiring the adversary to complete an additional authentication method before their access is permitted.|
  


### Tags
- [Identity](#tag-identity)
  


### References
- <https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html>
- <https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pool-settings-compromised-credentials.html>
- <https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pool-settings-adaptive-authentication.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='amazon-detective'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 25. Amazon Detective



Amazon Detective is an automated data enrichment tool that extracts time-based events from other services such as AWS CloudTrail, Amazon VPC flow logs, and GuardDuty.
These events include: login attempts,  API calls,  and network traffic and can be very useful in understanding security issues or operational account activity. Amazon Detective uses machine learning, statistical analysis, and graph theory to help you visualize and conduct faster and more efficient security investigations.

- [Mapping File](AmazonDetective.yaml) ([YAML](AmazonDetective.yaml))
- [Navigator Layer](layers/AmazonDetective.json) ([JSON](layers/AmazonDetective.json))

### Mapping Comments


Although this service can be scored as a Response control (Minimal/Data Enrichment/Forensics), due to the generic nature of its functionality, currently it does not look to be reasonably mappable to specific (sub-)techniques of MITRE ATT&CK.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
  


### Tags
- [Not Mappable](#tag-not-mappable)
  


### References
- <https://aws.amazon.com/detective/>
- <https://aws.amazon.com/detective/faqs/>
- <https://docs.aws.amazon.com/detective/latest/adminguide/what-is-detective.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='amazon-guardduty'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 26. Amazon GuardDuty



Amazon GuardDuty is a threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts, workloads, and data stored in Amazon S3. The service uses machine learning, anomaly detection, and integrated threat intelligence to identify and prioritize potential threats. GuardDuty analyzes tens of billions of events across multiple AWS data sources, such as AWS CloudTrail event logs, Amazon VPC Flow Logs, and DNS logs.

- [Mapping File](AmazonGuardDuty.yaml) ([YAML](AmazonGuardDuty.yaml))
- [Navigator Layer](layers/AmazonGuardDuty.json) ([JSON](layers/AmazonGuardDuty.json))

### Mapping Comments


Scores for this service are capped at Partial due to limited coverage and accuracy information.
The temporal factor for this control is consistent: the first instance of a finding taking place is alerted within 5 minutes of the event occurring. After that any subsequent events can be customized to be reported at 15 minutes, 1 hour, or the default of 6 hours.
The following findings were not mappable:
  Backdoor:EC2/Spambot
  Impact:EC2/AbusedDomainRequest.Reputation
  InitialAccess:IAMUser/AnomalousBehavior  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1020 - Automated Exfiltration](https://attack.mitre.org/techniques/T1020/)|Detect|Partial|The following GuardDuty finding type flags events that may indicate adversaries attempting to exfiltrate data, such as sensitive documents, through the use of automated processing after being gathered during Collection.<br/>Behavior:EC2/TrafficVolumeUnusual Exfiltration:S3/MaliciousIPCaller Exfiltration:S3/ObjectRead.Unusual PenTest:S3/KaliLinux PenTest:S3/ParrotLinux PenTest:S3/PentooLinux UnauthorizedAccess:S3/MaliciousIPCaller.Custom UnauthorizedAccess:S3/TorIPCaller|
|[T1029 - Scheduled Transfer](https://attack.mitre.org/techniques/T1029/)|Detect|Minimal|The following GuardDuty finding type flags events that may indicate adversaries attempting to exfiltrate data, such as sensitive documents, through the use of automated processing after being gathered during Collection.<br/>Behavior:EC2/TrafficVolumeUnusual<br/>Accuracy and Coverage is unknown, as this finding flags traffic volume that differs from a baseline.|
|[T1041 - Exfiltration Over C2 Channel](https://attack.mitre.org/techniques/T1041/)|Detect|Minimal|The following GuardDuty finding type flags events that may indicate adversaries attempting to exfiltrate data, such as sensitive documents.<br/>Behavior:EC2/TrafficVolumeUnusual<br/>Accuracy and Coverage is unknown, as this finding flags traffic volume that differs from a baseline.|
|[T1046 - Network Service Scanning](https://attack.mitre.org/techniques/T1046/)|Detect|Partial|The following GuardDuty finding types reflect flagged events where there is an attempt to get a list of services running on a remote host.<br/>Recon:EC2/PortProbeEMRUnprotectedPort Recon:EC2/PortProbeUnprotectedPort Recon:EC2/Portscan Impact:EC2/PortSweep|
|[T1048 - Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048/)|Detect|Partial|The following GuardDuty finding type flags events where adversaries may steal data by exfiltrating it over a different protocol than that of the existing command-and-control channel.<br/>Trojan:EC2/DNSDataExfiltration Behavior:EC2/TrafficVolumeUnusual|
|[T1071 - Application Layer Protocol](https://attack.mitre.org/techniques/T1071/)|Detect|Partial|GuardDuty flags events matching the following finding types that relate to adversaries attempting to communicate using application layer protocols to avoid detection.<br/>UnauthorizedAccess:EC2/MaliciousIPCaller.Custom Trojan:EC2/DropPoint!DNS Trojan:EC2/DropPoint Backdoor:EC2/C&CActivity.B!DNS Trojan:EC2/BlackholeTraffic Trojan:EC2/BlackholeTraffic!DNS<br/>|
|[T1078 - Valid Accounts](https://attack.mitre.org/techniques/T1078/)|Detect|Partial|GuardDuty implements a finding that flags occurrences unattended behavior from an IAM User in the Account.<br/>PenTest:IAMUser/KaliLinux, PenTest:IAMUser/ParrotLinux, PenTest:IAMUser/PentooLinux, Policy:IAMUser/RootCredentialUsage, PrivilegeEscalation:IAMUser/AdministrativePermissions, UnauthorizedAccess:IAMUser/ConsoleLogin, UnauthorizedAccess:IAMUser/ConsoleLoginSuccess.B, UnauthorizedAccess:IAMUser/MaliciousIPCaller, UnauthorizedAccess:IAMUser/MaliciousIPCaller.Custom, UnauthorizedAccess:IAMUser/TorIPCaller, Policy:S3/AccountBlockPublicAccessDisabled, Policy:S3/BucketAnonymousAccessGranted, Policy:S3/BucketBlockPublicAccessDisabled, Policy:S3/BucketPublicAccessGranted, CredentialAccess:IAMUser/AnomalousBehavior, DefenseEvasion:IAMUser/AnomalousBehavior, Discovery:IAMUser/AnomalousBehavior, Exfiltration:IAMUser/AnomalousBehavior, Impact:IAMUser/AnomalousBehavior, Persistence:IAMUser/AnomalousBehavior, Recon:IAMUser/MaliciousIPCaller, Recon:IAMUser/MaliciousIPCaller.Custom, UnauthorizedAccess:IAMUser/InstanceCredentialExfiltration|
|[T1090 - Proxy](https://attack.mitre.org/techniques/T1090/)|Detect|Minimal|The following GuardDuty finding type flags events where adversaries may use a connection proxy to direct network traffic between systems or act as an intermediary for network communications to a command-and-control server to avoid direct connections to their infrastructure.<br/>UnauthorizedAccess:EC2/TorClient UnauthorizedAccess:EC2/TorRelay<br/>Due to the detection being limited to a specific type of proxy, Tor, its coverage is Minimal resulting in a Minimal score.|
|[T1098 - Account Manipulation](https://attack.mitre.org/techniques/T1098/)|Detect|Partial|GuardDuty has a finding types that flag events where an adversary may have compromised an AWS IAM User.  Finding Type: Persistence:IAMUser/AnomalousBehavior|
|[T1110 - Brute Force](https://attack.mitre.org/techniques/T1110/)|Detect|Minimal|Finding types such as UnauthorizedAccess:EC2/RDPBruteForce, UnauthorizedAccess:EC2/SSHBruteForce, Impact:EC2/WinRMBruteForce, and Stealth:IAMUser/PasswordPolicyChange can detect when an EC2 instance may be involved in a brute force attack aimed at obtaining passwords.  Due to the detection being limited to a specific set of application protocols, its coverage is Minimal resulting in a Minimal score.|
|[T1189 - Drive-by Compromise](https://attack.mitre.org/techniques/T1189/)|Detect|Partial|There is a GuardDuty Finding that flags this behavior: Trojan:EC2/DriveBySourceTraffic!DNS|
|[T1190 - Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)|Detect|Minimal|There is a GuardDuty finding type that captures when vulnerable publicly facing resources are leveraged to capture data not intended to be viewable (e.g., IAM credentials associated with the resource).<br/>UnauthorizedAccess:EC2/MetadataDNSRebind - This finding type only detects MetadataDNSRebind and is more focused on the EC2 instance and not the application running on the instance itself resulting in Minimal coverage.|
|[T1485 - Data Destruction](https://attack.mitre.org/techniques/T1485/)|Detect|Partial|The following GuardDuty finding type flags events where adversaries may destroy data and files on specific systems or in large numbers on a network to interrupt availability to systems, services, and network resources.<br/>Impact:S3/MaliciousIPCaller, Impact:IAMUser/AnomalousBehavior Stealth:S3/ServerAccessLoggingDisabled UnauthorizedAccess:S3/MaliciousIPCaller.Custom UnauthorizedAccess:S3/TorIPCaller PenTest:S3/PentooLinux PenTest:S3/ParrotLinux PenTest:S3/KaliLinux|
|[T1486 - Data Encrypted for Impact](https://attack.mitre.org/techniques/T1486/)|Detect|Partial|The following GuardDuty finding type flags events where adversaries may encrypt data on target systems or on large numbers of systems in a network to interrupt availability to system and network resources.<br/>Impact:S3/MaliciousIPCaller Stealth:S3/ServerAccessLoggingDisabled UnauthorizedAccess:S3/MaliciousIPCaller.Custom UnauthorizedAccess:S3/TorIPCaller PenTest:S3/PentooLinux PenTest:S3/ParrotLinux PenTest:S3/KaliLinux|
|[T1491 - Defacement](https://attack.mitre.org/techniques/T1491/)|Detect|Partial|GuardDuty provides multiple finding types that flag malicious activity against resources. These findings focus on API calls that look suspicious and although they do not flag events such as Defacement specifically, it can be inferred that these findings can result in mitigating this technique's negative impact. With this assumption the score is capped at Partial.|
|[T1496 - Resource Hijacking](https://attack.mitre.org/techniques/T1496/)|Detect|Partial|The following GuardDuty finding types flag events where adversaries may leverage the resources of co-opted systems in order to solve resource intensive problems which may impact system and/or hosted service availability.<br/>CryptoCurrency:EC2/BitcoinTool.B CryptoCurrency:EC2/BitcoinTool.B!DNS Impact:EC2/BitcoinDomainRequest.Reputation UnauthorizedAccess:EC2/TorRelay|
|[T1498 - Network Denial of Service](https://attack.mitre.org/techniques/T1498/)|Detect|Partial|The following finding types in GuardDuty flag events where adversaries may perform Network Denial of Service (DoS) attacks to degrade or block the availability of targeted resources to users.<br/>Backdoor:EC2/DenialOfService.UdpOnTcpPorts Backdoor:EC2/DenialOfService.UnusualProtocol Backdoor:EC2/DenialOfService.Udp Backdoor:EC2/DenialOfService.Tcp Backdoor:EC2/DenialOfService.Dns|
|[T1526 - Cloud Service Discovery](https://attack.mitre.org/techniques/T1526/)|Detect|Partial|GuardDuty has the following finding types to flag events where there is an attempt to discover information about resources on the account.<br/>Recon:IAMUser/MaliciousIPCaller Recon:IAMUser/MaliciousIPCaller.Custom Recon:IAMUser/TorIPCaller|
|[T1530 - Data from Cloud Storage Object](https://attack.mitre.org/techniques/T1530/)|Detect|Partial|The following GuardDuty finding types flag events where adversaries may have access data objects from improperly secured cloud storage.<br/>UnauthorizedAccess:S3/MaliciousIPCaller.Custom UnauthorizedAccess:S3/TorIPCaller Impact:S3/MaliciousIPCaller Exfiltration:S3/MaliciousIPCaller Exfiltration:S3/ObjectRead.Unusual PenTest:S3/KaliLinux PenTest:S3/ParrotLinux PenTest:S3/PentooLinux UnauthorizedAccess:S3/MaliciousIPCaller.Custom UnauthorizedAccess:S3/TorIPCaller|
|[T1531 - Account Access Removal](https://attack.mitre.org/techniques/T1531/)|Detect|Partial|The following GuardDuty Finding type flags events where adversaries may interrupt availability of system and network resources by inhibiting access to accounts utilized by legitimate users.<br/>Impact:IAMUser/AnomalousBehavior|
|[T1552 - Unsecured Credentials](https://attack.mitre.org/techniques/T1552/)|Detect|Minimal|This control provides minimal to partial coverage for a minority of this technique's sub-techniques, and without specific coverage for its procedures, resulting in an overall score of Minimal.|
|[T1562 - Impair Defenses](https://attack.mitre.org/techniques/T1562/)|Detect|Partial|GuardDuty flags the following finding type DefenseEvasion:IAMUser/AnomalousBehavior as a defense evasion technique. It looks for API calls that delete, disable, or stop operations, such as, DeleteFlowLogs, DisableAlarmActions, or StopLogging. The following Finding types are examples:<br/>Stealth:IAMUser/CloudTrailLoggingDisabled Stealth:IAMUser/PasswordPolicyChange Stealth:S3/ServerAccessLoggingDisabled|
|[T1565 - Data Manipulation](https://attack.mitre.org/techniques/T1565/)|Detect|Partial|The following GuardDuty finding type flags events where adversaries may insert, delete, or manipulate data in order to manipulate external outcomes or hide activity.<br/>Impact:S3/MaliciousIPCaller|
|[T1566 - Phishing](https://attack.mitre.org/techniques/T1566/)|Detect|Partial|GuardDuty implements a finding type that flags/alerts when an EC2 service queries a Domain known to be tied to a phishing attack.<br/>Trojan:EC2/PhishingDomainRequest!DNS|
|[T1567 - Exfiltration Over Web Service](https://attack.mitre.org/techniques/T1567/)|Detect|Partial|The following finding types in GuardDuty flag events where adversaries may use an existing, legitimate external Web service to exfiltrate data rather than their primary command-and-control channel.<br/>Exfiltration:S3/ObjectRead.Unusual Exfiltration:S3/MaliciousIPCaller Exfiltration:IAMUser/AnomalousBehavior Behavior:EC2/TrafficVolumeUnusual|
|[T1568 - Dynamic Resolution](https://attack.mitre.org/techniques/T1568/)|Detect|Partial|GuardDuty has the following finding types to flag events where adversaries may dynamically establish connections to command-and-control infrastructure to evade common detections and remediations.<br/>Trojan:EC2/DGADomainRequest.B Trojan:EC2/DGADomainRequest.C!DNS|
|[T1571 - Non-Standard Port](https://attack.mitre.org/techniques/T1571/)|Detect|Partial|GuardDuty has the following finding type to flag events where adversaries may communicate using a protocol and port paring that are typically not associated.<br/>Behavior:EC2/NetworkPortUnusual|
|[T1580 - Cloud Infrastructure Discovery](https://attack.mitre.org/techniques/T1580/)|Detect|Partial|The following GuardDuty finding types flag events that are linked to Discovery techniques and can be used to capture events where a malicious user may be searching through the account looking for available resources. The finding types are also used to flag certain signatures of running services to detect malicious user activities from commonly used pentest operating systems.<br/>Discovery:IAMUser/AnomalousBehavior Discovery:S3/MaliciousIPCaller Discovery:S3/MaliciousIPCaller.Custom Discovery:S3/TorIPCaller PenTest:IAMUser/KaliLinux PenTest:IAMUser/ParrotLinux PenTest:IAMUser/PentooLinux PenTest:S3/KaliLinux PenTest:S3/ParrotLinux PenTest:S3/PentooLinux|
|[T1595 - Active Scanning](https://attack.mitre.org/techniques/T1595/)|Detect|Partial|Documentation states that the Service can flag such attempts: Reconnaissance -- Activity suggesting reconnaissance by an attacker, such as unusual API activity, intra-VPC port scanning, unusual patterns of failed login requests, or unblocked port probing from a known bad IP. Note: This is from the perspective of the resource running in the AWS account. Meaning GuardDuty has several finding types that flag events that take place via a resource (e.g., EC2, IAM, S3).|
  


### References
- <https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_finding-types-ec2.html#recon-ec2-portscan>
- <https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_findings.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='amazon-inspector'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 27. Amazon Inspector



Amazon Inspector is an automated assessment service that evaluates the security and compliance of applications in AWS. It supports assessment packages for CVEs, CIS Benchmarks (various Windows and Linux platforms), Best Practices (Linux only), and Network Reachability. The result of running an assessment is a list of findings that can be used to inform decision-making processes that improve the security of applications.  

- [Mapping File](AmazonInspector.yaml) ([YAML](AmazonInspector.yaml))
- [Navigator Layer](layers/AmazonInspector.json) ([JSON](layers/AmazonInspector.json))

### Mapping Comments


The CIS Benchmarks assessment package is considered out of scope because a separate project will be responsible for mapping CIS Benchmarks and ATT&CK.  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1003 - OS Credential Dumping](https://attack.mitre.org/techniques/T1003/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Furthermore, Amazon Inspector only supports a subset of the sub-techniques for this technique. Due to these things and the fact the security control is only supported for Linux platforms, the score is Minimal.|
|[T1021 - Remote Services](https://attack.mitre.org/techniques/T1021/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can detect a security control setting related to remote service access on Linux endpoints. Specifically, "Disable root login over SSH". This information can be used identify insecure configurations and harden the endpoints. Amazon Inspector does not directly protect against adversaries accessing remote services. Given Amazon Inspector can only assess this security control on Linux platforms (although it also supports Windows), it only restricts access to remote services for one user account, and only supports one sub-technique, the coverage score is Minimal leading to an overall Minimal score.|
|[T1037 - Boot or Logon Initialization Scripts](https://attack.mitre.org/techniques/T1037/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Furthermore, Amazon Inspector only supports a subset of the sub-techniques for this technique. Due to these things and the fact the security control is only supported for Linux platforms, the score is Minimal.|
|[T1046 - Network Service Scanning](https://attack.mitre.org/techniques/T1046/)|Protect|Partial|The Amazon Inspector Network Reachability assessment package can assess whether or not cloud/network components are vulnerable (e.g., publicly accessible from the Internet). Amazon Inspector does not directly protect cloud/network components rather reports on vulnerabilities that it identifies which can then be used to securely configure the cloud/network components. Due to this, the score is capped at Partial.|
|[T1053 - Scheduled Task/Job](https://attack.mitre.org/techniques/T1053/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Furthermore, Amazon Inspector only supports a subset of the sub-techniques for this technique. Due to these things and the fact the security control is only supported for Linux platforms, the score is Minimal.|
|[T1068 - Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068/)|Protect|Partial|Amazon Inspector can detect known vulnerabilities on various Windows and Linux endpoints. Furthermore, the Amazon Inspector Best Practices assessment package can assess security controls for "Enable Address Space Layout Randomization (ASLR)" and "Enable Data Execution Prevention (DEP)" that makes it more difficult for an attacker to exploit vulnerabilities in software. This information can be used to patch, isolate, and remove vulnerable software and endpoints. Amazon Inspector does not directly protect against exploitation and it is not effective against zero-day attacks, vulnerabilities with no available patch, and software that may not be analyzed by the scanner. As a result, the score is capped at Partial.|
|[T1070 - Indicator Removal on Host](https://attack.mitre.org/techniques/T1070/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Furthermore, Amazon Inspector only supports a subset of the sub-techniques for this technique. Due to these things and the fact the security control is only supported for Linux platforms, the score is Minimal.|
|[T1110 - Brute Force](https://attack.mitre.org/techniques/T1110/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can detect security control settings related to authentication and password policies on Linux endpoints. Specific security controls it can assess include "Disable password authentication over SSH", "Configure password maximum age", "Configure password minimum length", and "Configure password complexity" all of which impact the ability to brute force a password. This information can be used identify insecure configurations and harden the endpoints. Amazon Inspector does not directly protect against brute force attacks. Given Amazon Inspector can only assess these security controls on Linux platforms (although it also supports Windows), the coverage score is Minimal leading to an overall Minimal score.|
|[T1133 - External Remote Services](https://attack.mitre.org/techniques/T1133/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can detect a security control setting related to remote service access on Linux endpoints. Specifically, "Disable root login over SSH". This information can be used identify insecure configurations and harden the endpoints. Amazon Inspector does not directly protect against adversaries accessing remote services. Given Amazon Inspector can only assess this security control on Linux platforms (although it also supports Windows) and it only restricts access to remote services for one user account, the coverage score is Minimal leading to an overall Minimal score.|
|[T1189 - Drive-by Compromise](https://attack.mitre.org/techniques/T1189/)|Protect|Partial|Amazon Inspector can detect known vulnerabilities on various Windows and Linux endpoints. Furthermore, the Amazon Inspector Best Practices assessment package can assess security controls for "Enable Address Space Layout Randomization (ASLR)" and "Enable Data Execution Prevention (DEP)" that makes it more difficult for an attacker to exploit vulnerabilities in software. This information can be used to patch, isolate, and remove vulnerable software and endpoints. Amazon Inspector does not directly protect against exploitation and it is not effective against zero-day attacks, vulnerabilities with no available patch, and software that may not be analyzed by the scanner. As a result, the score is capped at Partial.|
|[T1190 - Exploit Public-Facing Application](https://attack.mitre.org/techniques/T1190/)|Protect|Partial|Amazon Inspector can detect known vulnerabilities on various Windows and Linux endpoints. Furthermore, the Amazon Inspector Best Practices assessment package can assess security controls for "Enable Address Space Layout Randomization (ASLR)" and "Enable Data Execution Prevention (DEP)" that makes it more difficult for an attacker to exploit vulnerabilities in software. This information can be used to patch, isolate, and remove vulnerable software and endpoints. Amazon Inspector does not directly protect against exploitation and it is not effective against zero-day attacks, vulnerabilities with no available patch, and software that may not be analyzed by the scanner. As a result, the score is capped at Partial.|
|[T1203 - Exploitation for Client Execution](https://attack.mitre.org/techniques/T1203/)|Protect|Partial|Amazon Inspector can detect known vulnerabilities on various Windows and Linux endpoints. Furthermore, the Amazon Inspector Best Practices assessment package can assess security controls for "Enable Address Space Layout Randomization (ASLR)" and "Enable Data Execution Prevention (DEP)" that makes it more difficult for an attacker to exploit vulnerabilities in software. This information can be used to patch, isolate, and remove vulnerable software and endpoints. Amazon Inspector does not directly protect against exploitation and it is not effective against zero-day attacks, vulnerabilities with no available patch, and software that may not be analyzed by the scanner. As a result, the score is capped at Partial.|
|[T1210 - Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210/)|Protect|Partial|Amazon Inspector can detect known vulnerabilities on various Windows and Linux endpoints. This information can be used to patch, isolate, and remove vulnerable software and endpoints. Furthermore, the Amazon Inspector Best Practices assessment package can assess a security control "Support SSH version 2 only" that prevents the use of a vulnerable version of SSH from being used as well as assess security controls for "Enable Address Space Layout Randomization (ASLR)" and "Enable Data Execution Prevention (DEP)" that makes it more difficult for an attacker to exploit vulnerabilities in software. Amazon Inspector does not directly protect against exploitation and it is not effective against zero-day attacks, vulnerabilities with no available patch, and software that may not be analyzed by the scanner. As a result, the score is capped at Partial.|
|[T1211 - Exploitation for Defense Evasion](https://attack.mitre.org/techniques/T1211/)|Protect|Partial|Amazon Inspector can detect known vulnerabilities on various Windows and Linux endpoints. Furthermore, the Amazon Inspector Best Practices assessment package can assess security controls for "Enable Address Space Layout Randomization (ASLR)" and "Enable Data Execution Prevention (DEP)" that makes it more difficult for an attacker to exploit vulnerabilities in software. This information can be used to patch, isolate, and remove vulnerable software and endpoints. Amazon Inspector does not directly protect against exploitation and it is not effective against zero-day attacks, vulnerabilities with no available patch, and software that may not be analyzed by the scanner. As a result, the score is capped at Partial.|
|[T1212 - Exploitation for Credential Access](https://attack.mitre.org/techniques/T1212/)|Protect|Partial|Amazon Inspector can detect known vulnerabilities on various Windows and Linux endpoints. Furthermore, the Amazon Inspector Best Practices assessment package can assess security controls for "Enable Address Space Layout Randomization (ASLR)" and "Enable Data Execution Prevention (DEP)" that makes it more difficult for an attacker to exploit vulnerabilities in software. This information can be used to patch, isolate, and remove vulnerable software and endpoints. Amazon Inspector does not directly protect against exploitation and it is not effective against zero-day attacks, vulnerabilities with no available patch, and software that may not be analyzed by the scanner. As a result, the score is capped at Partial.|
|[T1222 - File and Directory Permissions Modification](https://attack.mitre.org/techniques/T1222/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Due to this and the fact the security control is only supported for Linux platforms, the score is Minimal.|
|[T1489 - Service Stop](https://attack.mitre.org/techniques/T1489/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Due to this and the fact the security control is only supported for Linux platforms, the score is Minimal.|
|[T1529 - System Shutdown/Reboot](https://attack.mitre.org/techniques/T1529/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Due to this and the fact the security control is only supported for Linux platforms, the score is Minimal.|
|[T1543 - Create or Modify System Process](https://attack.mitre.org/techniques/T1543/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Furthermore, Amazon Inspector only supports a subset of the sub-techniques for this technique. Due to these things and the fact the security control is only supported for Linux platforms, the score is Minimal.|
|[T1548 - Abuse Elevation Control Mechanism](https://attack.mitre.org/techniques/T1548/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Furthermore, Amazon Inspector only supports a subset of the sub-techniques for this technique. Due to these things and the fact the security control is only supported for Linux platforms, the score is Minimal.|
|[T1562 - Impair Defenses](https://attack.mitre.org/techniques/T1562/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Furthermore, Amazon Inspector only supports a subset of the sub-techniques for this technique. Due to these things and the fact the security control is only supported for Linux platforms, the score is Minimal.|
|[T1595 - Active Scanning](https://attack.mitre.org/techniques/T1595/)|Protect|Partial|The Amazon Inspector Network Reachability assessment package can assess whether or not cloud/network components are vulnerable (e.g., publicly accessible from the Internet). Amazon Inspector does not directly protect cloud/network components rather reports on vulnerabilities that it identifies which can then be used to securely configure the cloud/network components. Due to this, the score is capped at Partial.|
|[T1599 - Network Boundary Bridging](https://attack.mitre.org/techniques/T1599/)|Protect|Minimal|The Amazon Inspector Best Practices assessment package can assess security control "Configure permissions for system directories" that prevents privilege escalation by local users and ensures only the root account can modify/execute system configuration information and binaries. Amazon Inspector does not directly protect against system modifications rather it just checks to see if security controls are in place which can inform decisions around hardening the system. Furthermore, Amazon Inspector only supports a subset of the sub-techniques for this technique. Due to these things and the fact the security control is only supported for Linux platforms, the score is Minimal.|
  


### References
- <https://docs.aws.amazon.com/inspector/latest/userguide/inspector_introduction.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='amazon-macie'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 28. Amazon Macie



Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to help you discover, monitor, and protect sensitive data in your AWS environment.  Macie automates the discovery of sensitive data, such as personally identifiable information (PII) and financial data, to provide you with a better understanding of the data that your organization stores in Amazon Simple Storage Service (Amazon S3).
Macie also provides you with an inventory of your S3 buckets, and it automatically evaluates and monitors those buckets for security and access control. Within minutes, Macie can identify and report overly permissive or unencrypted buckets for your organization.
If Macie detects sensitive data or potential issues with the security or privacy of your data, it creates detailed findings for you to review and remediate as necessary.

- [Mapping File](AmazonMacie.yaml) ([YAML](AmazonMacie.yaml))
- [Navigator Layer](layers/AmazonMacie.json) ([JSON](layers/AmazonMacie.json))

### Mapping Comments


Although the service detects the instance of sensitive data, it does not create an alert for the user to take immediate action. It does create a log report which the user can then view to see the results of the scan jobs.    


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1530 - Data from Cloud Storage Object](https://attack.mitre.org/techniques/T1530/)|Detect|Minimal|The following Macie findings can detect the collection of data from S3 buckets: Policy:IAMUser/S3BlockPublicAccessDisabled Policy:IAMUser/S3BucketEncryptionDisabled Policy:IAMUser/S3BucketPublic Policy:IAMUser/S3BucketReplicatedExternally Policy:IAMUser/S3BucketSharedExternally<br/>This type of detection is limited to only the S3 storage type and not other storage types available on the platform (such as file or block storage) and therefore has Minimal coverage resulting in a Minimal score.|
|[T1530 - Data from Cloud Storage Object](https://attack.mitre.org/techniques/T1530/)|Protect|Minimal|The following Macie findings can protect against collection of sensitive data from S3 buckets: SensitiveData:S3Object/Credentials SensitiveData:S3Object/CustomIdentifier SensitiveData:S3Object/Financial SensitiveData:S3Object/Multiple SensitiveData:S3Object/Personal<br/>The ability to discover this type of sensitive data stored in a bucket may lead to hardening steps or removing the data altogether which would prevent an adversary from being able to collect the data.<br/>This type of protection is limited to only the S3 storage type and not other storage types available on the platform (such as file or block storage) and therefore has Minimal coverage resulting in a Minimal score.|
|[T1537 - Transfer Data to Cloud Account](https://attack.mitre.org/techniques/T1537/)|Detect|Minimal|The following Macie findings can detect attempts to replicate data objects from a monitored bucket to an Amazon Web Services account that isn't part of your organization:<br/>Policy:IAMUser/S3BucketReplicatedExternally Policy:IAMUser/S3BucketSharedExternally<br/>This type of detection is limited to only the S3 storage type and not other storage types available on the platform (such as file or block storage) and therefore has Minimal coverage resulting in a Minimal score.|
|[T1552 - Unsecured Credentials](https://attack.mitre.org/techniques/T1552/)|Protect|Minimal|Macie only provides detection for the Credentials in Files sub-technique of this technique and only for the S3 storage type resulting in Minimal coverage and an overall Minimal score.|
|[T1567 - Exfiltration Over Web Service](https://attack.mitre.org/techniques/T1567/)|Detect|Minimal|Macie only provides detection of this technique for the S3 storage type and not other storage types offerred by the platform such as file or block storage resulting in a Minimal coverage score resulting in an overall score of Minimal.|
  


### Tags
- [Storage](#tag-storage)
  


### References
- <https://docs.aws.amazon.com/macie/latest/user/securityhub-integration.html#securityhub-integration-finding-example>
- <https://docs.aws.amazon.com/macie/latest/user/custom-data-identifiers.html>
- <https://docs.aws.amazon.com/macie/latest/user/what-is-macie.html>
- <https://docs.aws.amazon.com/macie/latest/user/discovery-jobs-manage.html>
- <https://docs.aws.amazon.com/macie/latest/user/findings-types.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='amazon-virtual-private-cloud'></a>

## ![GCP icon](/security-stack-mappings/icons/aws_icon.png) 29. Amazon Virtual Private Cloud



Amazon Virtual Private Cloud (Amazon VPC) is a service that lets you launch AWS resources in a logically isolated virtual network that you define.  Amazon VPC provides advanced security features that allow you to perform inbound and outbound filtering at the instance and subnet level.  Amazon VPC also has monitoring features that let you perform functions like out-of-band monitoring and inline traffic inspection, which help you screen and secure traffic.

- [Mapping File](AmazonVirtualPrivateCloud.yaml) ([YAML](AmazonVirtualPrivateCloud.yaml))
- [Navigator Layer](layers/AmazonVirtualPrivateCloud.json) ([JSON](layers/AmazonVirtualPrivateCloud.json))

### Mapping Comments


The mappings contained in this file were based on Amazon's "Security in Amazon Virtual Private Cloud" documentation listed in the references section. The following VPC components were assessed to produce this mapping: Security Groups, Network Access Control Lists (NACLs), VPC Peering, VPC Endpoints, and Virtual Private Network (VPN).  


### Techniques

|Technique|Category|Value|Comment|
| :--- | :--- | :--- | :--- |
|[T1008 - Fallback Channels](https://attack.mitre.org/techniques/T1008/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can be used to restrict external network access to the minimum required and can therefore mitigate an adversary utilizing a fallback or alternative communication channels.  In environments where unrestricted Internet access is required, security groups and NACLs can still be used to block known malicious endpoints.  Because in such environments the protection is limited to known  malicious IP addresses and domains and does not provide protection from such attacks from unknown domains and IP addresses, this is scored as partial coverage resulting in an overall Partial score.|
|[T1018 - Remote System Discovery](https://attack.mitre.org/techniques/T1018/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can filter network traffic and therefore can be effective for mitigating network based remote system discovery.  Other remote system discovery methods such as discovering hosts from local host files are not mitigated resulting in Partial coverage score and an overall score of Partial.|
|[T1021 - Remote Services](https://attack.mitre.org/techniques/T1021/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can provide partial protection for all of its sub-techniques and procedure examples resulting in an overall score of Partial.|
|[T1040 - Network Sniffing](https://attack.mitre.org/techniques/T1040/)|Protect|Significant|The VPC service's support for the AWS Virtual Private Network (VPN) can be used to encrypt traffic traversing over untrusted networks which can prevent information from being gathered via network sniffing.|
|[T1046 - Network Service Scanning](https://attack.mitre.org/techniques/T1046/)|Protect|Significant|VPC security groups and network access control lists (NACLs) can filter both internal and external network traffic and therefore, can mitigate unauthorized network service scanning.|
|[T1048 - Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can limit access to external hosts and can therefore provide mitigation of this technique.  For environments where Internet access is required, these controls can be used to block known malicious addresses.  Because this latter protection is limited to known malicious endpoints, it provides Partial coverage resulting in an overall Partial score.|
|[T1072 - Software Deployment Tools](https://attack.mitre.org/techniques/T1072/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can be used to limit access to critical network systems such as software deployment tools.|
|[T1090 - Proxy](https://attack.mitre.org/techniques/T1090/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can restrict ports and inter-system / inter-enclave connections as described by the Proxy related sub-techniques although it doesn't provide protection for domain-fronting.  It furthermore provides partial protection of this technique's procedure examples resulting in an overall Partial score.|
|[T1095 - Non-Application Layer Protocol](https://attack.mitre.org/techniques/T1095/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can be used to restrict external network access to the minimum required and can therefore mitigate adversary attempts to utilize non-application layer protocols for communication.  In environments where unrestricted Internet access is required, security groups and NACLs can still be used to block known malicious endpoints.  Because in such environments the protection is limited to known  malicious IP addresses and domains and does not provide protection from such attacks from unknown domains and IP addresses, this is scored as partial coverage resulting in an overall Partial score.|
|[T1133 - External Remote Services](https://attack.mitre.org/techniques/T1133/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can limit access to external remote services  to the minimum necessary.|
|[T1199 - Trusted Relationship](https://attack.mitre.org/techniques/T1199/)|Protect|Partial|VPC network access control lists (NACLs) can isolate portions of the network that do not require network-wide access, limiting some attackers that leverage trusted relationships such as remote access for vendor maintenance. Coverage partial, Temporal Immediate.|
|[T1205 - Traffic Signaling](https://attack.mitre.org/techniques/T1205/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can provide significant protection for some variations of this technique, for example Port Knocking.  Other variations of this technique such as using traffic signaling to execute a malicious task is not easily mitigated by security groups or NACLs.  Consequently, its coverage score is Partial resulting in an overall Partial score.|
|[T1210 - Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can be used to restrict access to remote services to the minimum necessary.|
|[T1219 - Remote Access Software](https://attack.mitre.org/techniques/T1219/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can be used to limit outgoing traffic to only sites and services used by authorized remote access tools.  This is scored as partial because it doesn't protect against an adversary using an authorized remote access tool for malicious activity.|
|[T1482 - Domain Trust Discovery](https://attack.mitre.org/techniques/T1482/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can be used to isolate sensitive domains to limit discovery.|
|[T1498 - Network Denial of Service](https://attack.mitre.org/techniques/T1498/)|Protect|Minimal|VPC security groups and network access control lists (NACLs) can be used to restrict access to endpoints but will prove effective at mitigating only low-end DOS attacks resulting in a Minimal score.|
|[T1499 - Endpoint Denial of Service](https://attack.mitre.org/techniques/T1499/)|Protect|Minimal|VPC security groups and network access control lists (NACLs) provides minimal protection for a majority of this control's sub-techniques and procedure examples resulting in an overall score of Minimal.|
|[T1542 - Pre-OS Boot](https://attack.mitre.org/techniques/T1542/)|Protect|Minimal|VPC security groups and network access control lists (NACLs) can provide partial protection coverage of Pre-OS Boot  mechanisms that utilize TFTP boot resulting in an overall score of Minimal.|
|[T1557 - Man-in-the-Middle](https://attack.mitre.org/techniques/T1557/)|Protect|Significant|The VPC service's support for the AWS Virtual Private Network (VPN) can be used to encrypt traffic traversing over untrusted networks which can mitigate Man-in-the-Middle attacks that manipulate network protocol data in transit. VPC Peering can also be utilized to route traffic privately between two VPCs which can reduce the Man-in-the-Middle attack surface.  VPC Endpoints can also similarly reduce the attack surface of Man-in-the-Middle attacks by ensuring network traffic between a VPC and supported AWS services are not exposed to the Internet.|
|[T1565 - Data Manipulation](https://attack.mitre.org/techniques/T1565/)|Protect|Partial|The VPC service's support for the AWS Virtual Private Network (VPN) can be used to encrypt traffic traversing over untrusted networks which can provide protection against one sub-technique (Transmitted Data Manipulation) of this technique while not providing protection for its remaining sub-techniques resulting in overall score of Partial.|
|[T1570 - Lateral Tool Transfer](https://attack.mitre.org/techniques/T1570/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can be used to limit traffic between systems and enclaves to minimum necessary for example via a zero-trust strategy.|
|[T1571 - Non-Standard Port](https://attack.mitre.org/techniques/T1571/)|Protect|Significant|VPC security groups and network access control lists (NACLs) can limit access to the minimum required ports and therefore, protect against adversaries attempting to use non-standard ports for C2 traffic.|
|[T1590 - Gather Victim Network Information](https://attack.mitre.org/techniques/T1590/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can prevent the gathering of victim network information via (active) scanning methods but is not effective against other methods of gathering victim network information such as via Phishing or online databases (e.g. WHOIS) resulting in a Partial coverage score and an overall Partial score.|
|[T1595 - Active Scanning](https://attack.mitre.org/techniques/T1595/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can be used to restrict inbound traffic that can protect against active scanning techniques such as Scanning IP Blocks and/or Vulnerability Scanning.  Because this protection is limited to known malicious IP addresses and domains and does not provide protection from such attacks from unknown domains and IP addresses, this is scored as partial coverage resulting in an overall Partial score.|
|[T1602 - Data from Configuration Repository](https://attack.mitre.org/techniques/T1602/)|Protect|Partial|VPC security groups and network access control lists (NACLs) can limit attackers' access to configuration repositories such as SNMP management stations, or to dumps of client configurations from common management ports.|
  


### Tags
- [Network](#tag-network)
  


### References
- <https://docs.aws.amazon.com/vpc/latest/userguide/security.html>
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>


# Control Tags
<a name='tag-auditing'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 1. Auditing


### Controls
- [AWS Audit Manager](#aws-audit-manager)

### Views
- [Navigator Layer](layers/tags/Auditing.json) ([JSON](layers/tags/Auditing.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-credentials'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 2. Credentials


### Controls
- [AWS Single Sign-On](#aws-single-sign-on)

### Views
- [Navigator Layer](layers/tags/Credentials.json) ([JSON](layers/tags/Credentials.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-database'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 3. Database


### Controls
- [AWS RDS](#aws-rds)

### Views
- [Navigator Layer](layers/tags/Database.json) ([JSON](layers/tags/Database.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-denial-of-service'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 4. Denial of Service


### Controls
- [AWS Shield](#aws-shield)

### Views
- [Navigator Layer](layers/tags/Denial_of_Service.json) ([JSON](layers/tags/Denial_of_Service.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-identity'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 5. Identity


### Controls
- [Amazon Cognito](#amazon-cognito)

### Views
- [Navigator Layer](layers/tags/Identity.json) ([JSON](layers/tags/Identity.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-internet-of-things'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 6. Internet of Things


### Controls
- [AWS IoT Device Defender](#aws-iot-device-defender)

### Views
- [Navigator Layer](layers/tags/Internet_of_Things.json) ([JSON](layers/tags/Internet_of_Things.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-iot'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 7. IoT


### Controls
- [AWS IoT Device Defender](#aws-iot-device-defender)

### Views
- [Navigator Layer](layers/tags/IoT.json) ([JSON](layers/tags/IoT.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-metrics'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 8. Metrics


### Controls
- [AWS CloudWatch](#aws-cloudwatch)

### Views
- [Navigator Layer](layers/tags/Metrics.json) ([JSON](layers/tags/Metrics.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-network'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 9. Network


### Controls
- [Amazon Virtual Private Cloud](#amazon-virtual-private-cloud)

### Views
- [Navigator Layer](layers/tags/Network.json) ([JSON](layers/tags/Network.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-not-mappable'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 10. Not Mappable


### Controls
- [Amazon Detective](#amazon-detective)

### Views
- [Navigator Layer](layers/tags/Not_Mappable.json) ([JSON](layers/tags/Not_Mappable.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-reports'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 11. Reports


### Controls
- [AWS Audit Manager](#aws-audit-manager)

### Views
- [Navigator Layer](layers/tags/Reports.json) ([JSON](layers/tags/Reports.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>

<a name='tag-storage'></a>
## ![tag icon](/security-stack-mappings/icons/tag-solid.svg) 12. Storage


### Controls
- [Amazon Macie](#amazon-macie)

### Views
- [Navigator Layer](layers/tags/Storage.json) ([JSON](layers/tags/Storage.json))
  

<p class="text-center"><a href="#contents">Back to Contents</a></p>


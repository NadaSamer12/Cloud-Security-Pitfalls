# Cloud Security Notes

## Cloud Service Models

### IaaS — Infrastructure as a Service

* Provides computing infrastructure on demand.
* The cloud provider manages physical servers and virtualization.
* The customer manages the operating system and resources above it.
* Security monitoring should cover workloads, cloud services, and the control plane.

### PaaS — Platform as a Service

* Provides a managed environment for building and hosting applications.
* The provider manages the underlying infrastructure and platform.
* Customers primarily focus on their applications and data.

### SaaS — Software as a Service

* Provides ready-to-use applications through the cloud.
* The provider manages most of the underlying infrastructure.
* Security monitoring focuses heavily on user activity, access, and available audit logs.

## Security of the Cloud

Cloud providers are responsible for securing their own underlying infrastructure, but customers should still monitor for risks involving:

* Compromised cloud accounts
* Supply-chain attacks
* Third-party vendor breaches
* Misconfigured resources
* Exposed sensitive data

Using a cloud service does not remove the need for security monitoring.

## Cloud Logging Challenges

Cloud environments can introduce difficulties when integrating logs with a SIEM:

* Some logging features require additional payment or licensing.
* Log formats may be incomplete or poorly documented.
* Some cloud products may have limited SIEM integration.
* SaaS environments can provide less visibility than on-premises infrastructure.

## Cloud Monitoring

Important areas to monitor include:

### Workloads

VMs and containers running in cloud environments.

### Cloud Services

Activities involving services such as databases and cloud storage.

### Control Plane

Administrative logins, configuration changes, and other actions performed through the cloud management interface.

## Cloud Security Tools

| Tool | Purpose                                           |
| ---- | ------------------------------------------------- |
| CASB | Enforces security policies for cloud applications |
| CWPP | Protects cloud workloads                          |
| CSPM | Detects and helps manage cloud misconfigurations  |

Examples of workload security tools include **Falco** and **Tetragon**.

## Common Cloud Migration Pitfalls

Moving an existing system to the cloud does not automatically make it secure.

Organizations should consider:

* Unpatched systems
* Weak passwords
* Missing MFA
* Exposed API keys
* Stolen session cookies
* Misconfigured cloud resources
* Insufficient logging
* Third-party and supply-chain risks

Cloud environments require security controls appropriate to the cloud model rather than simply copying traditional on-premises practices.

## Recommended Monitoring Approach

1. Identify all cloud platforms used by the organization.
2. Understand potential cloud and vendor risks.
3. Enable available cloud audit logs.
4. Enable workload logging for IaaS environments.
5. Forward relevant logs to a SIEM.
6. Monitor for suspicious logins and administrative actions.

## Key Takeaway

Cloud security requires continuous monitoring across workloads, cloud services, and administrative control planes. Effective SOC coverage depends on understanding the cloud service model, enabling available logs, and detecting suspicious activity.

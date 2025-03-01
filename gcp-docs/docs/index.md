# **Welcome to GCP Optimization Docs by Rohit**
# **Introduction**
In this documentation, we will discuss strategies to optimize Google Cloud Platform (GCP) costs and enhance efficiency.

---

### 1. What is GCP Optimization?
Google Cloud cost optimization is the process of managing and reducing cloud expenses while maximizing the value derived from GCP services. It involves tracking resource usage, cutting waste and making smart choices with GCP features.
### 2. Why GCP Optimization?
GCP cost optimization is necessary because cloud costs can quickly spiral out of control without proper management. As businesses scale their cloud operations, the complexity of resource allocation and pricing models increases. Optimization helps companies avoid unexpected bills, reduce waste and improve their return on cloud investments.

### 3. Best Practices for GCP Cost Optimization.
- ???  "Long-term Commitment Discounts"
    ### GCP offers two discount models:
    - SUDs (Sustained Use Discounts) – Monthly based
    - CUDs (Committed Use Discounts) – Yearly based (1-3 years)
    !!! info "Steps"
        -  Resource Forcasting.
        - Choose Appropriate Commitment(SUD or CUD).
        - Review Terms & conditions.
    !!! warning "Cons"
        - Overcommitment
        - Overspending
- ??? "Implementing Cloud Logging & Cloud Monitoring"
    !!! info "Steps"
        - Enable Cloud Monitoring & Cloud Logging.
        - Configure Metrics.
        - Setup Alerts.
        - Analyze. 
- ??? "Maximizing Resource Utilization"
    !!! info "Steps"
        - Monitor & Analyze.
        - Rightsize your resources.
        - Setup Preemptible VMs.
        - Identify and terminate Idle Resources.
        - Manage Quota Limits.
    !!! warning 
        - Preemptible VMs can be stopped by Google Cloud at any time.
        - They are cheaper than standard VMs but have limited availability.
- ??? "Leveraging Cost Management Tools"
    Leveraging cost management tools (both built-in GCP features and third-party solutions) provides deeper visibility into your cloud spending and identifies areas for optimization.
    - ***Example: Google Cloud Billing***  
- ??? "Adopting FinOps"
    ***FinOps*** (Financial Operations) is a cloud cost management and optimization practice that helps organizations control and optimize cloud spending while maintaining performance and innovation. It brings finance, engineering, and business teams together to make data-driven cloud spending decisions.
### 4. Compute Engine Cost Optimization.
??? question "Compute Engine Cost depends on"
    - Machine Type
    - CPU
    - Memory
    - Storage
    - Duration of Usage 
    - Local Storage(SSDs, HDDs and GPUs)
    - Data Transfer
    - Location(Regions and Zones of the VM  instances)
??? Question "How to Optimize Compute Engine"
    - Choose most effective VM type based on your Workload requirement.
    - Consider cost saving Preemptible VMs
    - Identify and stop unused VMs.
    - Implement Auto Scaling.
    - Run workloads(Application, service or processes) off-peak hours to leverage sustained use discounts.
    - Use CPU intensive workloads with vertical machine types offering more CPU per memory unit.
### 5. Google Cloud Database Optimization.
??? question "Depends On"
    - Type of Database
    - Size of Database
    - Storage Capacity
    - Data Transfer
    - Type of Database Service(Cloud SQL,Cloud Spanner or Cloud Bigtable)
??? question "How to Optimize Google Cloud Database Costs"
    - Rightsize database instances.
    - Use Read replicas for Load Balancing.
    - Leverage Comitted use discounts.
    - Implement proper indexing.
    - Implement efficient query design.
    - Implement data archiving strategies to move infrequently accessed data to cheaper storage options.
    - Use Caching mechanism for frequently accessed data.
    - Choose appropriate database service.
    - Optimize Connection Pooling.
    - Enable Auto scaling for read replicas.
    - Enable backups and Retention Policy.
    - Partition Larage Tables.
    - Shared Core Instances for low-traffic apps.
    - Regularly monitor and analyze database performance.
    !!! warning
        Use Cloud Spanner database service only for globally distributed, high-scale needs
### 6. How to Optimize Google Cloud Operations costs ?
Google Cloud Operations includes a suite of services designed to monitor, troubleshoot and optimize your Google Cloud environment. What primarily inflates your bill in GCP Cloud Operations is the use of advanced monitoring, logging and cost management functionalities beyond the free-tier features included with other Google Cloud services.
??? "Steps to Optimize the costs"
    - Leverage Free monitoring and logging.
    - Limit use of Prmium features like datailed metrices,anomaly detectionand longer log retention.
    - Avoid Using Ops Agent to reduce costs.
    - Setup Alerts for unexpected cost spikes
    - Regularly review cloud Billing reports.
### 7. Benefits of GCP Cost Optimization.
The main benefits of Google Cloud Platform (GCP) cost optimization address both financial and operational aspects of cloud management. By implementing effective cost optimization strategies, organizations can significantly reduce their cloud expenditures, enhance resource utilization, improve financial governance and visibility, and increase scalability and flexibility.
??? tip "Benefits"
    - Reduced Cost/billing
    - Enhanced Resource utilization
    - Improved financial governance and visibility
    - Scalability and flexibility
    - Increased Competitiveness
### 8. GCP Alerts based on Metrics
In Google Cloud Platform alerts are based on metrics collected from your resources.We can create alert policies to ***monitor performance, detect failures, and control costs.***

### **Three Types of Metric Alerts**
### 1. System Metrics
| Metric Type      | Description                          |
| :---------- | :----------------------------------- |
| CPU Utilization     |     Tracks CPU usage of VMs  |
| Memory Usage       | Monitors RAM consumption |
| Disk Usage    | Checks Disk Read/Write Activity |
| Network Traffic | Measures incoming/outgoing network data |

### 2. Application & Service Metrics
| Metric Type      |Metric                          |
| :---------- | :----------------------------------- |
| Cloud SQL    | Connection Count  |
| Kubernetes(GKE)      | Pod Restart count |
| Cloud Functions    | Execution Duration |
| Cloud Run | Request Latency |

### 3. Billing & Cost Metrics
| Metric Type      | Description                          |
| :---------- | :----------------------------------- |
| Budget Consumption     | Monitors Cloud Spending vs Budget  |
| Estimated Charges      | Tracks real-time cost estimates |
|Specific Service Cost    | Cost per service  |

## 9. How to Set Up Alerts in GCP
1. Open Cloud Monitoring
    - Go to **Google Cloud Console** :arrow_right: **Monitoring** :arrow_right: **Alerting**
2. Create an Alert Policy
    - Click **"Create Policy"**
    - Select a metric
    - Set **Threshold conditions**(e.g., CPU > 80%)
3. Add Notifications
    - Choose **Email, Slack, Webhook, SMS** for alerts
4. Save and Activate
    - Click **"Create"** and the alert is now active

---

# **Conclusion**
By following these best practices, you can significantly reduce costs, improve resource utilization, and enhance financial governance in GCP. Whether you're optimizing Compute Engine, databases, or monitoring costs, strategic planning will help you get the most value from your cloud investment.
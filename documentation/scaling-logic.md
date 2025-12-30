# Auto Scaling Logic

The Auto Scaling Group was configured with the following values:

- Desired capacity: 1
- Minimum capacity: 1
- Maximum capacity: 3

---

## Scale Out Policy
- Trigger: CPUUtilization > 60%
- Evaluation period: 1 minute
- Action: Launch a new EC2 instance

---

## Scale In Policy
- Trigger: CPUUtilization < 30%
- Evaluation period: 5 minutes
- Action: Terminate one EC2 instance

---

CloudWatch alarms were directly linked to Auto Scaling policies
to ensure automatic scaling based on workload.

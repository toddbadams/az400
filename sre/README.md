## Develop a Site Reliability Engineering (SRE) strategy (5-10%)
### Develop an actionable alerting strategy
- identify and recommend metrics on which to base alerts
- implement alerts using appropriate metrics
- implement alerts based on appropriate log messages
- implement alerts based on application health checks
- analyze combinations of metrics
- develop communication mechanism to notify users of degraded systems
- implement alerts for self-healing activities (e.g., scaling, failovers)
### Design a failure prediction strategy
- analyze behavior of system with regards to load and failure conditions
- calculate when a system will fail under various conditions
- measure baseline metrics for system
- leverage Application Insights Smart Detection and Dynamic thresholds in Azure Monitor
### Design and implement a health check
- analyze system dependencies to determine which dependency should be included in health check
- calculate healthy response timeouts based on SLO for the service
- design approach for partial health situations
- design approach for piecemeal recovery (e.g., to improve recovery time objective strategies)
- integrate health check with compute environment
- implement different types of health checks (container liveness, startup, shutdown)
# SIEM Tools and Their Functionality 

## Introduction: 
Security Information and Event Management (SIEM) tools are essential for monitoring and analyzing security-related logs. They help in identifying suspicious activities and ensuring timely responses to potential threats. 

## Key Points: 

1. Log Ingestion and Analysis: 

• SIEM tools collect security logs from various sources, including agents and port forwarding. 

• They analyze the logs for unwanted behaviors based on rules set by analysts. 

• If the criteria are met, an alert is triggered, prompting further investigation. 

2. Dashboards: 

• Dashboards are crucial components of a SIEM, displaying normalized data for analysis. 

• They summarize insights through actionable visuals, providing information such as: 

• Alert Highlights 

• System Notifications 

• Health Alerts 

• Counts of Failed Login Attempts 

• Events Ingested 

• Triggered Rules 

• Top Domains Visited 

• SIEM solutions usually have default dashboards, with options for custom dashboard creation. 

3. Correlation Rules: 

• These rules facilitate timely threat detection, allowing analysts to act quickly. 

• Examples include: 

• Alerting on multiple failed login attempts. 

• Notifying successful login after prior failures. 

• Raising alerts for USB use when restricted. 

• Triggering alerts for excessive outbound traffic indicating potential data exfiltration. 

4. Creating Correlation Rules: 

• Rules are created based on specific event logs to trigger alerts. 

• Use-Case examples include: 

• Logging attempts to clear event logs. 

• Detecting the execution of commands like "whoami" after exploitation. 

5. Alert Investigation: 

• After an alert is triggered, analysts review associated events to verify the alert's validity. 

• Actions post-analysis can include: 

• Tuning rules to reduce false positives. 

• Further investigation of true positives. 

• Contacting asset owners or isolating infected hosts if suspicious activity is confirmed. 

## Conclusion: 
SIEM tools are vital for monitoring security logs and responding to potential threats through established processes such as log ingestion, dashboard analysis, correlation rules, and alert investigations.
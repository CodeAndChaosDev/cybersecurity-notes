# Overview of Change Control Process

- The Change Control process is essential for implementing changes in environments with numerous devices, where simple updates can become complex.
- Technicians play a critical role in this process as they execute the actual changes required.
- Examples of changes include modifying allow or deny lists for applications, which help manage security by controlling which applications can run in the environment.

## Allow and Deny Lists

- Allow lists permit only specified applications to run, while deny lists block specific applications from executing.
- Deny lists are generally more flexible, allowing all applications except those explicitly named.
- Antivirus and antimalware systems can be considered large deny lists, permitting all applications except for identified harmful code.

## Change Control Board and Scope of Changes

- A Change Control Board oversees the change process, ensuring that changes are documented and limited to what is specified in the Change Control document.
- Scheduled time windows are allocated for specific updates, such as upgrading printer drivers, and changes outside of this scope are typically not permitted.
- However, technicians may need to make additional modifications that are necessary to achieve the primary goal of the change, highlighting the importance of flexibility within the documented process.

## Downtime Considerations

- Change Control often raises concerns about potential downtime, though not all changes require it.
- To minimize disruption, IT professionals typically schedule changes during non-production hours when fewer users are active.
- In 24x7 operational environments, strategies such as switching to secondary systems for updates can help avoid downtime.

Rebooting Systems Post-Change

- Rebooting may be necessary after implementing changes to ensure new configurations take effect.
- This can involve restarting the entire operating system or just specific services, depending on the nature of the change.
- Understanding the reboot requirements helps prepare for scenarios such as power outages and ensures systems can recover properly.

Managing Legacy Applications

- Legacy applications pose unique challenges during the Change Control process due to their long-standing use and lack of current support.
- These applications often come with warnings against making changes, as they may not be well understood by current staff.
- By documenting these legacy systems, IT professionals can bring them into the support cycle, improving overall management and understanding.

Dependencies in Change Control

- Dependencies complicate the Change Control process, as changes to one application may necessitate updates to others.
- For instance, updating firewall management software may require prior updates to the firewalls themselves.
- This interconnectedness means that a seemingly simple change can escalate into a broader update across multiple systems.

Importance of Documentation

- Continuous documentation is vital in the Change Control process to keep records current and accurate amidst frequent changes.
- Documentation updates may include network configurations, IP addresses, and procedures for managing new applications.
- Version Control systems are often employed to track changes and facilitate easy reversion to previous configurations if issues arise.

Version Control and Change Management

- Version Control plays a crucial role in managing changes, allowing for detailed tracking of modifications across systems.
- Some applications and operating systems have built-in Version Control, while others may require third-party solutions for effective management.
- This functionality helps ensure that IT professionals can monitor changes and revert to previous versions as necessary, maintaining system stability and integrity.


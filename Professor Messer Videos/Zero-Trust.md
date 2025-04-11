# Network Security and Zero Trust Model

- Many networks traditionally allow free movement within the network after passing through a firewall, which poses risks as both authorized and unauthorized users can access various systems without checks.
- Security administrators are increasingly adopting a zero trust model, which requires verification for every access attempt to network resources, regardless of the user's location within the network.
- In a zero trust environment, every device, process, and user must undergo security checks, which may include multi-factor authentication and data encryption during storage and transmission.
- Implementing zero trust involves creating a series of security policies and controls, often requiring additional firewalls and permissions to enhance security measures.

## Functional Planes of Security Devices

- To implement zero trust effectively, security devices can be divided into smaller components known as functional planes of operation, which can be physical, virtual, or cloud-based.
- These functional planes are broadly categorized into two types: the data plane and the control plane.
- The data plane is responsible for executing the actual security processes, such as processing network packets and forwarding data in real time.
- The control plane manages the operations of the data plane by configuring policies and rules that dictate how data should be handled and routed within the network.
- Understanding the distinction between the data plane and control plane can be illustrated by examining a physical switch, where the data plane handles traffic while the control plane manages configurations and address settings.

## Adaptive Identity and Enhanced Security Controls

- To strengthen security in a zero trust model, organizations can employ adaptive identity technology, which assesses user identity and applies security controls based on various factors beyond just user input.
- This involves evaluating the source of access requests, such as identifying discrepancies between a user's location and their IP address, which could indicate potential unauthorized access.
- Additional considerations in the authentication process include the user's relationship with the organization and their physical location, all of which contribute to a more robust verification of identity.
- By analyzing multiple data points, organizations can implement stronger authentication measures as needed, thereby enhancing overall security.

## Security Zones and Access Control Policies

- Security zones categorize different areas of a network to better manage access and trust levels, allowing for a more nuanced approach to security than simple user-server relationships.
- These zones can differentiate between trusted and untrusted networks, enabling the establishment of rules that restrict access based on the originating zone.
- For instance, users in a corporate office (trusted zone) may have different access privileges compared to users connecting from an untrusted zone, such as a public Wi-Fi network.
- Creating separate VPN connections for different departments or groups within an organization can further enhance security and control over inter-zone communications.

## Policy Enforcement Points and Decision Making

- To enforce security policies effectively, a policy enforcement point acts as a gatekeeper that evaluates all network traffic and subjects, ensuring compliance with established security protocols.
- This point does not make decisions on whether to allow or deny traffic; instead, it gathers relevant data and forwards it to a policy decision point for evaluation.
- The policy decision point examines authentication requests against predefined security policies and determines whether access should be granted, denied, or revoked.
- Results from the policy decision are communicated back to the policy enforcement point, which then implements the decision regarding access to network resources.

## Integrating Zero Trust into Network Architecture

- The overall zero trust model integrates various components, starting with subjects and systems communicating from untrusted zones over the data plane and through the policy enforcement point.
- If a policy enforcement is required, the enforcement point relays this need to the policy administrator, who then coordinates with the policy engine to make access decisions.
- The final decision regarding whether traffic is allowed is communicated back to the policy enforcement point, which then facilitates access to the trusted zone and the requested enterprise resources.


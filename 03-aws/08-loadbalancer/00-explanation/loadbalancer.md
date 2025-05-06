# AWS Load Balancer Explanation
AWS Load Balancer is a managed service that distributes incoming traffic across multiple targets (like EC2 instances, containers, or IP addresses) to ensure high availability, fault tolerance, and better performance.

# Types of AWS Load Balancers
- Application Load Balancer (ALB) - Works at Layer 7 (HTTP/HTTPS) - ideal for routing traffic based on URL paths, hostnames, or headers
- Network Load Balancer (NLB) - Works at Layer 4 (TCP/UDP/TLS) - used for low-latency, high-performance applications
- Gateway Load Balancer (GWLB) - Used mainly for integrating third-party virtual appliances like firewalls and traffic monitoring tools
- Classic Load Balancer (CLB) - Legacy load balancer working at both Layer 4 and Layer 7, but mostly replaced by ALB and NLB

# Proxy Server Monitoring
<h2>Overview</h2>
A requierement for a server that is used for SSL offloading and proxies thousands of request, is in need of capture critical and evaluation of metric data, to identify issues, set preventive actions, and capacity planning.
This document is a very abstract about key metrics and their challenges/goals.

<h2>Key Metrics</h2>
<h3>Hardware related</h3>

- CPU load average (1, 5, 15): Keep track of CPU usage for capacity planning or find an issue in combination with other metrics.
- RAM usage: Keep track of RAM usage for capacity planning or find an issue in combination with other metrics.
- Disk free space/inodes: Keep track of Disk usage for capacity planning or find any issue in combination with other metrics.
- SMART status: Preventive actions (replacement) maybe needed for a physical disk drive.
- NIC inbound/outbound traffic: Keep track of resource usage for capacity planning or find any issue in combination with other metrics.
- NIC Link Aggregation status: Identify if a NIC or switch could be failing.

<h3>Proxy related</h3>

- Request per second: Find any abnormal behaviour to detect DDOS (in combination with NIC traffic), or a unusual drop in the RPS due to backend node failing, a network issue, or CPU/RAM overload.
- Error logs: To identify any error within the proxy configuration, or the SSL offloading.
- SSL certificates (public): Validate expiration date, domains, and root certificate authorities.

<h3>Backend pool related</h3>

- Node health checks: Combined with RPS to help in identifiying if a specific issue with a node.
- SSL certificates (internal): Validate expiration date, domains, and root certificate authorities.

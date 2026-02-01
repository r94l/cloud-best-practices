### ☁️ On Today’s Episode of Cloud & Troubleshooting: The Case of the Missing DNS

A critical virtual machine on Azure suddenly stopped resolving DNS. This wasn’t just any VM. It powered key internal services, so downtime wasn’t an option.

The customer believed it was using the Azure-provided DNS on the VNet… but a quick nslookup told a different story. The VM was pointing to a random IP instead of the default 168.63.129.16.

Time to investigate 🔍
Ping to the DNS IP → unreachable
Port 53 → no connectivity

Digging deeper, we found the NIC DNS setting was configured to Custom instead of “Inherit from Virtual Network.” Using PowerShell, we reset it to Azure’s default DNS, confirmed the NIC configuration in the portal and instantly, name resolution came back to life ⚡

💡 Lesson of the day:
Even a small DNS misconfiguration can cripple critical workloads. And on a larger scale like the recent AWS Route 53 incident — DNS disruptions can bring down entire regions and services..

To avoid that:
 ✅ Standardize DNS settings using Azure Policy
 ✅ Regularly audit network configurations
 ✅ Monitor for unreachable DNS endpoints
Because when DNS breaks; Everything breaks.

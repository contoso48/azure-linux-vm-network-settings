# azure-linux-vm-network-settings
Linux OS settings to increase throughput across high latency, congested networks, especially with single-threaded large file transfers. 
Tested on Azure Marketplace Image with Ubuntu 24.02

Use-case example:
Linux client in West US region pulling single large (GB) file from a source system (example GitHub Enterprise Server) in West Europe region, over 150ms apart in latency.    
- Default Azure Marketplace Linux OS settings will achieve X transfer rates
   - Same VMs with updated OS settings in this example achieve over 3x of untuned transfer rate
- Example measurement with "iperf3 -n 2048M -c ipaddr -w 32M"
   - 100-200Mbps single threaded test without tuning
   - and >1Gbps with OS network setting applied


UPDATE:  
- Official Microsoft Learn documentation is available on this topic
- https://learn.microsoft.com/en-us/azure/virtual-network/virtual-network-optimize-network-bandwidth
- https://learn.microsoft.com/en-us/azure/virtual-network/virtual-network-tcpip-performance-tuning
- https://learn.microsoft.com/en-us/azure/virtual-network/virtual-machine-network-throughput
- https://learn.microsoft.com/en-us/azure/virtual-network/how-to-virtual-machine-mtu

And during Ignite 2025 conference, they demoed this briefly at 31 minutes into the session: 
- https://ignite.microsoft.com/en-US/sessions/BRK143 


Credit goes to https://github.com/naioja for creating these and helping me test & validate them 
Example only - no guarantee of getting same result in all situations


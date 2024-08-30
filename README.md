# azure-linux-vm-network-settings
Linux OS settings to increase throughput across high latency, congested networks
Tested on Azure Marketplace Image with Ubuntu 24.02

Use-case example:
Linux client in West US region pulling single large (GB) file from a source system (example GitHub Enterprise Server) in West Europe region, over 150ms apart in latency.    
- Default Azure Marketplace Linux OS settings will achieve X transfer rates
- Same VMs with updated OS settings in this example achieve over 2x to 3s transfer rates.
- Example measurement with "iperf3 -n 2048M -c <ipaddr> -w 32M"
   - 100-200Mbps single threaded test without tuning
   - and >1Gbps with OS network setting applied

Credit goes to https://github.com/naioja for creating these and helping me test & validate them 

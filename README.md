# azure-linux-vm-network-settings
Linux OS settings to increase throughput across high latency, congested networks

Use-case example:
Linux client in West US region pulling single large (GB) file from a source system (example GitHub Enterprise Server) in West Europe region, over 150ms apart in latency.    
- Default Azure Marketplace Linux OS settings will achieve ~400-600Mbps transfer rates
- Same VMs with updated OS settings in this example achieve over 2 to 3 Gbps transfer rates, so 3x or more. 

Credit goes to https://github.com/naioja for creating these and helping me test & validate them 

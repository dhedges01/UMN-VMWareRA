# UMN-VMWareRA
Powershell wrappers for interacting with VMWare 6.5+ Rest API

Functions

Get-VMWareRAVMMac
This function is used to grab the mac address of a sincle connected nic.  Look at 'GET /vcenter/vm/{vm}/hardware/ethernet' to get more information about all nics associated with a vm

New-VMWareRAVM
diskSizeGB will take an array of Integers to build multiple disks.  You can still use secondDiskSizeGB and it will work as expected


# Releases
## 1.2.1 -- 2/15/18
Add docs and code signing.

## Prior to 1.2.1
Send array of integers to disksizeGB in newVM function  .Fix get-vmwareravm function to return ID.  Return null if Get-VMWareRAVMID cant find ID.  Fix recursion issue.  Update Get-VMWareRAVMID so ignore case sensativity.  Fix Get-VMWareRAVTag, Addfuctions to get host and cluster, expand get vm to do a better search, Add function Get-VMWareRAVMMac, Add -UseBasicParsing switch to invoke-webrequest to run on server-core
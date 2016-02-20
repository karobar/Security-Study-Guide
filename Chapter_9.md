# Disk Redundancy 
#### RAID-0 (striping)
 - doesn't provide any redundancy or fault tolerance.
 - Includes 2+ physical disks. 
 - Files stored on a RAID-0 array are spread acrosss each of the disks
 - increased read/write performance

#### RAID-1 (mirroring)
 - uses two disks
 - data written on one disk is also written to the other disk.
 - each of the disks also has its own **disk controller**
 - You can add an additional **disk controller** to a RAID-1 configuration to remove the disk controller as a single point of failure. This is called **disk duplexing**

#### RAID-5
 - 3+ disks that are striped together (similar to RAID-0)
 - The equivalent of one drive includes **parity information**, which is striped across each drive and is used for fault tolerance
 - If a drive fails, the system can read the information on the remaining drives and determine what the actual data should be.
 - If two of the drives fail, the data is lost

#### RAID-6
 - An extension of RAID-5
 - includes an extra parity block
 - will continue to operate even if two disk drives fail.
 - Requires 4+ disks

#### RAID-10/RAID 1+0
 - combines the features of mirroring from RAID-1 and striping from RAID-0
 - has a variantion is RAID-01 or RAID 0+1 with a slightly different implementation

Hardware | Software RAID
---|---
significantly better performance | significantly worse performance
dedicated hardware manages the disks in the RAID, removing the load from the OS | The OS manages the disks in the RAID array
often includes extra features | 
can logically remove a failed disk out of the configuration, add an online spare into the configuration, and rebuild the array; which can happen without admin intervention |
often **hot-swappable**, allowing admins to swap out the failed drive without powering the system down |

###### Five Nines
achieving 99.999% uptime

###### Scaling Up
adding additional resources such as processors and/or memory

###### Scaling Out
adding additional servers (managed with a load balancer)

Load-Balanced Cluster | Failover Cluster
---|---
systems don't need to share storage | systems need to share the same storage
less expensive | more expensive
easier to add servers | more difficult to add servers

Redundancy | Backups
---|---
fire can destroy all redundant data | fire can't destroy (proper) backups

---
# BCP (Business Continuity Plan)
looks at an entire organization and can include one or more DRPs (Disaster Recovery Plans)
#### BIA (Business Impact Analysis)
Example: if a disaster such as a hurricane hit, what services must the organization restore to stay in business?
#### RTO (Recovery Time Objective)
 - the maximum amount of time it can take to restore a system after an outage
 - Example: An organization that sells products via a web site generates $10,000 in revenue an hour. It might decide that the maximum acceptable outage for the web server is five minutes. The RTO would then be five minutes.

#### RPO (Recovery Point Objective)
 - identifies a point in time where data loss is acceptable. 
 - Example: a server may host archived data that has very few changes on a weekly basis. Management might decide that some data loss is acceptable, but they always want to be able to recover data from at least the previous week. In this case, the RPO is one week

#### COOP (Continuity Of Operations Planning)
 - focuses on restoring critical business functions at an alternate location after a critical outage. 
 - example: a hurricane prevents a company from operating in one location, a COOP site allows it to continue to provide critical services at an alternate location

###### Hot Site
 - when you need to be operational within 60 minutes
 - operational 24/7
 - includes all equipment, software, and communication capabilities of the primary site
 - up-to-date data and backups

###### Cold site
when you need to be operational within a few days
###### Warm site
when you need to be operational within 60 minutes - a few days
###### Mobile site
non-permanent location

---
###### HVAC (Heating, Ventilation, and Air Conditioning)

---
###### Fail-Safe = Fail-Secure == Fail-Close


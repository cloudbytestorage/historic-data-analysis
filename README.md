# Historic Data Analysis
Tools/Visualizations for Historic data. 

## Goal
Based on the historic data collected from the system, the Visualizations should provide insights into usage patterns and abilitity to quickly detect anomolies/changes in the usage patterns.

## Data Input Format
Historic data can include one or more metrics and can be collected from one or more entities. 

For example:
- Network stats (in packets, out packets, in errs, out errs)  from different network interfaces of a system.
- Processor stats (user, system, idle, interrupt) of different CPUs of a system. 
- Storage Space Stats (used, available) of different disks in a system 
- Storage Performance Stats (reads, writes, read throughput, write throughput ) of different disks in a system 

There can be multiple data input files, and each data input file can have multiple entities belonging to the same group (entities that share the same metrics). For example, CPU0, CPU1 stats can be provided in the same file, but not CPU0 and Disk0. 

The input(csv) file format is as shown below:
```
Date, Timestamp, EntityName, Param1, Param2, Param3, Param4, ...
2016-09-09,11:37:00.270, Ent1, Val-111, Val-121, Val-131, Val-141, ... 
2016-09-09,11:37:00.370, Ent2, Val-211, Val-221, Val-231, Val-241, ...
2016-09-09,11:37:00.870, Ent3, Val-311, Val-321, Val-331, Val-341, ...
2016-09-09,11:39:00.165, Ent1, Val-112, Val-122, Val-132, Val-142, ... 
2016-09-09,11:39:00.175, Ent2, Val-212, Val-222, Val-232, Val-242, ...
2016-09-09,11:39:00.190, Ent3, Val-312, Val-322, Val-332, Val-342, ...
2016-09-09,11:42:00.164, Ent1, Val-113, Val-123, Val-133, Val-143, ... 
2016-09-09,11:42:00.185, Ent2, Val-213, Val-223, Val-233, Val-243, ...
2016-09-09,11:42:00.290, Ent3, Val-313, Val-323, Val-333, Val-343, ...

```
There can be multiple data input files like above. 






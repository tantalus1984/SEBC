### My cluster's specification
* Worker vcores: 4
* Worker spindles: 1 SSD. For the purpose of this exercise assuming 6
* Worker RAM: 15GB
* Workload factor: 2
* Worker nodes: 3

### Necessary adjustments
* without adjustments YARN resources = -1
* this is because my cluster has less vcores than this excel would minimally expect
* fixing this by setting CM Agent vcores=0 and DataNode vcores=0 assuming they are sharing a vcore together with OS
* also setting OS vcores=1
* setting OS memory to 2GB (1,5 GB might not be enough and in case of physical machines we need an even number here)

### Workload factor
* Workload factor states the ratio between a job's CPU core utilization and Disk utilization behavior
* A value of 1 means that your job's CPU core/disk utilization is balanced. Account for one disk spindle per CPU. Your workload is very disk I/O intensive. Disk I/O intensive jobs are typically scanning/writing lots of data from/to disk (e.g., teragen, WordCount, etc.)
* A value of 2 or 4 means that your job requires more CPU cores per spindle because it is doing more complex processing on data. Your job is disk I/O-bound. Examples include analytical workloads (e.g., Machine Learning algorithms), such as Apache Spark's MLlib

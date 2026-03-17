# CRUD General Purpose Ranking

The benchANT CRUD General Purpose Ranking enables the performance and price-performance comparison of various relational and NoSQL DBMS operated on IaaS across multiple cloud providers. 

The following tables show the specifications on DBMS, cloud infrastructure and benchmark level to ensure transparency, comparability and reproducibility. 

For each DBMS, benchANT specifies a vanilla configuration as a baseline comparison and there is the option to tune specific DBMS and cloud infrastructure parameters.


## Scaling Size XSMALL 

### DBMS Specification
| DBMS Parameter | Description                                                      | Vanilla Value     | Tunable |
|-----------------------|------------------------------------------------------------------|-------------------|----------|
| DBMS Version          | The DBMS version                                     | as specified          | yes      |
| DBMS Configuration    | DBMS server configuration | provider default  | yes      |
| Cluster Size          | number of nodes for this scaling size                             | 1                 | no      |
| Replication Factor     | Replication factor per data item                                          | 1               | no      |



### Cloud Infrastructure Specification

| Cloud Infrastructure Parameter | Description                                                                                       | Vanilla Value           | Tunable |
|--------------------------------|---------------------------------------------------------------------------------------------------|--------------------------|----------|
| Region                         | The target region to deploy the DBMS instance         | Frankfurt                | yes      |
| Availability Zone              | The target availability zone(s) to deploy the DBMS instances                                     |  not specified       | yes      |
| instance type                         | The VM instance type                             | general purpose                    | yes       |
| vCores                         | The  number of vCores to be used for this specific scaling size                            | 2                        | no       |
| Memory                         | The  amount of RAM to be used for this specific scaling size (in GiB)                      | 8                       | no      |
| Storage Size                   | The storage size per node for this specific scaling size (in GB)                                  | 100                      | no      |
| Storage Type                   | The storage type per node for this specific scaling size; the minimal considered type is SSD       | SSD (cheapest option as specified)     | yes      |


### Benchmark Specification

| Benchmark Parameter | Description                                                                 | Value                |
|----------------------|------------------------------------------------------------------------------|----------------------|
| Cloud                | The target cloud to run the benchmark VM                                    | same as DBMS        |
| Region               | The target cloud region to run the benchmark VM                             | same as DBMS        |
| Availability Zone    | The target availability zone to deploy the benchmark VM                     | not specified or identical to the DBMS if specified for the DBMS        |
| VM Type              | The target VM type to run the benchmark                                     | 16 Cores / 32 GB RAM |
| Benchmark Suite      | Yahoo Cloud Serving Benchmark                                               | YCSB            |
| Workload             | YCSB core workload                                           | site.ycsb.workloads.CoreWorkload                |
| Threads          | The applied number of threads for this scaling size | 50                  |
| Items            | The data items initially loaded into the DBMS | 5,000,000                   |
| Item Size (KB)           | The data size of a single item | 0.5                   |
| Read Ratio            | The ratio of read requests | 50                   |
| Insert Ratio            | The ratio of insert requests | 50                   |
| Request Distribution            | The read access pattern | zipfian                   |
| Runtime              | The runtime of the workload in minutes; workloads are always run during daytime business hours | 30                   |


## Scaling Size SMALL 

### DBMS Specification
| DBMS Parameter | Description                                                      | Vanilla Value     | Tunable |
|-----------------------|------------------------------------------------------------------|-------------------|----------|
| DBMS Version          | The DBMS version                                     | as specified          | yes      |
| DBMS Configuration    | DBMS server configuration | provider default  | yes      |
| Cluster Size          | number of nodes for this scaling size                             | 1                 | no      |
| Replication Factor     | Replication factor per data item                                          | 1               | no      |



### Cloud Infrastructure Specification

| Cloud Infrastructure Parameter | Description                                                                                       | Vanilla Value           | Tunable |
|--------------------------------|---------------------------------------------------------------------------------------------------|--------------------------|----------|
| Region                         | The target region to deploy the DBMS instance         | Frankfurt                | yes      |
| Availability Zone              | The target availability zone(s) to deploy the DBMS instances                                     |  not specified       | yes      |
| instance type                         | The VM instance type                             | general purpose                    | yes       |
| vCores                         | The  number of vCores to be used for this specific scaling size                            | 4                        | no       |
| Memory                         | The  amount of RAM to be used for this specific scaling size (in GiB)                      | 16                       | no      |
| Storage Size                   | The storage size per node for this specific scaling size (in GB)                                  | 100                      | no      |
| Storage Type                   | The storage type per node for this specific scaling size; the minimal considered type is SSD       | SSD (cheapest option as specified)     | yes      |


### Benchmark Specification

| Benchmark Parameter | Description                                                                 | Value                |
|----------------------|------------------------------------------------------------------------------|----------------------|
| Cloud                | The target cloud to run the benchmark VM                                    | same as DBMS        |
| Region               | The target cloud region to run the benchmark VM                             | same as DBMS        |
| Availability Zone    | The target availability zone to deploy the benchmark VM                     | not specified or identical to the DBMS if specified for the DBMS        |
| VM Type              | The target VM type to run the benchmark                                     | 16 Cores / 32 GB RAM |
| Benchmark Suite      | Yahoo Cloud Serving Benchmark                                               | YCSB            |
| Workload             | YCSB core workload                                           | site.ycsb.workloads.CoreWorkload                |
| Threads          | The applied number of threads for this scaling size | 100                  |
| Items            | The data items initially loaded into the DBMS | 5,000,000                   |
| Item Size (KB)           | The data size of a single item | 0.5                   |
| Read Ratio            | The ratio of read requests | 50                   |
| Insert Ratio            | The ratio of insert requests | 50                   |
| Request Distribution            | The read access pattern | zipfian                   |
| Runtime              | The runtime of the workload in minutes; workloads are always run during daytime business hours | 30                   |


## Scaling Size MEDIUM 

### DBMS Specification
| DBMS Parameter | Description                                                      | Vanilla Value     | Tunable |
|-----------------------|------------------------------------------------------------------|-------------------|----------|
| DBMS Version          | The DBMS version                                     | as specified          | yes      |
| DBMS Configuration    | DBMS server configuration | provider default  | yes      |
| Cluster Size          | number of nodes for this scaling size                             | 3                 | no      |
| Replication Factor     | Replication factor per data item                                          | 3               | no      |



### Cloud Infrastructure Specification

| Cloud Infrastructure Parameter | Description                                                                                       | Vanilla Value           | Tunable |
|--------------------------------|---------------------------------------------------------------------------------------------------|--------------------------|----------|
| Region                         | The target region to deploy the DBMS instance         | Frankfurt                | yes      |
| Availability Zone              | The target availability zone(s) to deploy the DBMS instances                                     |  not specified       | yes      |
| instance type                         | The VM instance type                             | general purpose                    | yes       |
| vCores                         | The  number of vCores to be used for this specific scaling size                            | 4                        | no       |
| Memory                         | The  amount of RAM to be used for this specific scaling size (in GiB)                      | 16                       | no      |
| Storage Size                   | The storage size per node for this specific scaling size (in GB)                                  | 100                      | no      |
| Storage Type                   | The storage type per node for this specific scaling size; the minimal considered type is SSD       | SSD (cheapest option as specified)     | yes      |


### Benchmark Specification

| Benchmark Parameter | Description                                                                 | Value                |
|----------------------|------------------------------------------------------------------------------|----------------------|
| Cloud                | The target cloud to run the benchmark VM                                    | same as DBMS        |
| Region               | The target cloud region to run the benchmark VM                             | same as DBMS        |
| Availability Zone    | The target availability zone to deploy the benchmark VM                     | not specified or identical to the DBMS if specified for the DBMS        |
| VM Type              | The target VM type to run the benchmark                                     | 16 Cores / 32 GB RAM |
| Benchmark Suite      | Yahoo Cloud Serving Benchmark                                               | YCSB            |
| Workload             | YCSB core workload                                           | site.ycsb.workloads.CoreWorkload                |
| Threads          | The applied number of threads for this scaling size | 100                  |
| Items            | The data items initially loaded into the DBMS | 5,000,000                   |
| Item Size (KB)           | The data size of a single item | 0.5                   |
| Read Ratio            | The ratio of read requests | 50                   |
| Insert Ratio            | The ratio of insert requests | 50                   |
| Request Distribution            | The read access pattern | zipfian                   |
| Runtime              | The runtime of the workload in minutes; workloads are always run during daytime business hours | 30                   |


## Scaling Size LARGE 

### DBMS Specification
| DBMS Parameter | Description                                                      | Vanilla Value     | Tunable |
|-----------------------|------------------------------------------------------------------|-------------------|----------|
| DBMS Version          | The DBMS version                                     | as specified          | yes      |
| DBMS Configuration    | DBMS server configuration | provider default  | yes      |
| Cluster Size          | number of nodes for this scaling size                             | 3                 | no      |
| Replication Factor     | Replication factor per data item                                          | 3               | no      |



### Cloud Infrastructure Specification

| Cloud Infrastructure Parameter | Description                                                                                       | Vanilla Value           | Tunable |
|--------------------------------|---------------------------------------------------------------------------------------------------|--------------------------|----------|
| Region                         | The target region to deploy the DBMS instance         | Frankfurt                | yes      |
| Availability Zone              | The target availability zone(s) to deploy the DBMS instances                                     |  not specified       | yes      |
| instance type                         | The VM instance type                             | general purpose                    | yes       |
| vCores                         | The  number of vCores to be used for this specific scaling size                            | 8                        | no       |
| Memory                         | The  amount of RAM to be used for this specific scaling size (in GiB)                      | 32                       | no      |
| Storage Size                   | The storage size per node for this specific scaling size (in GB)                                  | 100                      | no      |
| Storage Type                   | The storage type per node for this specific scaling size; the minimal considered type is SSD       | SSD (cheapest option as specified)     | yes      |


### Benchmark Specification

| Benchmark Parameter | Description                                                                 | Value                |
|----------------------|------------------------------------------------------------------------------|----------------------|
| Cloud                | The target cloud to run the benchmark VM                                    | same as DBMS        |
| Region               | The target cloud region to run the benchmark VM                             | same as DBMS        |
| Availability Zone    | The target availability zone to deploy the benchmark VM                     | not specified or identical to the DBMS if specified for the DBMS        |
| VM Type              | The target VM type to run the benchmark                                     | 16 Cores / 32 GB RAM |
| Benchmark Suite      | Yahoo Cloud Serving Benchmark                                               | YCSB            |
| Workload             | YCSB core workload                                           | site.ycsb.workloads.CoreWorkload                |
| Threads          | The applied number of threads for this scaling size | 200                  |
| Items            | The data items initially loaded into the DBMS | 5,000,000                   |
| Item Size (KB)           | The data size of a single item | 0.5                   |
| Read Ratio            | The ratio of read requests | 50                   |
| Insert Ratio            | The ratio of insert requests | 50                   |
| Request Distribution            | The read access pattern | zipfian                   |
| Runtime              | The runtime of the workload in minutes; workloads are always run during daytime business hours | 30                   |

## Scaling Size XLARGE 

### DBMS Specification
| DBMS Parameter | Description                                                      | Vanilla Value     | Tunable |
|-----------------------|------------------------------------------------------------------|-------------------|----------|
| DBMS Version          | The DBMS version                                     | as specified          | yes      |
| DBMS Configuration    | DBMS server configuration | provider default  | yes      |
| Cluster Size          | number of nodes for this scaling size                             | 9                 | no      |
| Replication Factor     | Replication factor per data item                                          | 3               | no      |



### Cloud Infrastructure Specification

| Cloud Infrastructure Parameter | Description                                                                                       | Vanilla Value           | Tunable |
|--------------------------------|---------------------------------------------------------------------------------------------------|--------------------------|----------|
| Region                         | The target region to deploy the DBMS instance         | Frankfurt                | yes      |
| Availability Zone              | The target availability zone(s) to deploy the DBMS instances                                     |  not specified       | yes      |
| instance type                         | The VM instance type                             | general purpose                    | yes       |
| vCores                         | The  number of vCores to be used for this specific scaling size                            | 8                        | no       |
| Memory                         | The  amount of RAM to be used for this specific scaling size (in GiB)                      | 32                       | no      |
| Storage Size                   | The storage size per node for this specific scaling size (in GB)                                  | 100                      | no      |
| Storage Type                   | The storage type per node for this specific scaling size; the minimal considered type is SSD       | SSD (cheapest option as specified)     | yes      |


### Benchmark Specification

| Benchmark Parameter | Description                                                                 | Value                |
|----------------------|------------------------------------------------------------------------------|----------------------|
| Cloud                | The target cloud to run the benchmark VM                                    | same as DBMS        |
| Region               | The target cloud region to run the benchmark VM                             | same as DBMS        |
| Availability Zone    | The target availability zone to deploy the benchmark VM                     | not specified or identical to the DBMS if specified for the DBMS        |
| VM Type              | The target VM type to run the benchmark                                     | 16 Cores / 32 GB RAM |
| Benchmark Suite      | Yahoo Cloud Serving Benchmark                                               | YCSB            |
| Workload             | YCSB core workload                                           | site.ycsb.workloads.CoreWorkload                |
| Threads          | The applied number of threads for this scaling size | 600                  |
| Items            | The data items initially loaded into the DBMS | 5,000,000                   |
| Item Size (KB)           | The data size of a single item | 0.5                   |
| Read Ratio            | The ratio of read requests | 50                   |
| Insert Ratio            | The ratio of insert requests | 50                   |
| Request Distribution            | The read access pattern | zipfian                   |
| Runtime              | The runtime of the workload in minutes; workloads are always run during daytime business hours | 30                   |
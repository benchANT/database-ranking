# OLTP DBaaS Ranking

The benchANT OLTP DBaaS Rankings enables the performance and price-performance comparison of PostgreSQL and MySQL DBaaS offers. 

The following tables show the specifications on DBMS, cloud infrastructure and benchmark level to ensure transparency, comparability and reproducibility. 

For each DBaaS, benchANT specifies a vanilla configuration as a baseline comparison and there is the option to tune specific DBMS and cloud infrastructure parameters.


## Scaling Size Small 

### PostgreSQL Specification
| PostgreSQL Parameter | Description                                                      | Vanilla Value     | Tunable |
|-----------------------|------------------------------------------------------------------|-------------------|----------|
| DBMS Version          | The major PostgreSQL version                                     | 17                | yes      |
| DBMS Configuration    | PostgreSQL configuration, can be tuned individually for the target workload | provider default  | yes      |
| Cluster Size          | The minimum cluster size to enable a high-availability (HA) setup | 2                 | yes      |
| High-Availability     | Enable high-availability                                          | yes               | yes      |
| Replication Mode      | The PostgreSQL replication mode                                  | provider default  | yes      |
| Read Replicas         | Usage of additional nodes as read replicas                       | no                | no       |
| Connection Pooling    | Usage of additional connection pooling services such as pgBouncer | no                | yes      |


### Cloud Infrastructure Specification

| Cloud Infrastructure Parameter | Description                                                                                       | Vanilla Value           | Tunable |
|--------------------------------|---------------------------------------------------------------------------------------------------|--------------------------|----------|
| Region                         | The target region to deploy the DBaaS instance, preferably Frankfurt or another EU region         | Frankfurt                | yes      |
| Availability Zone              | The target availability zone(s) to deploy the DBaaS instances                                     | provider specified        | yes      |
| vCores                         | The maximum number of vCores to be used for this specific scaling size                            | 8                        | no       |
| CPU Type                       | The CPU type to be used for this specific scaling size, e.g., Intel, Arm, Graviton, etc.          | Intel                    | yes      |
| Memory                         | The maximum amount of RAM to be used for this specific scaling size (in GiB)                      | 32                       | yes      |
| Storage Size                   | The storage size per node for this specific scaling size (in GB)                                  | 500                      | yes      |
| Storage Type                   | The storage type per node for this specific scaling size; the minimal considered type is SSD       | SSD (cheapest option)     | yes      |


### Benchmark Specification

| Benchmark Parameter | Description                                                                 | Value     |
|----------------------|------------------------------------------------------------------------------|-----------|
| Benchmark Suite      | BenchBase by CMU                                                             | BenchBase |
| Workload             | TPC-C implementation of BenchBase                                            | TPC-C     |
| ScaleFactor          | The applied scale factor to determine the number of warehouses               | 150       |
| Terminals            | The number of terminals used to execute concurrent requests                  | 75        |
| Runtime              | The runtime of the workload in minutes; workloads are always run during daytime business hours | 30        |


## Scaling Size Medium

TBD
# benchANT Database Ranking Data - DevOps Workload  

The following data sets contain the raw performance data and metadata of the [benchANT database ranking](https://benchant.com/ranking/database-ranking) for the DevOps workload created by the [Time Series Benchmark Suite (TSBS)](https://github.com/timescale/tsbs). 


Each folder contains the data of a single run benchmark, i.e. one data point of the ranking. 

***

## Data Set Structure


In order to ensure full transparency and reproducibility,  each data folder contains benchmark configuration data,  performance data, monitoring data, cloud provider metadata, VM metadata and DBMS configuration data.

In addition the `aggregation.xlsx` provides an abstracted view over all data points.  

***

### Benchmark Configuration Data

All configurable benchmark parameters are defined in the `evaluationScenario.json`.

The `benchANT_versions` contains the used versions of the benchANT software components to execute the benchmarks. 

The execution logs of the individual benchmark steps are contained in `airflowTaskInstanceDetails.json`. 

***

### Performance Data

The raw performance data output of the TSBS is contained in the `0_load.txt`  for the LOAD phase and in the `0_run.txt`for the RUN phase.  

In addition, the `runtimeDataframe.xlsx` represents a cleaned time-series of the LOAD and RUN phase performance data. 

The `validate.json` provides a validation overview of the raw benchmark results.  


***

### Monitoring Data

The DBMS cluster and the benchmark instances are monitored with [Telegraf](https://github.com/influxdata/telegraf) and the data is stored in [InfluxDB](https://github.com/influxdata/influxdb). 

A full snapshot of the monitoring data of each run is contained in the  `influx_data.zip` file.

The time frame of the RUN phase for the relevant metrics is extracted in the `dbmsMetrics.xlsx`.

*** 

### Cloud Provider Metadata

The cloud provider metadata for the DBMS deployment is contained in the `dbms_data_resources.json` / `dbms_management_resources.json` and for the benchmark deployment in the `benchmark_resources.json`. 


*** 

### VM Metadata

The VM metadata for the DBMS deployment is contained in the `dbms_data_hardware_facts.json` / `dbms_management_hardware_facts.json` and for the benchmark deployment in the `benchmark_hardware_facts.json`.  


*** 

### DBMS Metadata

For each DBMS, relevant configuration files and cluster states are stored before executing the workload. 

DBMS-specific files are contained in each folder, e.g. `postgresql.conf` for PostgreSQL DBMS deployments. 

*** 

## Benchmark Specification

The following tables show the specifications on DBMS, cloud infrastructure and benchmark level to ensure transparency, comparability and reproducibility. 

For each DBMS, benchANT specifies a vanilla configuration as a baseline comparison and there is the option to tune specific DBMS and cloud infrastructure parameters.


## Scaling Size XSMALL 

### DBMS Specification
| DBMS Deployment Parameter | Description                                                      | Vanilla Value     | Tunable |
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

| Benchmark Parameter | Description                                                                 | Value                | Tunable |
|----------------------|------------------------------------------------------------------------------|----------------------|---------|
| Cloud                | The target cloud to run the benchmark VM                                    | same as DBMS        | no      |
| Region               | The target cloud region to run the benchmark VM                             | same as DBMS        | no      |
| Availability Zone    | The target availability zone to deploy the benchmark VM                     | not specified or identical to the DBMS if specified for the DBMS        | no      |
| VM Type              | The target VM type to run the benchmark                                     | 16 Cores / 32 GB RAM | no      |
| Benchmark Suite      | Time Series Benchmark Suite (TSBS)                                          | TSBS                 | no      |
| Workload             | TSBS DevOps workload                                                        | devops               | no      |
| Threads              | The applied number of threads for this scaling size                         | 50                   | no      |
| Time Range           | The time range of the time-series data initially loaded into the DBMS       | 3 days               | no      |
| Scale                | The scale (granularity) of the time-series data                             | 1000                 | no      |
| Queries              | The number of queries to be executed                                        | 100.000              | no      |
| Batch Size           | The batch size for loading the data                                         | 1000                 | no      |
| Hash Workers         | During loading the data, whether to consistently hash insert data to the same workers (i.e., the data for a particular host always goes to the same worker) | false | yes     |


## Scaling Size SMALL 

### DBMS Specification
| DBMS Deployment Parameter | Description                                                      | Vanilla Value     | Tunable |
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

| Benchmark Parameter | Description                                                                 | Value                | Tunable |
|----------------------|------------------------------------------------------------------------------|----------------------|---------|
| Cloud                | The target cloud to run the benchmark VM                                    | same as DBMS        | no      |
| Region               | The target cloud region to run the benchmark VM                             | same as DBMS        | no      |
| Availability Zone    | The target availability zone to deploy the benchmark VM                     | not specified or identical to the DBMS if specified for the DBMS        | no      |
| VM Type              | The target VM type to run the benchmark                                     | 16 Cores / 32 GB RAM | no      |
| Benchmark Suite      | Time Series Benchmark Suite (TSBS)                                          | TSBS                 | no      |
| Workload             | TSBS DevOps workload                                                        | devops               | no      |
| Threads              | The applied number of threads for this scaling size                         | 100                   | no      |
| Time Range           | The time range of the time-series data initially loaded into the DBMS       | 3 days               | no      |
| Scale                | The scale (granularity) of the time-series data                             | 1000                 | no      |
| Queries              | The number of queries to be executed                                        | 100.000              | no      |
| Batch Size           | The batch size for loading the data                                         | 1000                 | no      |
| Hash Workers         | During loading the data, whether to consistently hash insert data to the same workers (i.e., the data for a particular host always goes to the same worker) | false | yes     |


## Contact

In case of questions or feedback on the data feel free to reach out to info@benchant.com


## Scientific References

```latex

@inproceedings{10.1145/3491086.3492473,
author = {Seybold, Daniel and Domaschka, J\"{o}rg},
title = {Benchmarking-as-a-Service for Cloud-Hosted DBMS},
year = {2021},
isbn = {9781450391542},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3491086.3492473},
doi = {10.1145/3491086.3492473},
booktitle = {Proceedings of the 22nd International Middleware Conference: Demos and Posters},
pages = {12–13},
numpages = {2},
keywords = {cloud, DBMS, performance, scalability, benchmarking-as-a-service},
location = {Virtual Event, Canada},
series = {Middleware '21}
}

@phdthesis{seybold2021automation,
  title={An automation-based approach for reproducible evaluations of distributed DBMS on elastic infrastructures},
  author={Seybold, Daniel},
  year={2021},
  school={Universit{\"a}t Ulm}
}

```
# benchANT Database Ranking Data - CRUD General Purpose  

The following data sets contain the raw performance data and metadata of the [benchANT database ranking](https://benchant.com/ranking/database-ranking) for the CRUD general purpose workload created by the [Yahoo Cloud Serving Benchmark (YCSB)](https://github.com/brianfrankcooper/YCSB). 


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

The raw performance data output of the YCSB is contained in the `0_load.txt`  for the LOAD phase and in the `0_run.txt`for the RUN phase. The database ranking data only considers the RUN phase. 

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


## Contact

In case of questions or feedback on the data feel free to reach out to info@benchant.com
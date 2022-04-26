# Database Ranking

![2022-04-25 Database Ranking - 16-9](https://user-images.githubusercontent.com/104062083/165261213-68e54222-e5a0-4a90-86b0-a81bfb417794.png)

Link: https://benchant.com/ranking/database-ranking

## Motivation

"Data is the new Oil". Data and data processing is one of the central IT topics of the 2020s. Applications in the areas of IoT, Industry 4.0, machine learning, AI, eCommerce, social media, etc. generate and process huge amounts of data.
For this reason, there are now over 600 different database management systems with a wide variety of data structures and operating modes. Each database management system has its individual specialization and suitability here. 


It is not about which database is the best or the most popular. It is about which database can provide the best performance in which scenario.

Decisions should not be made solely on the basis of popularity, features and (especially not) data structures, but above all by including reliable data on performance and scalability.

Database performance problems, inefficient solutions and over-sized computing power ("Kill it with iron!") must be a thing of the past. In the future, IT applications must be properly scaled and equipped with the best possible technology in order to be efficient and competitive.

This database ranking serves as a first orientation!
We decided to make this data publicly to rise the awareness of the performance topic, starting discussions and making better decisions in the FUTURE!

> "One accurate measurement is worth a thousand expert opinions.” - Grace M.Hopper

## Call for Participation

The future size and content of the database ranking, i.e. the number of databases and workloads available, depends heavily on the dissemination and feedback from the IT community.

- Please comment on the results.
- Please share the ranking with your colleagues.
- Please link the ranking in your posts, tweets, blog articles.
- Please reach out to database vendors and ask them to participate.

And if you are interested in actively participating and descending into the world of performance engineering, please contact us!

## Workloads
A central concept of the ranking is the focus on a wide variety of workloads that IT applications, their users or their components generate and that the database has to deal with.

In general, the following workload types are distinguished:

- CRUD: Simple READ, WRITE, UPDATE and DELETE operations
- OLTP: Transactional, complex operations of data processing
- OLAP: Analytical batch processes
- Time-Series: Time-series data with very simple, but high-frequency access patterns

In addition to the access pattern, other workload characteristics can have a major impact
- Distribution of read/write/.. operations
- Number of parallel accesses
- Access pattern and caching
- Size of the data sets
- Total number of data sets

The load is generated using publicly available benchmark suites such as the Yahoo! Cloud Serving Benchmark Suite (YCSB).
Currently, we have defined and integrated the following workloads:

- CRUD: General Purpose (at 5 different scaling sizes) based on the YCSB.

The exact specifications can be found below the ranking in detail. 

## Databases
The following DBMS and DBaaS offerings are currently (see status) included (categorized and sorted alphabetically):

**SQL**
- AWS RDS for PostgreSQL (DBaaS)
- Azure Database for PostgreSQL (DBaaS)
- Oracle MySQL (community)
- PostgreSQL (open-source)

**NoSQL**
- Apache Cassandra (open source)
- Couchbase (community)
- MongoDB (community)

**NewSQL**
- CockroachDB (community)

## Cloud
Database Performance KPIs may vary on different cloud systems. Please refer to the literature attached below. Therefore, measurements are performed on multiple cloud providers.

The following cloud providers are currently included:
- AWS EC2
- MS Azure


## How it Works
The database benchmark measurements are performed using a science-based methodology and automated benchmarking technology.

For all measurements the Benchmarking-as-a-Service platform of [benchANT](https://benchant.com) is used. This is the technical product of Dr. Daniel Seybold and Dr. Jörg Domaschka and is based on more than 7 years of scientific research, as well as 2 years of industrial use.

**Procedure of the benchmarking**

The benchmarking platform of benchANT enables automated performance and scalability benchmarks of databases on cloud resources. Hereby, automatically
1. allocates the cloud resources for the database instances
2. the databases are installed and configured
3. a separate cloud resource is allocated for workload execution
4. load phase for initial test phase
5. run phase with defined workload
6. collection of measurement results
7. testing of the measurement results
8. preparation of the measurement results
9. release of the cloud resources

This process takes 20-300 minutes depending on the size of the workload and can be performed multiple times per configuration for statistically provable results.

## Scientific Literature
The scientific basis of the benchmarking method as well as many of the statements made above are based on findings from over 7 years of research.

[Google Scholar of Dr. Daniel Seybold](https://scholar.google.de/citations?hl=de&user=n364bowAAAAJ&view_op=list_works&sortby=pubdate)

The main research results and theoretical basis can be found in the following scientific papers:

[The impact of the storage tier: A baseline performance analysis of containerized dbms (2018)](https://scholar.google.de/scholar?oi=bibs&cluster=15581908768528237384&btnI=1&hl=de)  
[Mowgli: Finding your way in the dbms jungle (2019)](https://scholar.google.de/scholar?oi=bibs&cluster=3810314013149598045&btnI=1&hl=de)  
[King Louie: DBMS Availability Evaluation Data Sets (2019)](https://scholar.google.de/scholar?oi=bibs&cluster=17998603379077962616&btnI=1&hl=de)  
[Baloo: Measuring and modeling the performance configurations of distributed DBMS (2020)](https://scholar.google.de/scholar?oi=bibs&cluster=5025312541854281019&btnI=1&hl=de)

## License
The database ranking is licensed under the international license [Creative Commons 4.0 share Attribution NonCommercial ShareAlike 4.0](http://creativecommons.org/licenses/by-nc-sa/4.0/). You are thus free to copy and redistribute ("share") or remix, transform and build upon ("adapt") the material, subject to the following conditions:
- Attribution/source attribution ("Name + Link").
- Licensing of modified data under the same license ("Link")
- Non-commercial use only

For commercial use of the data contact us please!

## Adding more ...

### ... more databases/workloads/cloud

The goal is to measure and publish as many databases and clouds as possible for different workloads.

If you want a specific DBMS or DBaaS to be integrated, please contact the database provider.

If you are a DBMS vendor or DBaaS provider, please feel free to contact us via GitHub, or via email at ranking@benchant.com.

### ... more rankings

Interested in going beyond databases? If so, get in touch via GitHub, or via email at ranking@benchant.com.

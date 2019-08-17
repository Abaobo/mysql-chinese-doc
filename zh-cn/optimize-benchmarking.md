## 8.13 测量性能 (Benchmarking)

要衡量性能, 请考虑以下因素: 

- Whether you are measuring the speed of a single operation on a quiet system, or how a set of operations (a “workload”) works over a period of time. With simple tests, you usually test how changing one aspect (a configuration setting, the set of indexes on a table, the SQL clauses in a query) affects performance. Benchmarks are typically long-running and elaborate performance tests, where the results could dictate high-level choices such as hardware and storage configuration, or how soon to upgrade to a new MySQL version. 
- For benchmarking, sometimes you must simulate a heavy database workload to get an accurate picture. 
- Performance can vary depending on so many different factors that a difference of a few percentage points might not be a decisive victory. The results might shift the opposite way when you test in a different environment. 
- Certain MySQL features help or do not help performance depending on the workload. For completeness, always test performance with those features turned on and turned off. The most important feature to try with each workload is the [adaptive hash index](https://dev.mysql.com/doc/refman/8.0/en/innodb-adaptive-hash.html) for `InnoDB` tables. 

This section progresses from simple and direct measurement techniques that a single developer can do, to more complicated ones that require additional expertise to perform and interpret the results. 
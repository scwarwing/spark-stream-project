# SF Crime Statistics with Spark Streaming

**1. How did changing values on the SparkSession property parameters affect the throughput and latency of the data?**

Changing the parameter `processedRowsPerSecond` will affect the throughout and latency of the data. If we set higher number under this parameter, the session will then process more rows in second and hence resulting in higher throughput.


**2. What were the 2-3 most efficient SparkSession property key/value pairs? Through testing multiple variations on values, how can you tell these were the most optimal?**

To find the most optimal variation we can test multiple variations and see which is providing the largest possible value for processedRowsPerSecond.

To increase processedRowsPerSecond we can modify below parameters:

`spark.default.parallelism`: total number of cores on all executor nodes.

`spark.sql.shuffle.partitions`: number of partitions to use when shuffling data for joins or aggregations.

`spark.streaming.kafka.maxRatePerPartition`: maximum rate at which data will be read from each Kafka partition.

## Profiling information

Based on the Kraken documentation to create standar kraken db:

```shell
kraken2-build --standard --threads 32 --db $DBNAME
```

Referenced EC2 image:</br> 
Memory optimized instance: **r4.8xlarge**

Ec2 instance: 

| Default vCPUs	    | Default CPU | Default CPU cores | Default threads per core  | Default threads per core  |
| :---------------- | :---------: | :---------------: | :-----------------------: | :-----------------------: | 
| 32                |  16         |  2                |   1, 2,3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16 |1,2|    


ref:  [CPU cores and threads per CPU core per instance type](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/cpu-options-supported-instances-values.html)

Based on the information above, your actual implementation could be **nearly  30 threads, not 32**


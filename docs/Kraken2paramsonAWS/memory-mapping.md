## Memory Mapping Option

After implementing several use cases we don't recommend --memory-mapping in your kraken2 parameters execution if you have other options. \
I reckon OS swapping option is better option than **--memory-mapping**  takes lots of time to process the tool.
So if you go to AWS any EC2 instances memory optimize, r5's family for instance, with RAM between 60-100 GB can work very well in AWS Batch \
and last around 4 min in a big sample read with a humble vCPU of 16 threads.

If you go to AWS EC2 instances type memory optimize, r5's family example, with RAM between 60-100 GB, it works very well in AWS Batch \
and last around 4 min working on sample read with large size and vCPU with minimal 16 threads.

| EC2 Instance | RAM                 | Time exec (min)|
| :---         | :---                | :---           |
| r5's family  | between 60 - 100 GB | 4              |

ref: [how memory-mapping work?](https://github.com/DerrickWood/kraken2/issues/120)

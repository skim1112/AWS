## Cluster Type
- instance를 하나의 low-latency group in AZ에 클러스터화 하는것
-  Pros: Great Network speed
- Cons: If the rack(하드웨어) fails, all instances fails at the same time
- Use case: need to complete fast data job, needs extremely low latency/high network throughput


## Spread Placement Groups
- 모든 EC2 instance가 in different hardware(rack)
- Pros
	- Can span across AZs
	- Reduced risk is simultaneous failure
	- EC2 instances are on different physical hardware
- Cons
	- Limited to 7 instances per AZ per placement group
- Use Case
	- Maximize high availability
	- Each instance must be isolated from failure from each other

## Partition Placement Groups
- Spreads instances across many different partitions(which rely on different sets of racks within an AZ)
	- up to 7 partitions per AZ
- Scales to 100s of EC2 instances per group
- The instances in a partition **do not share racks with the instances in the other partitions**
	- A partition failure can affect many EC2 but won't affect other partitions
	- 
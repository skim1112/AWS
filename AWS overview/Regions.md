- AWS has **Regions** all around the world
- ex) us-east-1, eu-west-3...
- A region is a cluster of data centers
- Most AWS services are **region-scoped**
	- 그 지역에만 한정해서 서비스가 진행된다는 뜻

### How to choose an AWS Region?
- Depends on where you wanna launch your service
	- Proximity to customers: reduced latency
	- **어떤 지역에서만 쓸 수 있는 서비스도 존재**

## Available Zones(AZ)
- Each Region has many AZs
	- 2,3~6 max
	- ![[Pasted image 20221230174057.png]]
- Each AZ is **one or more** **discrete data centers** with redundant power, networking and connectivity
- Each AZ is **separate from each other** -> if one is taken down, other 

### Edge Locations
- Content is delivered to end users with lower latency
- Networking has two sorts of IPs
	- IPv4
	- IPv6

## Difference Public vs Private
- Public IP
	- Public IP means the machine can be identified on the internet(WWW)
	- Must be unique across the whole web
		- 두개의 기계가 같은 public IP를 가질 수 없다
	- can be geo-located easily
- Private IP
	- the machine can only be indentified **on a private network only**
	- The IP must be unique across the private network
	- **두개의 다른 private network가 같은 IP를 가질 수 있다**
	- Machines connect to WWW using **Internet Gateway**(a proxy)

### Elastic IPs
- Public IPv4 you own as long as you don't delete it
- EC2 재시작하면, Public IP가 바뀜
- **Fixed IP**가 필요하면 **Elastic IP**가 필요
- 
### Example
- Using public IP, two different servers can communicate between WWW
- Private Network에 있는 서버/컴퓨터들은 자기들끼리 통신할 수 있다
	- public IP와 통신하고 싶으면 **Internet Gateway**(with IP)를 통해서 접속해야 한다 
- 
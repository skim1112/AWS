
- Logical component in a VPC that represents a **virtual network card**
	- virtual network card: a thing to grant access to network
- EC2의 가상의 랜카드
	- IP주소와 MAC 주소를 보유
	- ENI 하나당 Private IP + 하나의 Public IP(이건 optional)
	- 필요에 따라서 한개 이상의 Private IP 부여 가능
- EC2는 처음 생성시, 하나의 primary ENI가 연결됨
- **EC2의 서브넷 위치, 보안그룹 등 외부와 관련된 연결은 ENI 단위에서 결정**
- 

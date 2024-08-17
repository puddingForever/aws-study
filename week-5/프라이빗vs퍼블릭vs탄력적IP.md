## Private vs Public IP (IPv4)

- 네트워크는 크게 IPv4와 IPv6로 나눠질 수 있음
  - 실습에서는 IPv4만 사용
- IPv4는 37억개의 서로 다른 주소를 가질 수 있음
- IPv4 [0-255].[0-255].[0-255].[0-255]

## Private VS Public IP (IPv4) Fundamental Differences

- Public IP:
  - 기기가 인터넷상(www)에서 식별될 수 있음
  - 각각의 public IP는 전체 웹에서 유일한 주소를 가지고 있음
  - IP의 지리적 위치를 알 수 있음
- Private IP:

  - 기기가 오직 사설 네트워크 안에서만 식별될 수 있음
  - 사설 네트워크 안에서 유일한 IP여야함
    - 두 개의 다른 사설 네트워크를 가진 회사에서는 같은 private IP를 가질 수 있음
  - 기기가 사설 네트워크에 있을 떄, public IP에 접속하기 위해서는 NAT 장치와 프록시 역할을 할 인터넷 게이트웨이를 통해 연결할 수 있음
  - 지정된 범위의 IP만 사설 IP로 사용될 수 있음

  ## Elastic IP (탄력적 IP)

  - EC2 인스턴스를 시작하고 중지할 때 공용 IP를 바꿀 수 있음
  - 만약 인스턴스에 고정된 공용 IP가 필요하다면 , Elastic IP가 필요함
  - Elastic IP는 공용 IPv4이며, 삭제하지 않는 한 계속 가지고 있음
  - 한 번에 한 인스턴스에만 첨부할 수 있음
  - Elastic IP주소를 가지고 있다면, 인스턴스의 실패가 발생했을 때 빠르게 오류를 마스킹(숨기다)할 수 있음.
  - 계정 당 5개의 Elastic IP를 가질 수 있음
  - 사실 Elastic IP는 좋은 방법이 아님 .
    - 매우 좋지 않은 구조적 결정으로 언급됨
    - 대신 임의의 공용 IP를 써서 DNS 이름을 할당하는 것이 좋음
    - 로드발랜서를 사용해서 public IP를 전혀 사용하지 않아도 됨 (AWS에서 취할 수 있는 최상의 패턴)

  ## Hands on

  - 기본적으로 EC2 머신은 내부 AWS 네트워크에는 사설 IP를 사용하고 , WWW에는 public IP를 사용함
  - EC2 기기에 SSH할 때는 private IP를 사용할 수 없음(VPN을 쓰지 않는 이상 같은 네트워크에 있는 것이 아니기 떄문임)
  - 인스턴스를 멈췄다가 다시 시작하면 public IP가 변경될 수 있음

### EBS Volume

- EBS(Elastic Block Store) Volume은 인스턴스가 구동될 때 연결할 수 있는 네트워크 드라이브
- 인스턴스가 종료(termination)된 후에도, 데이터를 유지할 수 있다.
- EBS volume은 한번에 한개의 인스턴스에만 연결될수 있다(only be mounted one instance at a time), 반면에 하나의 인스턴스는 여러개의 EBS Volume을 가질 수 있음
- 특정 가용영역에서만 가능하다
- 비유(Analogy) : network USB stick
- Free tier : 30 GB of free EBS storage type of General Purpose(SSD) or Magnetic per month
- 네트워크 드라이브 (물리적인 드라이브X,참고로, volume은 한국어로 용량, 무언가를 담아두는 드라이브라는 뜻)
  - 인스턴스끼리 통신하기 위해 네트워크를 사용함 . 따라서 지연(latency)가 있을 수 있음
  - EC2 인스턴스로부터 분리될 수 있으며 다른 인스턴스로 다시 연결될 수 있음
- Locked to an Availability Zone(AZ)
  - us-east-la의 EBS Volumne은 us-east-lb로 연결이 불가능하다
  - EBS volume을 이동시키려면 , 스냅샷을 해야한다
- Have a provisioned capacity (정해진 용량)
  - you get billed for all the provioned capacity
  - you can increase the capacity of the drive over time
- Delete on Termination attribute으로 termination이 됬어도 EBS volume을 유지할 수 있음

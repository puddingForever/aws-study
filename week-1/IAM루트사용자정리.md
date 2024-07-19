# IAM:USERS & GROUPS

- Root Account
  - AWS의 모든 서비스에 관여하는 루트계정
  - 오직 계정을 생성할 때만 사용되야함
  - 탈취시 복구가 매우 어려움
  - 따라서 계정 설정을 변경하거나, 과금관리(billing)의 목적으로만 사용하기
  - 루트 사용자는 사용을 최대한 자제
- IAM ( Identity and Access Management )
  - 사용자를 생성하고 그룹에 배치시키는 서비스 (글로벌 서비스 전반적인 형태)
  - IAM으로 그룹 + 사용자를 생성
  - AWS 관리를 제외한 서비스 관리용 계정으로 사용됨
  - Global 서비스

# IAM:Permissions

- Users or Groups can be assigned JSON documents called policies
  - 유저나 그룹에게는 JSON 형식으로된 권한을 부여받음.
- Least privilege principle (최소 권한의 원칙)
  - 유저가 원하는 것 이상으로 허용하지 말기 **Don't give more permissions than a user needs**

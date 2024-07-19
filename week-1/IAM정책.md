# IAM Policies inheritance

- 유저가 그룹에 속해있든, 속해있지 않든 inline policy를 적용할 수 있음
  - 보통은 유저가 그룹에 속해있어서 해당 그룹의 권한을 전달받는 형태로 진행됨

# IAM Policies Structure

사용자마다 JSON형태로된 정책을 부여받음

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "*",
            "Resource": "*"
        }
    ]
}
```

- 구성
  - Version : policy language version 정책언어버전
  - ID : identifier for the policy (optional) 정책식별ID
  - Statement : one or more individual statements 정책관련 문장
- Statements 구성요소
  - sid : statement의 식별자 (optional)
  - Effect : 문장이 특정 API에 접근하는걸 허용하는지 안하는지
  - Principal : 특정 정책이 적용될 사용자, 계정, 혹은 역할
  - Action : Effect에 기반해 허용 및 거부되는 API 호출의 목록
    - Get* , List* 등등 문자뒤에 \*로 되어있으면 Get으로 시작하는 모든 것, List로 시작하는 모든 것을 나타냄
  - Resource : 적용될 action의 리소스 목록
  - Condition : statement가 언제 적용될지를 결정

# Multi Factor Authorization - MFA

- 루트 계정과 IAM 유저들을 해커로부터 방해하기 위한 보안장치
- AWS에서 설정해둔 비밀번호 + 보안기기를 이용하여 로그인
  - 비밀번호 + MFA(보안기기) => 로그인
- MFA를 이용하면, 계정이 해킹당해도 해커들은 로그인할 수 없음
- AWS에서 필수로 사용하라고 권장하고 있음

# 가상 MFA 장치 (Virtual MFA Device)

- Google Authenticator
- Authy
- YubiKey

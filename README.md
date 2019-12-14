# GitSetting-Tip
1. 설치
```shell
brew install git git-lfs
```
2. 설정
```shell
git config --global user.name "Your Name"
git config --global user.email "you@your-domain.com"
# 한글을 사용하기 위한 설정
git config --global core.precomposeunicode true
git config --global core.quotepath false
```
2. 저장소별 계정 설정
저장소마다 다른 계정으로 로그인 해야 할 경우 `git commit` 을 하면 기본적으로 global 에 설정된 계정 정보로 commit 이 만들어 집니다.

이럴 땐 저장소 별로 `git config --local` 명령을 주면 됩니다. 이렇게하면 --global 보다 높은 우선순위를 가지게 됩니다.

원하는 저장소로 가서 다음과 같이 명령을 입력해줍니다.
```shell
git config --local user.name "현재 저장소에서 사용할 유저네임
git config --local user.email "현재 저장소에서 사용할 email"
```
이제는 local로 지정된 사용자 계정 정보로 commit/push가 이루어 집니다. : )

잘 설정되었는지 확인은 다음의 명령어로 합니다.
```shell
git config --list
```

# Git 원격 저장소에 브랜치 푸시하고 트래킹 설정하기

이 단계의 목표는 다음과 같습니다:
*  ```/tmp/repo``` 경로에 이미 초기화된 Git 저장소가 있습니다.
*  현재 ```master``` 브랜치는 이미 ```git add```와 ```git commit``` 작업이 완료된 상태입니다.
*  이제 이 로컬 브랜치를 지정된 원격 저장소(origin) 에 푸시하고, 로컬 ```master``` 브랜치가 ```origin/master```를 추적하도록 설정해야 합니다.

과제: 
*  /tmp/repo 디렉터리로 이동하세요.
*  로컬 저장소에 원격 저장소를 origin이라는 이름으로 추가하세요.
*  원격 저장소 경로는 로컬 경로(예: file:/// 혹은 절대경로) 형식입니다.
예: 
```
git remote add origin /path/to/remote/repo
```

*  ```git push -u origin master``` 명령어를 사용하여 현재 브랜치를 원격 저장소로 푸시하고, 추적(upstream) 설정을 완료하세요.

힌트:
*  원격 저장소 경로가 올바르지 않으면 오류가 발생합니다. 정확한 경로를 확인하거나, ```file://``` 접두사를 사용하는 것도 고려하세요.
*  원격 저장소 경로 : ```/tmp/remote.git```
*  PUSH 후 다음과 같은 메시지가 출력되어야 합니다:
```
On branch master, your branch is up to date with 'origin/master'.
```

모든 작업이 완료되면 ```/challenge/check``` 명령을 실행하여 flag를 획득하세요!

# Git rebase를 사용해 선형 커밋 기록으로 브랜치 병합하기

이 단계의 목표는 다음과 같습니다:
1. ```/tmp/repo``` 경로에 이미 초기화된 Git 저장소가 있습니다.
2. 이 저장소에는 ```master```와 ```feature``` 두 브랜치가 있으며, ```feature``` 브랜치에는 중요한 기능 개발 커밋들이 존재합니다.
3. ```feature``` 브랜치를 ```master```에 병합하되, 병합 커밋(merge commit) 없이 선형(linear) 커밋 히스토리를 요구합니다.
4. 각 커밋은 개별적으로 보존되어야 하며, ```squash```하지 말아야 합니다.

과제: 
1. ```/tmp/repo``` 디렉터리로 이동하세요.
2. ```git checkout feature```로 ```feature``` 브랜치로 이동한 뒤, ```git rebase master```를 수행하세요.
3. 이렇게 하면 ```feature``` 브랜치의 커밋들이 ```master``` 커밋 이후에 재배열됩니다.
4. 이후 ```git checkout master```로 이동한 뒤, ```git merge feature```를 사용해 병합 커밋 없이 ```fast-forward``` 방식으로 병합하세요.
5. 최종적으로 ```master``` 브랜치에는 ```feature``` 브랜치의 모든 커밋이 포함되어 있어야 하며, ```merge``` 커밋이 없어야 합니다.

힌트:
1. ```git log --oneline```을 사용해 커밋 기록이 선형(linear)인지 확인하세요.
2. ```git log --merges``` 명령어로 ```merge``` 커밋이 있는지 확인할 수 있습니다. 출력이 없어야 정상입니다.
3. ```git diff master feature```로 두 브랜치 간의 변경 내용을 비교할 수 있습니다.
4. 충돌이 발생하면 수정 후 ```git rebase --continue```로 이어가세요.

모든 작업이 완료되면 ```/challenge/check``` 명령을 실행하여 flag를 획득하세요!

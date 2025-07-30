# Git rebase를 사용해 여러 커밋을 하나로 정리하기 (Squash)

이 단계의 목표는 다음과 같습니다:
1. ```/tmp/repo``` 경로에 이미 초기화된 Git 저장소가 있으며, 총 4개의 커밋이 존재합니다.
2. 이 중 첫 번째는 ```initial commit```이고, 그 뒤로 ```add part1```, ```add part2```, ```add part3``` 커밋이 이어집니다.
3. 이 중 마지막 3개의 커밋을 하나의 커밋으로 합쳐서(squash) 커밋 히스토리를 간결하고 명확하게 정리해야 합니다.

과제: 
1. ```/tmp/repo``` 디렉터리로 이동하세요.
2. ```git log --oneline```을 통해 커밋 내역을 확인하세요.
3. ```git rebase -i HEAD~3``` 명령어를 사용하여 마지막 3개의 커밋을 하나의 커밋으로 합치세요.
   * 편집기에서 첫 번째 커밋은 ```pick```으로 두고, 나머지 두 개는 ```squash``` 또는 ```s```로 표시하세요.
   * 커밋 메시지를 하나로 정리할 수도 있습니다. (예: add part1, part2, part3)
6. ```git log --oneline```으로 확인했을 때, 최종적으로 다음과 같은 두 개의 커밋만 남아 있어야 합니다:
```
<new_commit_hash> add part1, part2, part3
<initial_commit_hash> initial commit
```

힌트:
1. 커밋을 ```squash```할 때는 ```interactive rebase```를 사용해야 합니다:
```
git rebase -i HEAD~3
```
2. 커밋 메시지를 수정하라는 편집기가 열리면, 하나의 메시지로 정리하거나 그대로 두어도 됩니다.
3. ```rebase```가 실패하거나 충돌이 생기면 수정 후 ```git rebase --continue```로 진행하세요.
4. 잘못된 경우 ```git rebase --abort```으로 원상복구할 수 있습니다.

모든 작업이 완료되면 ```/challenge/check``` 명령을 실행하여 flag를 획득하세요!

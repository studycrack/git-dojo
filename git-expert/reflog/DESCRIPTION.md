# Git reflog를 사용해 reset으로 사라진 커밋 복구하기

이 단계의 목표는 다음과 같습니다:
* ```/tmp/repo``` 경로에 이미 초기화된 Git 저장소가 있습니다.
*  이전에 중요한 파일인 ```secret.txt```를 커밋한 적이 있었지만, 이후의 커밋과 ```git reset``` 명령으로 인해 해당 커밋이 사라진 것처럼 보입니다.
*  이제 ```git reflog``` 명령어를 활용해 사라진 커밋을 추적하고 복구해야 합니다.

과제: 
*  ```/tmp/repo``` 디렉터리로 이동하세요.
*  ```git log```로는 ```secret.txt``` 관련 커밋이 보이지 않을 것입니다. 대신, ```git reflog``` 명령어를 사용해 ```HEAD```의 이동 이력을 확인하세요.
*  ```git reflog```는 ```reset```, ```checkout``` 등으로 이동했던 모든 커밋 참조를 보여줍니다.
*  ```secret.txt```가 포함되어 있던 커밋을 찾으세요.
*  해당 커밋으로 이동하여 내용을 복구하세요. 아래 두 가지 방법 중 하나를 사용합니다:
   * ```git checkout <커밋해시>``` : 해당 커밋 상태로 임시 이동 (detached HEAD)
   * ```git reset --hard <커밋해시>``` : 브랜치를 해당 커밋 상태로 완전히 되돌림
*  ```secret.txt``` 파일이 복원되었는지 확인하세요.

힌트:
*  ```git reflog```는 다음과 같이 출력됩니다:
```
e1a2b34 HEAD@{1}: reset: moving to HEAD~1
9f8d7c1 HEAD@{2}: commit: add secret.txt
```
*  위에서 원하는 커밋은 ```add secret.txt``` 메시지가 있는 부분입니다.
*  복구 후 ```git log```에 해당 커밋이 다시 나타나야 합니다.
*  실수했을 경우, ```git reflog```를 활용해 언제든지 다시 돌아갈 수 있습니다.

모든 작업이 완료되면 ```/challenge/check``` 명령을 실행하여 flag를 획득하세요!

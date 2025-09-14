# action-demo
Github Action Demo

# Action cheetsheet
실행중인 github action 조회
```
gh run watch
```

종료된 github action workflow 조회
```
gh run view
```

주요 github 이벤트(아래 목록 외에도 많이 존재)
- pull_request
- push
- release
- workflow_dispatch

cli로 workflow 실행하기(`on` 필드를 `workflow_dispatch`로 설정 필요)
```
gh workflow run manual.yml -f greeting=goodbye
```

What is `actions/checkout`
- 단순히 현재 코드를 가져오는 액션. 이름 그대로 git checkout을 하는 것이다.


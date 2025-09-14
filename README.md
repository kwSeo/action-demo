# action-demo
Github Action Demo

# Action cheetsheet
**실행중인 github action 조회**
```
gh run watch
```

**종료된 github action workflow 조회**
```
gh run view
```

**주요 github 이벤트(아래 목록 외에도 많이 존재)**
- pull_request
- push
- release
- workflow_dispatch

**cli로 workflow 실행하기(`on` 필드를 `workflow_dispatch`로 설정 필요)**
```
gh workflow run manual.yml -f greeting=goodbye
```

**What is `actions/checkout`**
- 단순히 현재 코드를 가져오는 액션. 이름 그대로 git checkout을 하는 것이다.

**Github context**
`github` context는 워크플로 실행 시의 정보나 출발점이 된 이벤트 정보를 속성에 저장하고 있다.
많이 사용되는 것은 다음과 같다.
- github.run_id
- github.head_ref
- github.worksapce
- github.repository
- github.repository_owner
- github.event
  - github.event.pull_request.title

**Runner context**
`runner` 컨텍스트는 잡 실행시 의 러너 정보를 저장한다.
- runner.name
- runner.os
- runner.arch
- runner.temp
- runner.tool_cache
- runner.debug

**env**
환경변수는 워크플로, 잡, 스텝별로 지정할 수 있다.
정의 위치에 따라 환경변수 범위가 달라진다.


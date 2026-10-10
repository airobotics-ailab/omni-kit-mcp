<!-- ailab-graph-method@1 -->
# omni-kit-mcp — 그래프 검사 방법론

허브의 `graph-method@1` 투영이다. 공통 정본은 [CHU-RELUVATOR](https://github.com/airobotics-ailab/CHU-RELUVATOR/blob/main/docs/GRAPH_METHOD.md), 조직 적용 현황은 [AILAB](https://github.com/airobotics-ailab/AILAB_DASHBOARD/blob/main/GRAPH_METHOD_ROLLOUT.md)에 있다.

적용: 요청된 그래프 구조·조회 효율 검사 또는 그 도구 변경. 일반 작업의 선행 조건은 아니다.
이 저장소의 기존 AGENTS·소유 검사·권한이 우선이며, 선언의 연결은 실행 허가나 제품 시험 통과를 뜻하지 않는다.

선언은 [.ailab/graph-method.profile.json](.ailab/graph-method.profile.json)이다. 기존 소유 선언이 있으면 그것을 참조한다.
`GRAPH_METHOD_CLI`에 CHU의 `tools/graph_method.py` 위치를 지정하고 저장소 루트에서 선택 실행한다.

```sh
python3 "$GRAPH_METHOD_CLI" check-profile --root . --profile .ailab/graph-method.profile.json
python3 "$GRAPH_METHOD_CLI" query-profile --root . --profile .ailab/graph-method.profile.json --question steps
```

구조 → 원본 기준 조회 정답 → 같은 질문의 시간·출력량 비교 → 요청한 실제 모델 업무 평가 순서다.
명령은 자동 실행하지 않는다. 자료 바이트·토큰화 수치·모델의 실제 사용량을 구별하고, 미측정은 UNKNOWN으로 남긴다.
이 일괄 적용의 PASS는 방법론 연결·자료 해시·구조 검사에 한정한다. 제품별 정상/장애 시험·실물·배포·모델 평가는 별도다.
공통 생성물을 모든 저장소에 복사하지 않는다. 이 두 파일은 허브 투영이며 소유별 확장은 별도 소유 선언에서 관리한다.

# Call Prep Brief Project

영업/미팅 **콜 프렙 브리프**를 자동 생성하기 위한 Claude Code 에이전트 모음입니다.
입력값 수집 → 고객사 웹 리서치 → 고정 포맷 브리프 생성까지의 워크플로우를 구성합니다.

## 에이전트 구성 (`.claude/agents/`)

| 에이전트 | 역할 |
|----------|------|
| `call-prep-orchestrator` | 전체 워크플로우 오케스트레이션 (입력 수집 → 리서치 → 브리프 생성 순차 위임) |
| `call-prep-info-collector` | 브리프 작성에 필요한 입력값(회사명, 담당자, 미팅 목적, 제안 제품 등) 수집·검증 |
| `client-research-collector` | 고객사 정보 웹 검색 및 요약 (사업, 최근 이슈, 조직 규모, 공공기관 여부 등) |
| `call-prep-brief-generator` | 수집된 입력값과 리서치 결과를 결합해 고정 한국어 포맷 브리프 생성 |

## 사용 방법

1. VSCode에 **Claude Code 확장** 설치 후 이 폴더를 엽니다.
2. 같은 계정으로 로그인하면 `.claude/agents/`의 에이전트가 자동 로드됩니다.
3. `call-prep-orchestrator`를 호출하면 전체 흐름이 진행됩니다.

## 디렉토리 구조

```
callPrepBrief_project/
├─ .claude/
│  └─ agents/        # 프로젝트 종속 에이전트 정의
├─ docs/             # 문서화 결과물 (작업 중)
├─ .gitignore
└─ README.md
```

# dotclaude

[Claude Code](https://claude.com/claude-code) 의 `~/.claude/agents/` 디렉터리를 여러 환경 간에 동기화하기 위한 저장소입니다.

## 구성

| 파일 | 설명 |
| --- | --- |
| `ux-researcher.md` | 서비스/플랫폼의 UX를 분석하고 `docs/` 에 구조화된 마크다운 문서를 생성하는 에이전트 |

## 사용법

### 새 환경에 적용

`~/.claude/agents/` 가 비어있는 환경에서 바로 clone:

```fish
git clone git@github.com:rixile9999/dotclaude.git ~/.claude/agents
```

이미 파일이 존재한다면 백업 후 진행:

```fish
mv ~/.claude/agents ~/.claude/agents.bak
git clone git@github.com:rixile9999/dotclaude.git ~/.claude/agents
```

### 변경사항 동기화

```fish
cd ~/.claude/agents

# 원격 변경 가져오기
git pull

# 로컬 변경 올리기
git add .
git commit -m "..."
git push
```

## 에이전트 추가하기

1. `~/.claude/agents/<agent-name>.md` 작성 (frontmatter 포함)
2. `git add`, `commit`, `push`
3. 다른 환경에서 `git pull`

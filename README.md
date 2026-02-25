# kyle-claude-plugin

Claude Code용 개인 플러그인 개발용 저장소입니다.

## 구조

- `.claude-plugin/marketplace.json`: 로컬/원격 marketplace 매니페스트
- `.claude/settings.json`: GitHub marketplace 자동 인식/자동 설치 설정
- `kyle-claude-plugin/.claude-plugin/plugin.json`: 플러그인 매니페스트
- `kyle-claude-plugin/commands/`: 커스텀 slash command
- `kyle-claude-plugin/skills/`: SKILL 기반 기능

## GitHub Source로 사용하기 (권장)

Claude Code 안에서:

```text
/plugin marketplace add qazqaz1000/kyle-claude-plugin
/plugin install kyle-claude-plugin@kyle-claude-marketplace
```

설치 후 Claude Code를 재시작하고 테스트:

```text
/kyle-claude-plugin:hello-kyle Kyle
/kyle-claude-plugin:standup-note
```

## 자동 설정으로 사용하기

이 저장소의 `.claude/settings.json`에는 아래가 포함되어 있습니다.

- `extraKnownMarketplaces`: GitHub `qazqaz1000/kyle-claude-plugin` 등록
- `enabledPlugins`: `kyle-claude-plugin@kyle-claude-marketplace` 활성화

즉, 저장소를 클론한 작업 디렉터리를 신뢰(trust)하면 플러그인 인식/설치가 더 빨라집니다.

## 로컬 경로로 테스트

```bash
cd /Users/kyle/project/ai
claude
```

Claude Code 안에서:

```text
/plugin marketplace add /Users/kyle/project/ai/kyle-claude-plugin
/plugin install kyle-claude-plugin@kyle-claude-marketplace
```

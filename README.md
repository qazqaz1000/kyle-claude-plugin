# kyle-claude-plugin

Claude Code용 개인 플러그인 개발용 저장소입니다.

## 구조

- `.claude-plugin/marketplace.json`: 로컬/원격 marketplace 매니페스트
- `kyle-claude-plugin/.claude-plugin/plugin.json`: 플러그인 매니페스트
- `kyle-claude-plugin/commands/`: 커스텀 slash command
- `kyle-claude-plugin/skills/`: SKILL 기반 기능

## 로컬 테스트

```bash
cd /Users/kyle/project/ai
claude
```

Claude Code 안에서:

```text
/plugin marketplace add ./kyle-claude-plugin
/plugin install kyle-claude-plugin@kyle-claude-marketplace
```

설치 후 재시작하고 테스트:

```text
/kyle-claude-plugin:hello-kyle Kyle
/kyle-claude-plugin:standup-note
```

## Git 연결 (URL 받은 뒤)

```bash
cd /Users/kyle/project/ai/kyle-claude-plugin
git init
git add .
git commit -m "feat: bootstrap kyle Claude Code plugin"
git remote add origin <YOUR_GIT_URL>
git branch -M main
git push -u origin main
```

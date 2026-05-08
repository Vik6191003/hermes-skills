# Code Review Skill

## Trigger
User says: "review this", "check my code", "look at PR", or any code diff context

## Steps
1. Load the diff/branch: `gh pr diff <number>` or `git diff`
2. Run security scan: `trufflehog` or `semgrep` if available
3. Check for: security issues, performance problems, missing tests, style violations
4. Summarize findings in ELI5 format with severity labels (🔴 critical / 🟡 warning / 🟢 info)
5. Present as yes/no actionable items

## Output Format
```
## 🔍 Code Review: [PR Title]

### 🔴 Critical (fix before merge)
- [issue]

### 🟡 Warnings  
- [issue]

### 🟢 Notes
- [observation]

### Decision
[YES/NO — merge or fix and re-review]
```

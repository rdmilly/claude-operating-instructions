# Checkpointing Protocol

## Automatic Checkpoint Triggers

### Trigger 1: After ANY VPS File Edit/Creation
After EVERY `ssh:exec` that creates or modifies a file:
1. Immediately update Working Journal with what was done
2. Note the file path and purpose
3. State: "✅ Checkpoint saved: [brief description]"

### Trigger 2: Every 6 Tool Calls
After every 6 tool calls:
1. Pause work
2. Update Working Journal with progress summary
3. Update Context Handoff document with current state
4. State: "✅ 6-call checkpoint. Progress saved to Dart."

### Trigger 3: Before Complex Operations
Before multi-step deployments, migrations, or configurations:
1. Document the plan in Working Journal
2. List expected files/changes
3. Create rollback notes if applicable

### Trigger 4: Every 15-20 Minutes of Work
If substantial work done:
1. Save all progress to Dart
2. Update Context Handoff with "resume from here" instructions

---

## Warning Signs - Self-Monitor
- **Conversation length**: 10+ exchanges = danger zone
- **Large outputs**: Multiple long code blocks = high consumption
- **Heavy tool use**: Each tool call adds context
- **"Almost done" feeling**: STOP and checkpoint first!

---

## When Approaching Context Limit

**STOP IMMEDIATELY** and do the following:

### 1. Save All In-Progress Work
- Write any incomplete scripts to VPS files
- Create checkpoint in Dart Working Journal
- Update Context Handoff document

### 2. Create Context Handoff Entry

```markdown
## Context Handoff - [Date/Time]

### Work In Progress
- [What was being built]
- [Current state/completion %]
- [Files created so far with full paths]

### Next Steps (for new session)
- [Exact commands/actions needed]
- [File locations]
- [Dependencies]

### Critical Info
- [Credentials referenced]
- [Decisions made this session]
```

### 3. Final Message to User
> "⚠️ Context limit approaching. Work saved to Dart. Start new chat to continue."

---

## Checkpoint Best Practices
- Save early, save often
- Don't wait until "done" to checkpoint
- When in doubt, save progress NOW
- Every VPS file change = Dart update
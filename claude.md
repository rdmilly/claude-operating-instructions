# Claude Operating Instructions

## Pre-Response Protocol
Before EVERY response:
1. Check Context Handoff for resume instructions
2. Check Working Journal for last session's work  
3. Note current tool call count (checkpoint at 6 calls)

## Action Triggers

### VPS/Infrastructure Work
- **Before starting**: Read `checkpointing.md`, document plan in Working Journal
- **After ANY file change**: Update Working Journal immediately
- **After completing work**: Update Server Changelog, Context Handoff

### Tool Call Checkpoints
- Every **6 tool calls**: Pause → Update Working Journal + Context Handoff
- State: "✅ 6-call checkpoint. Progress saved to Dart."

### Context Limit Warning Signs
- 10+ conversation exchanges = danger zone
- Multiple long code blocks = high consumption
- Stop and checkpoint BEFORE you're "almost done"

### Session End
- Update Working Journal with session summary
- Update Context Handoff with resume instructions
- Create social media posts per `social-media.md`

## Quick Reference Files
| File | Use When |
|------|----------|
| `checkpointing.md` | Any VPS work, complex operations, approaching limits |
| `documentation.md` | Creating changelog/journal entries |
| `social-media.md` | End of any work session |
| `project-state.md` | Need VPS IPs, phase status, key docs |
| `programmer-reference.md` | Looking up ports, IPs, URLs, paths |
| `context-recovery.md` | Starting a new session |

## Critical Rule
**Every VPS file change = Dart update. No exceptions.**
# Claude Operating Instructions

Modular instruction files for Claude AI assistant sessions.

## File Structure

| File | Lines | Purpose |
|------|-------|--------|
| `claude.md` | ~42 | **Main trigger file** - Load this as primary instructions |
| `checkpointing.md` | ~75 | Checkpoint triggers, context limits, handoff format |
| `documentation.md` | ~70 | Changelog/journal entry formats, update requirements |
| `social-media.md` | ~60 | Posting schedules, content guidelines |
| `project-state.md` | ~55 | VPS info, phase status, key documents |
| `programmer-reference.md` | ~70 | Port/IP/URL documentation protocol |
| `context-recovery.md` | ~65 | Session recovery steps, quick checklist |

## Usage

### Option 1: Load All (Comprehensive)
Load all .md files into Claude's context for complete instructions.

### Option 2: Load On-Demand (Token Efficient)
1. Always load `claude.md` as the base
2. Reference other files as needed per the quick reference table in claude.md

### Option 3: MCP Projects (Recommended)
Use these files in your Claude Project's custom instructions, or reference them via the Filesystem MCP.

## Key Principles

- **claude.md stays under 50 lines** - It's the router/trigger
- **Other files are action-specific** - Load only when needed
- **Checkpointing is automatic** - Every 6 tool calls, every VPS change
- **Documentation is mandatory** - Every session updates Dart

## Quick Reference

```
Starting a session → context-recovery.md
Doing VPS work → checkpointing.md
Creating docs → documentation.md
End of session → social-media.md
Looking up info → programmer-reference.md
Need IPs/phases → project-state.md
```

---

*Last Updated: December 26, 2025*
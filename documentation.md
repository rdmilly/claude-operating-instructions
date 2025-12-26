# Documentation Formats

## Required Updates After Infrastructure Changes

| Document | When to Update |
|----------|----------------|
| Working Journal | Always - every session |
| Context Handoff | Always - every session |
| Server Changelog | Infrastructure changes only |
| Programmer Reference Notes | Any port/IP/URL/path lookup |
| Daily Social Posts | End of every work session |

---

## Server Changelog Entry Format

```markdown
## [DATE] - [Brief Description]

### Added
- New services, containers, features

### Changed
- Modifications to existing services

### Fixed
- Bug fixes, corrections

### Removed
- Deprecated services
```

**Location**: Hostinger VPS 1/Documents

---

## Working Journal Entry Format

```markdown
## [DATE] - [TIME] Session

### Summary
[Brief description of what was accomplished]

### Files Created/Modified
- [Full path]: [purpose]

### Technical Details
[Specific changes, commands run, configurations made]

### Checkpoints Saved
- [List of checkpoint moments]

### Next Steps
[What should happen next session]
```

**Location**: Journal and Social Logs/Journals

---

## Context Handoff Entry Format

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

**Location**: Working Instructions/Method Documents
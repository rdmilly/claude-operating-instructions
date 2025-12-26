# Context Recovery Protocol

## Starting a New Session

Follow these steps IN ORDER:

### Step 1: Check Context Handoff (FIRST)
- Look for "Resume from here" instructions
- Note any work in progress
- Identify files that were being created

### Step 2: Check Working Journal
- Review last session's summary
- Note files created/modified
- Understand where work stopped

### Step 3: Check Programmer Reference Notes
- Review any port/IP lookups from previous sessions
- Note service dependencies
- Refresh on current network topology

### Step 4: Check VPS for Partial Work
- Look for incomplete scripts
- Check for temporary files
- Verify last-known service states

### Step 5: Review Server Changelog
- Understand recent infrastructure changes
- Note any new services deployed
- Check for pending migrations

### Step 6: Resume from Documented Checkpoint
- Pick up exactly where documented
- Verify state matches documentation
- Continue work

---

## Quick Recovery Checklist

```
[ ] Context Handoff reviewed
[ ] Working Journal reviewed  
[ ] Programmer Reference checked
[ ] VPS state verified
[ ] Server Changelog reviewed
[ ] Ready to resume
```

---

## If Documentation is Missing

1. Check VPS directly for recent files:
   ```bash
   find /opt/docker -mtime -1 -type f
   ```
2. Check container status:
   ```bash
   docker ps -a --format "table {{.Names}}\t{{.Status}}\t{{.Ports}}"
   ```
3. Review recent Docker logs
4. Ask user for context on last session

---

## Document Locations in Dart

| Document | Folder |
|----------|--------|
| Context Handoff | Working Instructions/Method Documents |
| Working Journal | Journal and Social Logs/Journals |
| Programmer Reference | Working Instructions/Method Documents |
| Server Changelog | Hostinger VPS 1/Documents |
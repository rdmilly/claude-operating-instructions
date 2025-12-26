# Programmer Reference Protocol

## When to Update Programmer Reference Notes

Update immediately when you:
- Look up a port number
- Discover an IP address or URL
- Find a configuration file location
- Troubleshoot and discover actual vs expected values
- Work with networking or routing
- Reference credentials or secrets locations

---

## What to Record

### Ports
- Service name
- Internal port
- External port  
- Binding (localhost vs 0.0.0.0)

### IPs
- Server name
- Public IP
- WireGuard IP
- Purpose

### URLs
- External URL
- What it routes to
- Which service handles it

### Paths
- Configuration file locations
- Data directories
- Log locations

### Commands
- Useful debugging commands
- Health check commands
- Restart procedures

### Lookups
- Anything researched or discovered during work
- Solutions to problems encountered

---

## Best Practices

| Practice | Why It Matters |
|----------|----------------|
| Keep it current | Update immediately when things change |
| Use consistent naming | Same conventions across all docs |
| Include dependencies | Note what services rely on what |
| Document the "why" | Not just what, but why it's configured that way |
| Version history | Track when changes were made |

---

## Example Entry

```markdown
## PostgreSQL (Core Stack)
- **Internal Port**: 5432
- **External Port**: Not exposed
- **Container**: postgres-core
- **Network**: core-network
- **Data Path**: /opt/docker/core/postgres/data
- **Config**: /opt/docker/core/postgres/docker-compose.yml
- **Health Check**: `docker exec postgres-core pg_isready`
```

---

**Location**: Working Instructions/Method Documents in Dart
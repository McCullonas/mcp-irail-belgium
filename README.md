# mcp-irail-belgium

MCP server for Belgian railway queries via the [iRail API](https://docs.irail.be).
Covers SNCB/NMBS train services across Belgium.

> **Status: Work in Progress** — Server scaffolding is in place. Tools are not yet implemented.

---

## Prerequisites

- [Bun](https://bun.sh) runtime (`curl -fsSL https://bun.sh/install | bash`)
- No API keys needed — iRail is a free open data API

---

## Planned Tools

- `irail_search_stations` — Search Belgian railway stations by name
- `irail_get_liveboard` — Get departures/arrivals at a station
- `irail_get_connections` — Plan journeys between two Belgian stations
- `irail_get_vehicle` — Get real-time info about a specific train

---

## Data Source

[iRail](https://irail.be) is a Belgian open-source project providing structured access to
SNCB/NMBS timetable and real-time data. Free to use, no registration required.

---

## Install

```bash
git clone git@github.com:McCullonas/mcp-irail-belgium.git
cd mcp-irail-belgium
bun install
```

---

## MCP Client Configuration (once implemented)

```json
{
  "mcpServers": {
    "irail-belgium": {
      "command": "bun",
      "args": ["run", "/path/to/mcp-irail-belgium/src/index.ts"]
    }
  }
}
```

---

## Licence

MIT

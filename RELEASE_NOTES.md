## Statistics and census API endpoints, snapshot 15 Nov 2026

- 292,624 endpoints passed a keyless data call, tested 14–15 Nov 2026 (IST)
- 27,495 services · 247 country codes · 206,713 keyless JSON rows

### Download

- `Statistics_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz`: the full list, 292,624 rows, 12.6 MB gzipped (92.9 MB as CSV), SHA-256 `314f7d6893a4fcaae029d46acfe2e061ff84d30371a7e57930b3c38093d885f4`
- `SHA256SUMS.txt`: the checksum of that file

Check the download in the folder that holds both files:

```bash
sha256sum -c SHA256SUMS.txt          # Linux
shasum -a 256 -c SHA256SUMS.txt      # macOS
certutil -hashfile Statistics_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz SHA256   # Windows: compare with SHA256SUMS.txt
```

Then `gunzip Statistics_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz` and pass the CSV path to the examples or to `node tools/test-endpoints.mjs`. The repository itself holds a 1,000-row sample and the services list.

### What's in it for you

- 🤖 Agent tools: 28,083 · Wrap one URL pattern as a get_indicator tool: pass a country code and an indicator or table id, return the latest value with its period and unit.
- 📱 App features: 15,603 · Show one country or district on a chart or a map: OWID chart CSVs give a yearly series per country; census and demographic layers give values per tract or area.
- 🧠 Grounding and data pipelines: 84,859 · Load statistics tables on a schedule into your own store, keeping the table id and period, so answers cite a dated official figure.
- 🧪 Evals and testing: 116,536 · Run your statistics tool against a fixed set of URLs across formats (JSON-stat, OData, CSV, XML); check that period, value and unit parse, and keep last_tested as the baseline for your own re-tests.

### Changes

- First release
- Left out: 4 rows whose URL carried a credential-looking parameter or a login.
- Left out: 101 rows with an email-like address.
- Left out: 943 ArcGIS Survey123 layers (they can hold people's form answers).
- Left out: 47 class-exercise copies of the same few ArcGIS Online layers (Miami Beach sea level rise, high-risk areas without shelter, flooded areas, sea level rise and storm surge maps) across many organisations, many with a person's name in the title.
- Left out: 2 layers marked editable in the title (they can hold entries that people added).
- Left out: 106 ArcGIS layers that keep a form's default service name (they can hold people's form answers).
- Left out: 5 rows that passed a data call only from a network location in India.
- Left out: 1,033 ArcGIS class or coursework layers (lab, assignment, exam, quiz, lesson, exercise, tutorial and final-project layers, copies of class layers, layers named for a person or a person's home, and layers whose name ends in a person's name or holds a student number).
- Left out: 16 ArcGIS layers that hold reports, comments, submissions or form responses sent in by the public.
- Overlap: 1,282 of these URLs are also in 190k-weather-apis-for-agents.
- Overlap: 586 of these URLs are also in 270k-transit-apis-for-agents.
- Overlap: 172 of these URLs are also in 270k-water-apis-for-agents.
- Overlap: 34,394 of these URLs are also in 130k-finance-economy-apis-for-agents.
- Overlap: 1,995 of these URLs are also in 130k-india-apis-for-agents.
- Overlap: 82 of these URLs are also in 86k-oceans-apis-for-agents.
- Overlap: 20 of these URLs are also in 20k-air-quality-apis-for-agents.
- Overlap: 206,713 of these URLs are also in 2.5m-agent-ready-apis.
- Overlap: 2 of these URLs are also in 6.5k-wildfire-apis-for-agents.
- Overlap: 17 of these URLs are also in 24k-traffic-apis-for-agents.
- Overlap: 14 of these URLs are also in 10k-earthquake-apis-for-agents.
- Overlap: 1 of these URLs is also in 5.2k-volcano-tsunami-apis-for-agents.

On the date in last_tested (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The format column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 14–15 Nov 2026; snapshot 15 Nov 2026.

For the latest tested endpoints, search agentpopulation.com/apis. This pack is a snapshot from 15 Nov 2026.

Credit: Statistics and census API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 15 Nov 2026.

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · corrections: [@agentpopulation](https://x.com/agentpopulation) on X

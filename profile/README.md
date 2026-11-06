<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/lapilli-project/lapilli/main/assets/lapilli-lockup-dark.png">
  <img alt="Lapilli" src="https://raw.githubusercontent.com/lapilli-project/lapilli/main/assets/lapilli-lockup.png" width="260">
</picture>

**Which of your alerts are worth their page?** Lapilli replays your alert
rules against the metrics' history and judges every firing against what
actually went wrong:

- a white stone when the alert caught an incident;
- a black stone when nothing was wrong.

Count a rule's stones and you know whether it earns its place. An incident
with no stone is one your alerts missed.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/lapilli-project/lapilli/main/assets/serve-dashboard-dark.png">
  <img alt="The lapilli serve dashboard: precision, firings and incidents by week, and where the noise is" src="https://raw.githubusercontent.com/lapilli-project/lapilli/main/assets/serve-dashboard.png" width="760">
</picture>

- **`lapilli verdict`** judges one period. Use it for a week's report, or as a
  check in CI that replays a change to the rules before it is merged
  (`--compare`).
- **`lapilli serve`** keeps judging, every hour, in a ledger with a
  dashboard. Teams follow the noisy rules and the missed incidents up there,
  and an outcomes page shows what each change came to. Agents can ask it
  over MCP, and replay a change they propose.

It reads rules from Prometheus, Thanos, Mimir and VictoriaMetrics, from
Grafana alerting, and from the managed Prometheus of AWS, Azure and Google
Cloud. It only reads: it never changes a rule, an alert or a cluster.

```sh
go install lapilli.dev/cmd/lapilli@latest
```

[lapilli.dev](https://lapilli.dev) ·
[Repository](https://github.com/lapilli-project/lapilli) ·
[Releases](https://github.com/lapilli-project/lapilli/releases) ·
[Roadmap](https://github.com/lapilli-project/lapilli/blob/main/ROADMAP.md) ·
[Security](https://github.com/lapilli-project/lapilli/blob/main/SECURITY.md)

### Help build it

Lapilli has one maintainer and is looking for more, from more than one
organisation. Several areas need what the current maintainer doesn't have:

- an AWS or Azure workspace;
- Loki alerts;
- an incident tool.

[MAINTAINERS.md](https://github.com/lapilli-project/lapilli/blob/main/MAINTAINERS.md)
says how contributing in an area leads to maintaining it, and
[CONTRIBUTING.md](https://github.com/lapilli-project/lapilli/blob/main/CONTRIBUTING.md)
how to send a change.

<sub>*Lapilli* are small stones. "It was the old custom to judge with white
and black pebbles": Ovid, *Metamorphoses* XV.41.</sub>

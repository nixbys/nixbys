# Personal security, built and run in public

These repositories are the tools I use to run my own security: harden the machine, run
the program, audit what's out there, respond to incidents.

| Layer | Project | What it is |
|---|---|---|
| Harden | [linux-hardening](https://github.com/nixbys/linux-hardening) | Hardens Fedora Workstation, Atomic and Universal Blue desktops in one run. 24 sections, each undone with `--rollback`; a dry-run mode; every file it changes is backed up and every file it creates is journaled; a live protection scorecard; signed releases. Mapped to NIST CSF 2.0, SP 800-53 and MITRE ATT&CK. A weekly CI run against Fedora Rawhide catches the next release early. |
| Run and respond | [spidergraph](https://github.com/nixbys/spidergraph) | A personal security program that runs in the browser: a tiered playbook across 12 control domains, seven self-audit tools, ten incident-response runbooks and a coverage radar chart. No backend, no accounts, no tracking. Ships its own threat model. |
| Audit | [wardline](https://github.com/nixbys/wardline) | A lawful OSINT and AI research platform: hybrid search (lexical, vector, graph), live geospatial views, and governance with an append-only audit log. |

## Study

- [chiron](https://github.com/nixbys/chiron): a fork of Odysseus, a self-hosted AI
  workspace. The core is unchanged; the fork adds 22 security MCP servers for
  pentesting, OSINT and threat intelligence. Runs locally, Podman first.

## How it's tested

CI on every change, container-based test suites, and rollback and dry-run designs that
are themselves tested. Offensive-security tooling and client work are kept private;
I'm happy to walk through them in an interview.

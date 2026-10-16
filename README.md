# lagoon

A single-file floating mermaid portal for macOS: a stdlib-only daemon plus a
pywebview panel. Agents push charts to it (`printf 'graph TD\nA-->B\n' | lagoon push name`), and the live panel renders them with draggable nodes, editable
edges and labels, PNG export, split compares, and version history.

Run `lagoon panel` to start everything (daemon auto-starts; panel venv and
app bundle self-build on first use). Full agent/CLI surface: `push`, `show`,
`list`, `compare`, `unmerge`, `offsets`, `history`, `open`, plus a unix socket
and HTTP API on 127.0.0.1 — see the header docstring of `lagoon`.

State lives under `~/.local/state/lagoon/`. Linux works with GTK panels;
macOS gets a proper app bundle and NSApp-level key forwarding.

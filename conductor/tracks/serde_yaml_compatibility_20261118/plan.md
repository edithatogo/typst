# Plan — Conductor planning: evaluate maintained YAML decoder with Typst compatibility

- [ ] Freeze current Typst YAML parse/encode values, CLI/test fixtures and error spans. Inventory `serde_yaml::Error` and `Value` API coupling, MSRV/feature footprint and downstream consumers.
- [ ] Compare maintained parsers on duplicate keys, anchors/aliases, tags, nested depth, scalar dates/bools, Unicode, floats and special numbers, malformed byte/input size, encode formatting and precise `error.location()` mapping.
- [ ] If an adapter is needed, scope it to the Typst library YAML loading boundary; preserve diagnostics and public functions. Reject candidate if it materially changes semantics without versioned compatibility.
- [ ] Run supported exact-head cargo/rustfmt/clippy, Typst language, documentation, golden output and release regression matrix; submit upstream-facing decision and coordinate maintainers. Record no-go if equivalent semantics cannot be achieved.


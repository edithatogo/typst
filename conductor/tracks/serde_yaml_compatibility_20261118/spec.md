# Specification — Conductor planning: evaluate maintained YAML decoder with Typst compatibility

## Current source
- Root `Cargo.toml` lists `serde` derive, `serde_json`, `serde_yaml` and `toml`; `crates/typst-library/src/loading/yaml.rs` calls `serde_yaml::from_slice`, `serde_yaml::to_string` and maps `serde_yaml::Error::location` into public diagnostics.
- This is appropriate Serde use: the YAML codec provides format handling that Serde's generic traits do not. Any maintained replacement must preserve Typst-visible `yaml.decode`/`yaml.encode` and location-aware error behaviour.
- Review `serde-saphyr` and `yaml_serde` at pinned versions; neither is assumed API or error-semantics compatible without testing. Respect upstream release and author ownership.

## Non-goals
No parser replacement with Serde alone, no change to Typst language or macro system, no divergent undocumented fork-only behavior, no extra broad dependency, no renaming release packages. This is supplementary planning; upstream feature/release governance remains authoritative.

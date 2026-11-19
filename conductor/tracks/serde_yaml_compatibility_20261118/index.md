# Conductor planning: evaluate maintained YAML decoder with Typst compatibility

[Specification](spec.md) · [Plan](plan.md) · [Metadata](metadata.json)

Typst already uses Serde for data loading. serde_yaml is the user-facing YAML codec; compatibility and diagnostic fidelity dominate a dependency change.

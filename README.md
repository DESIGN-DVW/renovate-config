# renovate-config

Canonical Renovate preset for **public** DVWDesign repos.

This mirrors `RootDispatcher/config/renovate-base.json` (the private-repo source of
truth — RootDispatcher itself and all private repos extend it directly via
`github>DESIGN-DVW/RootDispatcher//config/renovate-base.json`).

Public repos cannot resolve a preset hosted in a private repo, so they extend this
repo instead:

```json
{
  "extends": ["github>DESIGN-DVW/renovate-config"]
}
```

**Sync policy:** `default.json` here must be kept identical in substance to
`RootDispatcher/config/renovate-base.json`. Until this is automated (see
`DISPATCH-094`), update both by hand whenever the policy changes.

See `docs/ecosystem/DEPENDENCY-GOVERNANCE.md` in RootDispatcher for the full policy.

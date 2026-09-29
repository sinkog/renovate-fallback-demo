# renovate-fallback-demo

Demo repo for [renovatebot/renovate#43916](https://github.com/renovatebot/renovate/pull/43916) (`useBaseBranchConfig=fallback`).

| Branch | `renovate.json` on branch | Expected |
| --- | --- | --- |
| `main` | default config | Dockerfile update only |
| `with-branch-config` | yes: adds a custom manager for `versions.env` + `branch-config` label | Dockerfile **and** postgres updates, labelled `branch-config` |
| `without-branch-config` | **no** (file missing → platform 404) | falls back to default config: Dockerfile update only, no error |

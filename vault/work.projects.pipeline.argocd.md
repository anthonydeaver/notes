---
id: 69a895d4-9234-4831-ba1a-992000a7d674
title: Argocd
desc: ''
updated: 1617654466452
created: 1617654391714
---

```yaml
project: default
source:
  repoURL: 'https://github.skillsoft.com/aydeaver/aioli_api'
  path: podSpecs/overlays/develop
  targetRevision: HEAD
destination:
  server: 'https://kubernetes.default.svc'
  namespace: tools
syncPolicy:
  automated:
    prune: true
    selfHeal: true
```
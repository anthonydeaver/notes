---
id: 016ceaa8-405f-49c1-92e8-91babd04b898
title: 'Sprint 125'
desc: ''
updated: 1617900639815
created: 1617728515679
---

### tasks
---

- Create
  - test each page of the wizard and ensure that 'Go Back' works as expected
  - project file?
  - delete env var
  
- Merge
  - API:
    - update deploy.yaml with DocBlock
      - generator: Aioli
      - version: x.x.x
      - hash: \<hash>
    - endpoint that receives a repo url.
      - verifies service is valid and unedited
      - pulls down repo
        - parses repo extracting editable information
          - env-vars
          - namespace
          - team
          - resources
          - subsystem
  - UI: 
    - repo url screen
      - alert if service is invalid or edited.
    - Env vars editor
    - namespace? 
    - team?
    - resources
    - subsystem
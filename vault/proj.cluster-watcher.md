---
id: ugHcAhbKVBNG3TCV2Vthn
title: Cluster Watcher
desc: ''
updated: 1635539964196
created: 1635534244821
---

## Goal
Have a service that watching the count of deployments/pods running the in the application namespaces and alerts DevOps when the value changes.
Alternate idea, have it track the names of the deployments and the number of replicas and only alert when there is a new deployment.
<!-- What are you trying to accomplish -->

## Context
<!-- Background information -->
Purpose is to alert when a new service is deployed into a cluster we might not be aware of. Also will let us know when a cutover to another env happens in case we need to do maintenance work

## Success Criteria
<!-- milestones for this project -->
- service reports on deployments/pods in the cluster on startup.
- service notifies when a new deployment appears that wasn't there before
- service notifies when the replica count for a service goes nuts

## Log
<!-- For longer projects, keep a rough log of major events-->

## Outputs
<!-- any outputs that were generated from this project. eg. slides, videos, etc-->

<!-- Everything below this line is work needed to achieve the stated goal-->

## Tasks
<!-- use this space to track current tasks. alternatively, you can also link to your daily journal note -->

## Notes
<!-- use this space for arbitrary notes -->

## Lookup
<!-- relevant prior work or resources -->

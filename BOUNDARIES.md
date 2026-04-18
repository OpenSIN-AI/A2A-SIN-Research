# A2A-SIN-Research Boundaries

## Role
`A2A-SIN-Research` owns autonomous research workflows, fleet knowledge synthesis, and research-specific contracts.

## This repo should own
- autonomous research routing, coordination, and synthesis flows
- research evidence, recovery, information retrieval, and knowledge handling
- Research contracts used by strategy and execution agents
- runbooks tied to complex information gathering and analysis

## This repo must not own
- specific social or gaming platform logic
- organization SSOT docs or architecture canon
- downstream business logic unrelated to research coordination

## Hard rules
- Keep changes scoped to autonomous research and information synthesis.
- Move non-research platform logic back to the repos that own those surfaces.
- Keep reusable contracts focused on knowledge discovery and analysis.

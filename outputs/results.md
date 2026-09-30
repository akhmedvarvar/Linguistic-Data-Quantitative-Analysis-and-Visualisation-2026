# HW1 results — Akhmed Dugrichilov

The dominant direct dependency is queen → the (71 instances across 74 occurrences), showing that the character is usually referred to with a definite title; the queen → of → hearts path occurs three times and recovers the fuller title 'Queen of Hearts'. A separate community links the relative-clause verbs examine, pass, read, and talk through dependents such as who and be, illustrating a recurrent grammatical construction rather than a coherent semantic theme.

## Network measures

- target: queen
- target_occurrences: 74
- nonspace_tokens: 34533
- wordlike_tokens: 27216
- sentences: 1521
- nodes: 30
- edges: 36
- direct_nodes: 14
- secondary_nodes: 15
- dependency_instances: 121
- directed_density: 0.041379310344827586
- layer_constrained_density: 0.16071428571428573
- weak_components: 1
- strong_components: 30
- is_dag: True
- communities: 4
- weighted_modularity: 0.3175671060719896

## Community membership

- Community 1: 1:examine, 1:pass, 1:read, 1:talk, 2:all, 2:at, 2:be, 2:have, 2:list, 2:meanwhile, 2:once, 2:rose, 2:who
- Community 2: 0:queen, 1:!, 1:", 1:,, 1:alice, 1:and, 1:furiously, 1:the, 1:’s
- Community 3: 1:child, 2:,, 2:and, 2:everybody, 2:royal, 2:the
- Community 4: 1:of, 2:hearts

Density uses distinct edges, not frequency. The graph is connected and acyclic by construction. Communities use the weighted undirected projection and should not be equated with semantic topics. See the notebook for full methods, parameter justifications, and limitations.

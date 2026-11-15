# CS453 AI Project - Cleaning Robot

**Student:** أحمد مفتاح العجيلي - 09231026
**GitHub username:** Ahmed-1001 
**Project choice:** Cleaning Robot 
**Assigned variant:** Variant: v=3, Start: S, Target: D, Removed edge: E-G

## Open the notebook

[Open in Colab](https://colab.research.google.com/github/Ahmed-1001/09231026/blob/master/project.ipynb#scrollTo=cs453-revised-13)

Private repositories require authorized access; this link does not make the project public.

## Task and scope

The agent is a cleaning robot that observes its current location and the status of the target room. It must navigate from the starting location ('S') to the requested target room ('D') and execute a 'Clean' action. 

**Scope limits:** 
1. Unit-cost actions (no physical, distance, or battery constraints).
2. The agent handles a single assigned task per run.
3. Discrete state space with no complex real-time sensory input or physical obstacles.

## Files and environment

- `project.ipynb`: agent simulator, BFS, A*, assigned mission outputs and explanations.
- `README.md`: overview and run instructions.

Python 3 / Colab CPU. The required two-week checkpoint uses only Python's standard library. 

## Run steps

1. Open `project.ipynb` in Colab using authorized GitHub access, or download it and use Colab's Upload tab.
2. No additional file uploads are required; the initial graph and state are defined in the code.
3. Restart the session and run all cells in order. Inspect the assigned mission outputs.

## Progress

| Milestone | Date | Commit link | Evidence |
|---|---|---|---|
| Setup | 2026-11-14 | [2a1fc5f](https://github.com/Ahmed-1001/09231026/commit/2a1fc5fc9a075ac3093f560834539420ed809100) | Workbook uploaded |
| Agent and simulator | 2026-11-14 | [2a1fc5f](https://github.com/Ahmed-1001/09231026/commit/2a1fc5fc9a075ac3093f560834539420ed809100) | Legal actions and task goal |
| BFS baseline | 2026-11-15 | [598a427](https://github.com/Ahmed-1001/09231026/commit/598a427dbd544258b1a04fec666459baacfd2e65) | Working uninformed search and assigned mission |
| A* search | 2026-11-15 | [598a427](https://github.com/Ahmed-1001/09231026/commit/598a427dbd544258b1a04fec666459baacfd2e65) | Working informed search and assigned mission |

The final commit link is submitted in Classroom; do not require a commit to contain a link to itself.

## Search methods

BFS is an uninformed search method that explores level-by-level, guaranteeing a minimum-move path on this unit-cost graph. A* is an informed search method using the supplied heuristic (h). The heuristic is admissible because it represents the shortest paths in the original graph; removing the edge (E-G) in our variant means the actual path can only stay the same or get longer, so h never overestimates. Both algorithms successfully found the optimal 3-step path for the assigned mission: Move to A -> Move to D -> Clean D.

## Sources and assistance

Adapted the general search algorithm structure (BFS, A*) from the course code to handle a tuple state (Location, Task_Status) and included the 'Clean' action. Used an AI assistant to verify simulator logic, debug A* errors, and structure theoretical explanations. No unresolved questions.

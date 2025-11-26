# █ G R I D . O S \_ v 5 : S Y S T E M D O C U M E N T A T I O N █
|===============================================================|
| [ SYSTEM: GRID.OS Mobile v5 ] [ STATUS: OPERATIONAL ]         |
| [ BUILD: 2025.11.25.A ] [ INTERFACE: RETRO-TACTICAL CONSOLE ] |
|===============================================================|

LOGLINE
GRID.OS v5: The retro-tactical engine for decoding cellular automata, optimizing global constraint problems, and visualizing hidden grid logic.
01. SYSTEM OVERVIEW
GRID.OS v5 is a simulation and analysis environment designed for real-time visualization of foundational computing and mathematical concepts within a unified, 9x9 cellular grid canvas. The system is compartmentalized into distinct operational modes, each addressing a core algorithm or problem type.
02. OPERATIONAL MODES
The system facilitates the execution of three primary simulation protocols. Access these via the MODES tab in the control panel, or by swiping across the main viewport.
[ MODE 1 ] SUDOKU (Constraint Solver)
Protocol: Wave Function Collapse (WFC) Approximation
Objective: Resolve a 9x9 global constraint satisfaction problem (CSP) by iteratively minimizing cell entropy.
| METRIC | FUNCTION |
|---|---|
| Entropy | Real-time count of total possible candidate placements across the grid. |
| Rays | Toggles display of currently valid candidate numbers (1-9) within a cell. |
| Heatmap | Visualizes constraint tension by coloring cells based on the volume of remaining valid candidates. |
OPERATIONAL NOTES:
 * Input is restricted to non-fixed cells.
 * The solver prioritizes processing cells with the lowest entropy count to accelerate collapse.
 * Conflict detection triggers a system warning and immediate backtrack (value removal).
[ MODE 2 ] PATHFINDING (Graph Traversal)
Protocol: A-Star (A*) Search Algorithm
Objective: Determine the optimal, shortest-distance path between a designated Start (S) node and an End (E) node in a weighted, 2D graph structure.
| VARIABLE | DEFINITION |
|---|---|
| G-Score | Cost of the path from the Start node to the current node. |
| H-Score | Heuristic estimate of the cost from the current node to the End node (Manhattan Distance used). |
| F-Score | Total estimated cost (G + H). The A* algorithm always selects the node with the lowest F-Score. |
OPERATIONAL NOTES:
 * Nodes are assumed to have uniform cost (movement weight of 1).
 * Users can introduce environmental obstacles (Walls) by dragging or tapping, which are excluded from the search space.
 * The system highlights the Visited (closed set) and Promising (open set) nodes during execution.
[ MODE 3 ] GAME OF LIFE (Cellular Automata)
Protocol: Conway's Life Ruleset
Objective: Simulate zero-player evolution based on four simple local rules, exploring emergence and complex system dynamics.
| RULE | CONDITION |
|---|---|
| Survival | An alive cell with 2 or 3 living neighbors remains alive. |
| Death | An alive cell with fewer than 2 (underpopulation) or more than 3 (overpopulation) living neighbors dies. |
| Birth | A dead cell with exactly 3 living neighbors becomes alive. |
OPERATIONAL NOTES:
 * The system executes the simulation in discrete time-steps (Cycles).
 * Users seed the initial state by dragging/tapping to activate cells.
 * The simulation halts if the total population reaches zero or if a stable/oscillating pattern is achieved (no change between steps).
03. INTERFACE AND CONTROLS
[ I/O ] Console Log (⌘)
The console can be toggled via the ⌘ interface element. It logs system events, warnings, error messages, and successful protocol completions. It is critical for monitoring solver progress.
[ INPUT ] Touch/Drag Mapping
| MODE | SINGLE TAP | DRAG ACTION |
|---|---|---|
| Sudoku | Select Cell (Activates Numpad) | No effect (Input via Numpad) |
| Path | Toggle Wall/Clear | Paint Walls / Clear Cells |
| Life | Toggle Cell State | Bulk Toggle Cell States (Spawn or Clear) |
[ EXEC ] Run Panel
This panel contains controls for algorithm execution:
 * START SIMULATION: Begins continuous execution based on the active mode protocol.
 * Single Step: Advances the active simulation protocol by one cycle.
 * Reset State: Clears all non-fixed values and solver metadata (G/H/F scores, candidates).
<!-- end list -->


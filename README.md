# VOLT — DC circuit solver

Interactive netlist-based circuit analysis with a generated topology map, branch currents, voltages and power conservation check.

Open `index.html`. Supports resistors, independent voltage sources and current sources; ground is node `0`.

## Algorithm
Modified nodal analysis: stamp resistor conductance into G, add independent voltage-source currents as unknowns, stamp current injections into the RHS, solve using Gaussian elimination with partial pivoting. Positive branch current is from the first node to the second.

## Limitations
Linear DC only; no drag-and-drop editor, nonlinear devices, transient or AC analysis. Floating or singular networks are rejected. Topology map is not a conventional schematic.

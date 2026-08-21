# Emper Labs

Building open-source technologies for scientific simulation.

---

## Projects

| Repository | Description |
|------------|-------------|
| emper-engine | Core simulation engine |
| emper-samples | Examples and tutorials |

More projects will be added as Emper Labs grows.

---

# Vision

Emper Labs aims to build reusable technologies for scientific simulation.

Our long-term goal is to provide an open ecosystem for building simulations in many domains, including:

- Biology
- Chemistrymd
- Physics
- Ecology
- Artificial Intelligence
- Cellular Automata
- Molecular Dynamics
- Fluid Simulation

The engine is designed to remain small while allowing the ecosystem to grow through reusable modules and community packages.

---

# Philosophy

> Build small. Build clean. Build reusable.

Real simulations drive the engine—not assumptions.

Features are added only after they solve real problems discovered while building simulations.

---

# Design Principles

## 1. Engine first

The engine provides infrastructure.

Applications provide algorithms.

The engine should not contain Boids, SPH, chemistry, or biology implementations unless they are reusable engine components.

---

## 2. Interfaces over implementations

The engine defines contracts.

Examples include:

- Renderer
- Spatial Partition
- Physics Solver
- Integrator

Concrete implementations may live in official modules or community packages.

---

## 3. Real algorithms before abstractions

Abstractions must emerge from experience.

If only one implementation exists, an interface is usually unnecessary.

Interfaces should appear only after multiple implementations naturally exist.

---

## 4. Modular architecture

Every subsystem should be independently reusable.

Examples:

- Rendering
- Spatial partitioning
- Physics
- Chemistry
- Biology

Users should be able to include only the modules they need.

---

## 5. Keep the core lightweight

The core engine should remain small.

Large algorithms belong in modules.

Large applications belong in samples.

---

## 6. Samples are experiments

Samples are not demonstrations only.

They are where new algorithms are developed, validated, benchmarked, and refined.

When an algorithm proves generally useful, it may become an engine module.

---

## 7. Community extensibility

Official modules are not the only solution.

Anyone should be able to develop compatible modules without modifying the engine.

Future package management will make discovering and sharing modules straightforward.

---

## 8. Performance matters

Scientific simulations often involve millions of entities.

Performance is considered from the beginning, but never at the expense of maintainability.

Correctness comes first.

Optimization follows measurement.

---

## 9. Stable public APIs

Breaking public APIs should be avoided.

Internal implementations may evolve freely while preserving public contracts whenever possible.

---

## 10. Learn from simulations

The architecture should evolve based on real scientific workloads.

Every new reusable abstraction should originate from solving an actual simulation problem.

---
## 11. Data is not policy

The engine should describe *what exists*.

Algorithms decide *what happens*.

Objects, particles, atoms, cells, and organisms are data.

Behaviors belong to algorithms and systems, not to the data itself.
---

# Ecosystem

The long-term goal is an ecosystem similar to:

```
Emper Labs

├── emper-engine
├── emper-render-sdl3
├── emper-spatial
├── emper-physics
├── emper-chemistry
├── emper-biology
├── emper-ecology
├── emper-fluid
├── emper-ai
└── community packages
```

Each project should remain focused on a single responsibility.

---

# Contributing

Contributions are welcome.

Before introducing a new abstraction, please ask:

- Does this solve a real problem?
- Can this be reused by multiple simulations?
- Does it belong in the engine or in a module?
- Does it keep the engine simpler?

Small, focused improvements are preferred over large speculative designs.

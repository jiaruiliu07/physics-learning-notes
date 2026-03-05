# physics-learning-notes

A structured, long-term repository tracking my self-study in theoretical and computational physics — from undergraduate foundations through graduate-level core subjects. It contains LaTeX notes and derivations organized by textbook, alongside C++ implementations of numerical methods and physics simulations.

This is a working document, not a finished product. I will NOT version it or do advanced project management, but I'll do my best to keep the repo clean and readable. Some chapters are thorough; others are stubs. I'm building it in public partly to keep myself honest and motivated partly because I hope it becomes useful to other students eventually.

## Who I am and why this exists

I'm an undergraduate physics major at the University of Southern California, learning methods in computational physics. I started this repository because I wanted a single place to organize my notes, track what I've actually learned (vs. what I've skimmed), and practice writing scientific code in C++ alongside the math.

The structure here reflects a simple belief: understanding a derivation and implementing it numerically are complementary skills, and doing both is better than doing either alone.

## What's in here

```
physics-learning-notes/
│
├── notes/                         # LaTeX notes, organized by subject and textbook
│   ├── shared/                    # Shared preamble, macros, minted config
│   ├── classical-mechanics/
│   │   ├── taylor/ 
│   │   ├── goldstein/             # Each book has its own main.tex
│   │   └── topic-notes/           # Standalone summaries not tied to a book
│   ├── electrodynamics/
│   │   ├── griffiths/
│   │   └── jackson/
│   ├── quantum-mechanics/
│   │   ├── griffiths-qm/
│   │   └── sakurai/
│   ├── statistical-mechanics/
│   │   ├── schroeder/
│   │   └── pathria/
│   └── mathematical-methods/
│       ├── Boas/
│       └── arfken-weber-harris/
│
├── code/                          # C++ code (and some Python)
│   ├── learning/                  # Exercises from CS106L, LearnCpp, Gottschling
│   ├── solvers/                   # Reusable numerical library (ODE, linear algebra)
│   └── projects/                  # Self-contained mini-projects with READMEs
│
├── scripts/                       # Build helpers, plotting utilities
└── docs/                          # Roadmap, reading list, changelog
```

Each textbook compiles independently — there is no monolithic build. The `shared/` directory holds a common preamble and macro file so notation stays consistent across subjects.

On the code side, `learning/` is my scratch space for language exercises (not polished, not portfolio work). `solvers/` is a growing library of numerical tools. `projects/` contains self-contained simulations that tie back to the theory notes, each with their own CMake configuration.

## Roadmap

### Phase 1 — Foundations (Summer 2026)

**Theory:** Classical mechanics at the Goldstein level (Chapters 1–6). Supplement with Taylor for intuition where needed.

**C++:** Language fundamentals via Stanford CS106L and LearnCpp.com. Goal is reading fluency and comfort writing small programs — not production-grade HPC code.

**Projects:** A few numerical mini-projects connecting the theory to code:
- Harmonic oscillator (Euler vs. RK4 comparison)
- Kepler orbit simulation
- Double pendulum / chaos visualization

### Phase 2 — Intermediate (2026–2027)

**Theory:** Electrodynamics (Griffiths → Jackson), quantum mechanics (Griffiths → early Sakurai), and mathematical methods as needed.

**C++:** Templates, generic programming, and building out the solver library. Start reading research group codebases.

**Projects:** PDE solvers (Laplace's equation, Schrödinger equation in 1D), eigenvalue problems, Monte Carlo basics.

### Phase 3 — Graduate Core (2027–2028)

**Theory:** Sakurai in full, statistical mechanics (Pathria or Kardar), and deeper Jackson.

**C++:** Performance profiling, parallelism basics (OpenMP), interfacing with established libraries (Eigen, LAPACK).

**Projects:** Ising model, molecular dynamics, tight-binding models, or other condensed matter applications depending on research direction.

These timelines are approximate. Real life — coursework, research, transfer logistics — will shift things around. The phases describe a sequence, not a schedule.

## Reading list

### Theory textbooks (in rough order of study)

| Subject | Beginner | Intermediate |
|---|---|---|
| Classical Mechanics | Taylor, *Classical Mechanics* | Goldstein, Poole & Safko, *Classical Mechanics* |
| Electrodynamics | Griffiths, *Intro to Electrodynamics* | Jackson, *Classical Electrodynamics* |
| Quantum Mechanics | Griffiths, *Intro to Quantum Mechanics* | Sakurai & Napolitano, *Modern Quantum Mechanics* |
| Statistical Mechanics | Schroeder, *Thermal Physics* | Pathria & Beale, *Statistical Mechanics* |
| Math Methods | Boas, *Mathematical Methods in the Physical Sciences* | Arfken, Weber & Harris, *Mathematical Methods for Physicists* |

### C++ and computational resources

- **CS106L** — Stanford's C++ standard library course (free materials online)
- **LearnCpp.com** — Comprehensive online reference for modern C++
- **Gottschling, *Discovering Modern C++*** — Aimed at scientists; covers templates and numerical patterns
- **Press et al., *Numerical Recipes*** — Algorithm reference (read for ideas, not for code style)

## Using this repository

You're welcome to read, reference, or adapt anything here. A few notes:

- **Notes may contain errors.** These are study notes, not textbooks. If you find a mistake, I'd genuinely appreciate an issue or pull request.
- **The textbook list is not exhaustive.** I may add references to random textbooks not on the table above (*Feynman Lectures*, Walter Greiner's texts) if I find them helpful.
- **The C++ code is learning-stage work.** Especially in `learning/` and early projects. It will get better over time. Don't use `solvers/` in anything important without checking it yourself.
- **LaTeX compilation** requires `latexmk` and a TeX distribution with `minted` support (which requires Python's `Pygments`). Each book compiles from its own directory — see the repo skeleton docs for details.
- **C++ builds** use CMake 3.20+ and a C++17-compatible compiler. Individual projects can also be compiled directly with `g++` or `clang++`.

## License

Notes and writing are released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code is released under the [MIT License](https://opensource.org/licenses/MIT).

If any of this helps you in your own studies, that's the whole point.
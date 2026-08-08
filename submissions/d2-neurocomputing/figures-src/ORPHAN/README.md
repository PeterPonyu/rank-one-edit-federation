# Orphaned expanded D2 figures

Date isolated: 2026-08-05

This directory contains expanded-panel material produced during the D2 figure campaign but not used by the current Neurocomputing manuscript. The active manuscript (`../../main.tex` and `../../main-honest-review.tex`) includes only `figA.pdf` through `figE.pdf`. No active manuscript source references the 16 PDFs listed below, and `make_figures_d2_expanded.R` was not a dependency of the active `figures-src/Makefile` build graph.

Isolated PDFs:

- `figF1A.pdf`, `figF1B.pdf`, `figF1C.pdf`, `figF1D.pdf`
- `figF2A.pdf`, `figF2B.pdf`, `figF2C.pdf`, `figF2D.pdf`
- `figF3A.pdf`, `figF3B.pdf`, `figF3C.pdf`, `figF3D.pdf`
- `figF8A.pdf`, `figF8B.pdf`, `figF8C.pdf`, `figF8D.pdf`

The archived `make_figures_d2_expanded.R` came from `figures-r/`. It is an expanded-figure scaffold with paths designed to run from the package root; it was moved here because it is not part of the active manuscript or Makefile targets. The panel-specific R generators, TikZ sources, and standalone wrappers remain one directory above so provenance and reproducibility are preserved. Explicit legacy `make figF*.pdf` targets also remain available there, while the default `make all` target now builds only the five manuscript figures.

To revive an expanded panel, first verify that its evidence and caption still match the manuscript. Then either rebuild the desired PDF from `figures-src/` using its explicit Makefile target or move the archived PDF back to `figures-src/`, add an explicit `\includegraphics` reference in the manuscript, and re-run the full compile and rendered-page QA. If the scaffold itself is needed, restore `make_figures_d2_expanded.R` to `figures-r/` before running it from the package root.

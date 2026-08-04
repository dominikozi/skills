* Do not preserve backward compatibility unless explicitly requested or required by public APIs, persisted data, deployed clients, or rolling deployments. Prefer removing obsolete code over adding compatibility layers or fallbacks. Add migrations when they are necessary to preserve or safely transform existing data.
* Choose the simplest implementation that fully meets the current requirements. Avoid speculative abstractions, configuration, and indirection.
* Grow the system in layers. Start from the smallest version that works end to end, and add each new capability on top of a product that already works. Never trade a working product for unfinished complexity.
* Keep components modular and concerns clearly separated.
* Prefer established, well-maintained libraries when they reduce overall complexity or improve reliability. Do not reimplement common functionality without a clear reason.
* Lean on the dependencies already in the project before writing your own implementation or adding packages. Do not assume a library lacks a capability without checking its documentation and types.
* Prefer simple designs that can evolve without major rewrites. Avoid known dead ends and temporary solutions that are expected to be replaced soon.
* Do not use em dashes (—).


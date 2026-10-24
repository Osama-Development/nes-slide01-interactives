# Architecture and actions

Each HTML runs an immediate function that builds authored scene templates with inline SVG. `content` stores scene IDs, names, beat counts, narrator notes and HTML constructors. `I`, `head`, `R`, `character` and `actor` build icons, headings, reveals and characters; later elements also use `RS` for bounded reveal ranges.

`sequence` flattens scene beats. `go` clamps the current index, switches scene visibility and reveal classes, updates scene/step counters, button labels, pills and live narration. `next` wraps at the end; `previous` clamps at the start. Buttons, scene pills, keydown and touch handlers dispatch navigation. `fit` scales a 1600×900 stage to the viewport; `fullscreen` uses the browser fullscreen API and `toast` reports failure. A frozen window API exposes current scene, step and totals. No network loader, persistent storage or automatic progression across files is present.

Use has 6 scenes/15 steps; Understanding has 7/19; Achievement has 8/22. They move from operating a tool, to understanding requirements, to implementing and checking outcomes. Achievement bridges toward decision making, not a captured fourth element.

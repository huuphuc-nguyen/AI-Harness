this skill is used to build up a SPECS.md


Metadata
name
specs-planner
description
Create or refine a project's root SPECS.md before vibe coding. Use when starting an app, turning an idea into actionable requirements, clarifying MVP scope, deciding frontend page count and high-level features per page, mapping user flows, or planning implementation phases. Defer detailed visual/UI/UX design and code architecture to later workflows.
SPECS Planner
Turn a raw app idea into a concise, actionable, high-level product specification at the repository root: SPECS.md. This is a planning skill, not a UI design or coding skill.

Trigger and boundaries
Use for requests such as "plan this app," "define the MVP," "what pages should we build," "write/update SPECS.md," "scope the feature set," or "plan the frontend before coding."

Deliverable: one updated or newly created root SPECS.md, following SPECS.template.md.

Do not:

Write implementation code, scaffolds, migrations, tests, or design mockups as part of this skill.
Specify final colors, typography, spacing, icons, animations, detailed component trees, Figma layouts, or pixel-level responsive behavior; a later UI/UX skill owns these.
Overdesign backend architecture, select libraries without justification, or invent database schemas/API contracts.
Introduce optional accounts, payments, dashboards, AI assistants, admin panels, or other features just because they are common.
Treat every modal, tab, or subcomponent as a separate page unless it is truly a distinct navigable screen.
Workflow
Discover project context (read-only). Read AGENTS.md, README.md, existing SPECS.md, user-provided notes, and existing routes/screens when available. If no app exists yet, work from the user's idea. Distinguish confirmed, proposed, and open requirements. Never claim to have inspected files you could not read.
Understand the job to be done. Summarize target users, main problem, desired outcome, platform (web/mobile/desktop), core use case, and relevant constraints. Ask at most a few essential questions when missing answers would drastically alter scope; otherwise make conservative, clearly marked assumptions and proceed. Prefer the smallest coherent product.
Define scope. Split capabilities into MVP (must ship), Later (not MVP), and Out of scope. Describe features as user-observable capabilities, assign stable IDs F-01, F-02, and state a short success/acceptance condition for each. Avoid vague feature names such as "user management" without an outcome.
Design the frontend information architecture — high level only. Enumerate exactly how many unique pages/screens are proposed for MVP. Give each P-01, P-02, a human-readable name, suggested route (if relevant), its purpose, major user actions/features (referencing F-IDs), and access level when relevant. Include global navigation and the key journeys. Treat a page as one distinct destination; explicitly separate page count from dialogs, panels, tabs, and empty/error states. Avoid premature visual/layout choices.
Identify necessary non-UI capabilities. Note only the data concepts, integrations, permissions, or business rules needed to deliver specified features. Stay conceptual (for example, "a session belongs to a user," not tables, fields, endpoints, or class diagrams). For multi-user or sensitive apps, call out authentication, ownership, privacy, and authorization expectations at a high level.
Plan build order. Provide a short phased implementation roadmap in dependency order: foundation, core journey, supporting features, stabilization. Each phase must name feature/page IDs and have an observable completion check. Keep the sequence lean; do not assign ungrounded time estimates or pretend the work is already done.
Validate consistency. Check every MVP feature has an interface/entry point or is explicitly marked as background capability; every MVP page has a purpose and one or more supporting feature IDs; page IDs and feature IDs are unique; page count matches rows; no later feature silently leaks into MVP; any unknowns are listed, not invented.
Write SPECS.md. If it already exists, update in place while preserving user-approved decisions; record material changes and conflicts. If none exists, populate the template. Keep the file useful for coding agents: concrete enough to implement the product incrementally, but not a detailed design document. Do not modify unrelated files.
Report. State the output path, MVP page count, core features, main assumptions/open questions, and the recommended next step: UI/UX design after scope review.
Quality bar
One-sentence product purpose understandable to a new teammate.
Explicit MVP vs later boundary, including non-goals.
Every MVP capability answers: who can do what, and what observable result?
Page count is explicit and justified, with the major responsibilities of each page.
A developer can trace Feature → Page → Build phase from the spec.
User journeys describe navigation and outcomes, not UI styling.
No contradictory claims about users, permissions, storage, or platform.
Existing project facts vs proposals vs unresolved questions remain distinguishable.
No detailed UI/UX prescription. Stop at functional structure; hand off later.
Skill ownership
SPECS.md is the source of truth for product purpose, MVP feature scope, page inventory, and high-level build order. A later UI/UX skill may produce visual and interaction specifications using SPECS.md as input; it should not silently alter MVP features or page count. If significant requirements change, revise SPECS.md first.


when finsih building the SPECs.md, refernesce it in AGETNS.md
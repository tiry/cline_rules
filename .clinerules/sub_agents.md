

## Subagent Delegation & Research Protocol

### Scope of Authority
- **Main Agent:** Holds exclusive authority for `write_to_file`, `apply_diff`, and environment modifications.
- **Subagents:** Restricted to read-only discovery. They are tools for expanding the context window without polluting the main session.

### Delegation Triggers
Utilize subagents specifically for:
- **Broad Exploration:** Mapping dependencies across large or unfamiliar directories.
- **Pattern Matching:** Running complex regex or symbol searches to identify all touchpoints for a refactor.
- **Documentation Synthesis:** Reading and summarizing external documentation or internal `README` files that aren't currently in the active context.

### Integration & Handoff
1. **Naming:** Every subagent must be named according to its specific investigative goal (e.g., `feature-gate-audit`, `schema-dependency-mapper`).
2. **Synthesis Requirement:** Upon subagent completion, the findings must be condensed into a "Research Report" within the main chat.
3. **Actionability:** The Main Agent must explicitly confirm if the research findings necessitate a change to the current technical plan before proceeding with edits.

### Negative Constraints
- Never attempt to delegate a task to a subagent that requires a terminal command with side effects (e.g., `npm install`, `git commit`).
- Do not keep raw subagent logs in the main context after the "Research Report" is generated; summarize and archive to prevent token bloat.


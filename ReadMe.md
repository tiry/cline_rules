
# 🧠 Cline Rules Repository

This repository stores **project-specific rule files** for the Cline AI coding agent. Use these to direct Cline’s behavior, maintain coding standards, document architecture decisions, and enforce team workflows.

## Repository Structure

```

my-project/
├── .clinerules/              # All rule files live here
│   ├── 01-xxx.md
│   ├── 02-xxx.md
├── .memory/                  # memory bank folder
├── README.md                 # This file

````

## What Are Cline Rules?

Cline rules (.clinerules) are system-level instructions that guide the AI in every task it performs. They persist across sessions and influence the agent’s behavior at a project level .

You can choose:
- A **single `.clinerules` file**, or
- A **`.clinerules/` directory with multiple `.md` files** for modular rule sets.

This repository selected the 2nd option - having multiples files.

## Writing Effective Rules

Tips from the documentation and community best practices:
- Be **clear, concise, and specific.**
- Focus on outcomes, not low‑level steps.
- Use **pseudo-XML or markdown** to structure rules if needed .
- Use emphasis (`**bold**`, `*italic*`) to highlight critical points.
- Enable only relevant rules to avoid noise.

## How to Configure Cline to Use These Rules

1. **Install Cline in VS Code** (via Extensions)
2. Ensure your rule files are committed to version control under `.clinerules/`
3. Cline will **automatically detect** the `.clinerules` directory in the project root and load all `.md` rules within it.
4. Optionally, use the `/newrule` slash command in the Cline chat to create new rule files in `.clinerules/` ([Cline][1], [DataCamp][3]).
5. Use the **Rules tab** in the Cline UI to toggle individual rule files on or off during a session ([DataCamp][3], [Cline][1]).

## Optional: Memory Bank Integration (Advanced)

For long-lived or complex projects, you can include a **memory bank** folder that persists project state and context across sessions.

Example structure:

```
.memory/
├── projectbrief.md
├── activeContext.md
├── systemPatterns.md
├── techContext.md
└── progress.md
```

These files help Cline retain architectural decisions, tech stack choices, and ongoing progress over time.

## Getting Started

**To begin:**

* Clone this repository.
* Ensure `.clinerules/` exists with your rule files.
* Open in VS Code and install the Cline extension.
* Set your AI provider and API key in Cline settings.
* Launch Cline and type `/newtask` to start using rules.


# OpenCode Repository Guide
## How to Investigate
### Priority Read Order:
- `README*`, root manifests, workspace config, lockfiles
- Build, test, lint, formatter, typecheck, and codegen configuration files
- CI workflows and pre-commit / task runner configurations
- Existing instruction documents (`AGENTS.md`, `CLAUDE.md`, etc.)
- Repository-specific OpenCode configuration such as `opencode.json`

### Investigation Strategy:
If the architecture remains unclear after reading these, inspect a small number of representative code files to find entry points, package boundaries, and execution flow. Prefer files that describe how the system is wired together.
Prefer executable sources over prose documentation; trust scripts or config files when they conflict with written instructions.

## Extracted Information:
- Exact developer commands, especially non-obvious ones
- Command order if required (e.g., `lint -> typecheck -> test`)
- Monorepo boundaries and ownership of directories
- Toolchain quirks: generated code, migrations, special environment loading, dev server setup
- Important constraints from existing instruction files worth preserving
- Testing peculiarities: prerequisites for integration tests, snapshot workflows

## Questioning Strategy:
Only ask users if the repository doesn't clearly specify something critical. Prefer asking in a single batch.
Questions should address undocumented conventions or missing setup instructions.
Do not duplicate information that's already clear within the repo files.

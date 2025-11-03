# Python code style
- Always put imports at the top of the file, not within methods.
- Be judicial in use of comments, matching the style of the surrounding code. Prefer description method and variable names that convey meaning over extensive code comments.
- Use simple single-line comments for section headers. Never use decorative multi-line comment blocks with repeated characters (e.g., # ====, # ----, /* *** */).

# Claude Code Configuration
- Three tiers: Global (~/.claude/CLAUDE.md), Plugin Skills, Project-Local (.claude/CLAUDE.md)
- For detailed guidance on configuration architecture, use the cross-repo-config skill

# Git Worktrees for Context-Switching
- Use git worktrees (not multiple clones) when switching between PRs/bugs frequently
- In OSS projects where .claude/ can't be committed: symlink .claude/ from main worktree to share configuration
- For automation and details, use the cross-repo-config skill

# Machine-Specific Paths
- All source code repositories are kept under `~/src/` directory
- Example: vllm is at `~/src/vllm`, llama-stack is at `~/src/llama-stack`, etc.

# Technical Accuracy and Documentation
- NEVER fabricate or guess technical syntax without verifying against official documentation first
- Always check documentation BEFORE implementing, not after the user catches errors
- If uncertain about syntax or features, explicitly state uncertainty and verify before proceeding
- Inventing syntax (like non-existent template variables) wastes time and breaks functionality

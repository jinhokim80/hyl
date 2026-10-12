# hyl

- When the user gives a YouTube URL (alone or with a request for a log/timeline/notes), run the `hyl` skill (`.claude/skills/hyl/SKILL.md`) on it end to end without asking for confirmation.
- Cloud sessions: OUTPUT_ROOT is `/home/user/hyl/output`; do not ask where to save.
- Dispatch the registered `hyl-logger` / `hyl-verifier` agents (`.claude/agents/`). If an agent type is reported unknown, stop and tell the user instead of silently falling back.
- When finished, publish the final HTML with the Artifact tool and give the user the link, then commit and push `output/` to the session branch.
- Source of truth for the skill is `skills/hyl/`; `.claude/skills/hyl/` and `.claude/agents/` are copies — keep them in sync.

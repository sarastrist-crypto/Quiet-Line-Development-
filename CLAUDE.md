# CLAUDE.md — Quiet-Line-Development-

Guidance for Claude Code working in this repo.

## 🏷 Three-word session title

**Standing operator rule (Tristian, July 31, 2026), every repo, every session.**
The first reply of a session leads with a **bolded three-word title** naming what
the session is about, before anything else. Exactly three words, restated on a
genuine pivot, never skipped. Canonical version: the `cobbled-works` CLAUDE.md.

## ⏱ Stop a watch at 3 hours — standing rule (July 28, 2026)

**Standing operator rule (Tristian), applies in EVERY repo and EVERY session
without being re-asked.** No self-scheduled watch, poll, or check-in loop runs
past **three hours**. Hourly wake-ups on something only a person can unblock are
wasted motion — the operator is not sitting there to make the call in the moment.

- **Three hours, counted from the first check-in** on that subject, not the last.
  Six 60-minute re-arms is a three-hour watch.
- **At the cap, stop and write the report:** what was being watched, why it
  stopped, the single decision or action waiting on him, what happens after, and
  the one line that restarts it.
- **Delete the pending trigger** when you stop. A stop report with a live timer
  behind it is not a stop.
- **Decision-blocked work never starts a loop at all.** If no event could move it
  without a person acting, skip the watch and deliver the report immediately.
- **Machines still get watched** — a running CI job, deploy, migration, or an
  external approval with a real SLA — but report at the three-hour mark anyway
  and pace the checks to how fast the thing actually changes.

Full procedure, report format, and the trigger cleanup:
[`/watch-stop`](.claude/skills/watch-stop/SKILL.md). Canonical statement: the
`cobbled-works` CLAUDE.md.

## 🪪 Which model is running is CHECKED, never assumed

**Standing operator rule (Tristian, September 10, 2026), every repo, every
session.** A session carries three model facts that can disagree: the model it
was **configured** with at creation, the model `session_context` says it is
**set to run**, and `last_served_model`, which served the most recent turn. A
runtime fallback moves the third alone, and Tristian can switch models himself
mid-session, so a session does not always end on the model it began with.

Never state which model is running from a line in the system prompt alone: call
`get_session` (the claude-code-remote MCP server) with `session_id` omitted and
report what it says. Never guess a marketing name out of training, which is
older than the model serving the turn. The commit footer follows the model that
actually served, so one long session can carry two different `Co-Authored-By`
lines and that is a true record rather than an inconsistency. **A model
identifier never goes into a repo beyond that footer**, not in a commit body, a
PR description, a code comment, or a page. Canonical version: the
`cobbled-works` CLAUDE.md.

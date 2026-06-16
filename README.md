# Lakeside Marina — Process Docs

Plain-markdown documentation of business processes, written to be handed to
Claude as context for building solutions with SharePoint Lists, Power Automate,
and Forms.

## Why this repo exists

Each process is documented once, in a consistent structure, so that:

- The logic is captured in version control (real diffs, not "process_v3_FINAL").
- A revision can be drafted on a branch without disturbing the live definition.
- Any `.md` file here can be pasted straight into Claude to scaffold a build.

## Structure

    lakeside-marina-docs/
    ├── README.md            ← you are here
    ├── templates/           ← blank skeletons to copy for each new process
    ├── processes/           ← the actual documented processes (one file each)
    └── reference/           ← cheat-sheets and shared notes (Mermaid, conventions)

## How to document a new process

1. Copy templates/process-doc-template.md into processes/.
2. Rename it after the process (e.g. lease-renewals.md).
3. Fill it in — Data Model, Mermaid flow, Automation logic, Business Rules.
4. Commit. When ready to build, hand the file to Claude.

## Conventions

- One process per file, lowercase-hyphenated names (job-followups.md).
- Mermaid diagrams live inline (see reference/mermaid-cheatsheet.md).
- The Business Rules and Open Questions sections are mandatory — they're
  where unstated assumptions otherwise hide.

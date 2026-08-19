# garmin-connect-skill — moved

This skill now lives inside the CLI repo it documents:

**https://github.com/cluffa/garmin-connect-cli** → `skills/garmin-connect/SKILL.md`

## Why

The skill documents the CLI's commands, flags, output shapes, and error
modes. As a separate repo, a flag rename and the doc update that describes it
could not land in the same commit — the two drifted by construction. They are
now versioned together: `SKILL.md`'s `version` frontmatter tracks
`project.version` in the CLI's `pyproject.toml`.

## Migrating

If you installed the skill from this repo, replace it with the copy in the
CLI repo:

```bash
rm -rf ~/.claude/skills/garmin-connect
git clone https://github.com/cluffa/garmin-connect-cli
ln -s "$PWD/garmin-connect-cli/skills/garmin-connect" ~/.claude/skills/garmin-connect
```

The skill's `name` (`garmin-connect`) and trigger phrases are unchanged, so
nothing that invokes it needs updating.

The full history of `SKILL.md` was merged into the CLI repo, so
`git log --follow skills/garmin-connect/SKILL.md` there shows every commit
that was made here.

## Status

Archived. No further changes will be made here — open issues and pull
requests against
[cluffa/garmin-connect-cli](https://github.com/cluffa/garmin-connect-cli).

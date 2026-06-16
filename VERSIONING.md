# Versioning

Hunter Learning OS uses simple semantic versioning.

## Current Rule

Any change that affects how the skill behaves should update the version in `SKILL.md`.

This includes:

- Changes to Router behavior
- Changes to Skill behavior
- Changes to Method behavior
- Changes to Memory behavior
- Changes to system-level interaction principles
- Changes that affect how the skill should be installed or used

Small behavior changes should usually increment the patch version:

```text
0.1.0 -> 0.1.1
```

Larger changes that add a meaningful new capability should increment the minor version:

```text
0.1.1 -> 0.2.0
```

Major architecture changes should wait until the project is stable enough to use `1.0.0`.

## Non-Behavior Changes

The version does not need to change for:

- Typo fixes
- Formatting-only edits
- Private notes that are not part of the skill
- Git or repository maintenance

## Release Note Habit

When updating the version, include a short commit message that explains the behavior change.

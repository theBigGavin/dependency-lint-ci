# dependency-lint-ci

**A Dependency Rule gate for pull requests.** If your team has multiple modules
and an architectural rule about which module may depend on which, this GitHub
Action turns that rule into a machine check on every PR: an outer module that
imports a forbidden inner module fails the check. Zero third-party dependencies.

## Why

`import-linter`, `dependency-cruiser`, and `archunit` are great layering
checkers — but they are local tools that need per-repo config, and they only
run when someone remembers to run them. `dependency-lint-ci` is a GitHub Action
first: push a one-file rule config, and every PR is gated automatically.

## Status

This repository was created on 2026-11-12 as the delivery gate for proposal
card `t_d15ca40c` (bare-run scoreboard: `stargazers_count >= 3` by
2026-11-23 23:59 CST, counted via the public GitHub REST API). The Action
implementation is landing incrementally; watch the commits.

## The rule it enforces

> Source code dependencies must point only inward, toward policy.
> — the Dependency Rule

Nothing more, nothing less. Details are details.

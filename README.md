# GitHub Actions Lab

## Workflow 1 – Dependent Jobs

This workflow demonstrates job dependencies using the `needs` keyword.

Jobs:
- build
- test (depends on build)
- deploy (depends on test)

The jobs execute sequentially:
build → test → deploy

Key Concept:
- `needs` creates job dependencies.
- `runs-on` defines the operating system environment.
- Steps represent tasks executed within a job.

---

## Workflow 2 – Multi-Platform Testing

This workflow demonstrates parallel execution across multiple operating systems.

Jobs:
- ubuntu-job
- windows-job
- macos-job

There are no dependencies between jobs, so they run simultaneously.

Key Concepts:
- Absence of `needs` results in parallel execution.
- `runs-on` specifies the OS environment.
- `actions/checkout@v4` checks out repository code.

---

## Challenges Faced

- Ensuring correct YAML indentation
- Using correct OS-specific commands
- Understanding how `needs` controls execution order

All workflows executed successfully in the Actions tab.

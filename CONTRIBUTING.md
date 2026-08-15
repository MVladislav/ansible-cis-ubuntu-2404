# Contributing

Thanks for taking the time to contribute to this role.

## Project

An Ansible role that applies the hardening recommendations of the
**CIS Ubuntu Linux 24.04 LTS Benchmark v1.0.0** to Ubuntu 24.04 hosts.

## Setup

1. Fork and clone the repository.
2. Install the dev dependencies:

   ```bash
   python3 -m pip install -r requirements.txt
   ansible-galaxy collection install -r requirements.yml
   ```

3. Install the pre-commit hooks:

   ```bash
   pre-commit install
   ```

## Testing

Run the full molecule scenario (Docker based, Ubuntu 24.04):

```bash
molecule test -s ubuntu2404
```

Run only the linters:

```bash
pre-commit run --all-files
ansible-lint
```

CI runs both on every pull request.

## Rule conventions

- One task per recommendation, named `SECTION<n> | <cis-id> | <title>`.
- Rule switches live in `defaults/main.yml` as
  `cis_ubuntu2404_rule_<section>_<id>` and must be `true`/`false`.
- Tags: `rule_<section>_<level>` plus `server_l1`, `server_l2`,
  `workstation_l1`, `workstation_l2`.
- Non-CIS additions are marked `EXTENDED` in the task name.

## Pull requests

Use the pull request template and describe:

- what the change does and which CIS recommendation(s) it affects (if any)
- how it was tested (molecule scenario, manual steps)

Keep commits small and use conventional commit messages
(`feat:`, `fix:`, `refactor:`, `chore:`, `docs:`).

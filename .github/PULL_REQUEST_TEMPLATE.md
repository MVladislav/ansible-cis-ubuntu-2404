# Description

Please include a summary of the changes and the related issue. If the change
affects a CIS recommendation, mention the recommendation ID and title.
If it is a non-CIS addition, mark it as EXTENDED.

Fixes # (issue)

## Type of change

Please delete options that are not relevant.

- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New rule (adds or changes a CIS recommendation implementation)
- [ ] EXTENDED rule (non-CIS addition)
- [ ] Documentation update
- [ ] CI / tooling change

# How Has This Been Tested?

Please describe the tests that you ran to verify your changes:

- [ ] `pre-commit run --all-files`
- [ ] `ansible-lint`
- [ ] `molecule test -s ubuntu2404` (and which scenario if not the default)

# Checklist:

- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my code
- [ ] I have made corresponding changes to the documentation
      (README coverage table, if recommendation IDs changed)
- [ ] My changes generate no new warnings

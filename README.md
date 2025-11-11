# Openlane Policy Hub

This repository contains example **organizational policies** grouped by domain — such as security, privacy, and operations — to help teams establish a strong foundation for compliance, governance, and risk management.

Each policy is written in Markdown and includes standardized frontmatter metadata so it can be easily imported, remixed, or adapted for your organization.

---

## Repository Structure

- Each folder represents a **domain** of compliance
- Each file is a single policy document

```
├── security
│   ├── access-control.md
│   ├── change-management.md
│   ├── disaster-recovery.md
│   ├── employee.md
│   ├── encryption.md
│   ├── incident-response.md
│   ├── log.md
│   ├── password.md
│   ├── risk-assessment.md
│   ├── testing.md
│   ├── vendor.md
│   └── workstation.md
├── availability
│   ├── availability.md
│   └── business-continuity.md
```

## File Structure

1. All files should be in valid markdown
1. Organization name placeholder `{{company_name}}` can be used, and when uploaded into Openlane, it will be replaced with the organization's name
1. Frontmatter should include a minimum of `title`
1. All policies should include:
    1. Purpose and Scope
    1. Background
    1. Policy Details

> [!TIP]
> Use the `template.md` as a starting place to follow the same format as other policies

## Contributing

We welcome contributions to improve or extend these examples

1. Follow the existing folder structure
1. Use valid YAML frontmatter
1. Keep filenames in kebab-case (e.g. access-control-policy.md)
1. Keep titles in `Title Case`
1. Use neutral, vendor-agnostic language
1. Submit pull requests with a short description of your changes
1. Ensure the precommit hook is installed, which will ensure formatting of yaml files, as well as wrong a spellchecker

See the [contributing](.github/CONTRIBUTING.md) guide for more information.

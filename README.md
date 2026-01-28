# Openlane Policy Hub

This repository contains template **organizational policies** to help teams establish a strong foundation for compliance, governance, and risk management.

Each policy is written in Markdown and includes standardized frontmatter metadata so it can be easily imported, remixed, or adapted for your organization.

## Instructions

**For each policy section**

* Consider if this section and its corresponding risks apply to you. If it does not, remove it and/or replace it with your organization’s corresponding practices
* Replace any text in braces e.g. `{{company_name}}` with the appropriate name, date, frequency
* Update any language in angeled brackets with language specific to your organization; each policy should have something like: [^1]:  All fields in this document marked by angled brackets \< \> and highlighted must be filled in.
* Rewrite the policy language such that it reflects the practices of your organization

**Policy completion checklist**

1. Use Find to make sure that all text in braces is replaced
1. Proofread your policy for spelling and grammar mistakes
1. Confirm that the policy’s content reflects your organizations practices
1. Add any company-specific letterhead, branding, and formatting

**More questions?**

A good rule-of-thumb is to keep your language at a high enough level such that it stays representative for at least a year. If you have more questions about how to use this template, please reach out to [support@theopenlane.io](mailto:support@theopenlane.io) or your auditor for additional guidance.

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

1. Use valid YAML frontmatter
1. Keep filenames in kebab-case (e.g. access-control-policy.md)
1. Keep titles in `Title Case`
1. Use neutral, vendor-agnostic language
1. Submit pull requests with a short description of your changes
1. Ensure the precommit hook is installed, which will ensure formatting of yaml files, as well as wrong a spellchecker

See the [contributing](.github/CONTRIBUTING.md) guide for more information.

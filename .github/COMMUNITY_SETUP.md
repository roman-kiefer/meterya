# Community setup and publication checklist

This checklist applies to the public repositories `roman-kiefer/meterya`, `roman-kiefer/meterya-api`, and `roman-kiefer/meterya-app`. Community files in a working tree do not change GitHub settings or the community profile until published on the default branch.

## 1. Code of Conduct contact

All three `CODE_OF_CONDUCT.md` files use [conduct@meterya.com](mailto:conduct@meterya.com) for confidential conduct reports. The address has been set up and the draft notices removed. Keep the mailbox monitored and update all three policies and contribution guides if the contact changes.

The Code of Conduct uses Contributor Covenant 2.1. Preserve its attribution and links.

## 2. Enable confidential vulnerability reporting

On 2026-10-24, GitHub's API confirmed that Private Vulnerability Reporting is enabled in all three repositories. The repository owner confirmed that maintainer notification settings and delivery have been verified for all three repositories. No test vulnerability reports or test emails were submitted as part of this verification.

When reviewing or restoring the configuration, an owner or repository administrator should perform these steps for each repository:

1. Open **Settings → Security and quality → Advanced Security**.
2. Find **Private vulnerability reporting** and select **Enable**.
3. Confirm that **Security → Advisories → Report a vulnerability** is available.
4. Confirm that the maintainer's GitHub notification preferences include security alerts and a monitored delivery method. Do not submit a dummy vulnerability report.

Repository settings pages:

- [Meterya](https://github.com/roman-kiefer/meterya/settings/security_analysis)
- [Meterya API](https://github.com/roman-kiefer/meterya-api/settings/security_analysis)
- [Meterya App](https://github.com/roman-kiefer/meterya-app/settings/security_analysis)

See [GitHub's configuration instructions](https://docs.github.com/en/code-security/how-tos/report-and-fix-vulnerabilities/configure-vulnerability-reporting/configure-for-a-repository).

Each SECURITY.md must describe the verified reporting configuration. Keep guidance for unavailable reporting channels and ensure links match the repository. The public issue chooser links to SECURITY.md so reporters can read the confidential reporting process before proceeding.

## 3. Review and publish

Review each repository's diff separately. Check that new files contain no credentials, personal data, configured deployment files, or backups. No application behavior or license terms need to change.

The community files and templates are published on the default branches through Meterya PR #3, Meterya API PR #3, and Meterya App PR #4. Both component issues are closed. GitHub's Community Profile API reports a health percentage of 100 for all three repositories and detects the Contributor Covenant, contribution guide, README, license, and pull request template. The legacy issue_template API field can be null for YAML issue forms and is not evidence that the forms fail to render.

The API and app security policies have been updated to reflect enabled private reporting. The parent security policy correction accompanies this checklist update. Review and publish follow-up documentation changes through a focused pull request.

## 4. Verify the default branch

On 2026-10-24, the repository owner confirmed that the rendered bug and feature forms and cross-repository routing work in Meterya and Meterya App, and that the app pull request template is inserted automatically. The parent pull request template was already marked as verified in the coordinating issue. The API component issue records completion of its published-form and pull-request-template checks. These interface checks are owner-confirmed; the follow-up documentation review used GitHub's API for the reporting settings and community profiles.

When changing the templates or reporting configuration, repeat these checks after publication:

- Open each repository's **Insights → Community standards** page and check detection of the published files.
- Open **Issues → New issue** and inspect both forms and their contact links.
- Check that a new pull request displays the template without submitting a test PR.
- Follow README, contribution, security, and accessibility links.
- Confirm the security reporting form remains available and notifications are configured.

Confirm that GitHub recognizes the Code of Conduct after publication. No labels, assignees, or account-wide default community repository are required.

# Community setup and publication checklist

This checklist applies to the public repositories `roman-kiefer/meterya`, `roman-kiefer/meterya-api`, and `roman-kiefer/meterya-app`. Community files in a working tree do not change GitHub settings or the community profile until published on the default branch.

## 1. Code of Conduct contact

All three `CODE_OF_CONDUCT.md` files use [conduct@meterya.com](mailto:conduct@meterya.com) for confidential conduct reports. The address has been set up and the draft notices removed. Keep the mailbox monitored and update all three policies and contribution guides if the contact changes.

The Code of Conduct uses Contributor Covenant 2.1. Preserve its attribution and links.

## 2. Enable confidential vulnerability reporting

On 2026-10-18, GitHub's public API reported private vulnerability reporting as disabled in all three repositories. No remote settings were changed during this preparation.

An owner or repository administrator must perform these steps for each repository:

1. Open **Settings → Security and quality → Advanced Security**.
2. Find **Private vulnerability reporting** and select **Enable**.
3. Confirm that **Security → Advisories → Report a vulnerability** is available.
4. Confirm that the maintainer's GitHub notification preferences include security alerts and a monitored delivery method. Do not submit a dummy vulnerability report.

Repository settings pages:

- [Meterya](https://github.com/roman-kiefer/meterya/settings/security_analysis)
- [Meterya API](https://github.com/roman-kiefer/meterya-api/settings/security_analysis)
- [Meterya App](https://github.com/roman-kiefer/meterya-app/settings/security_analysis)

See [GitHub's configuration instructions](https://docs.github.com/en/code-security/how-tos/report-and-fix-vulnerabilities/configure-vulnerability-reporting/configure-for-a-repository).

Only after verification, replace the "Private reporting is not enabled yet" paragraph in the relevant SECURITY.md with a statement that private reporting is enabled, and change "When enabled, use" to "Use". Keep guidance for unavailable reporting channels and ensure links match the repository. The public issue chooser links to SECURITY.md so it does not imply an unverified private form is available.

## 3. Review and publish

Review each repository's diff separately. Check that new files contain no credentials, personal data, configured deployment files, or backups. No application behavior or license terms need to change.

Commits and pushes require a separate instruction. The Code of Conduct contact is complete. Private vulnerability reporting still needs to be enabled and verified as described above before the security policies can describe it as available.

## 4. Verify the default branch

After authorized publication:

- Open each repository's **Insights → Community standards** page and check detection of the published files.
- Open **Issues → New issue** and inspect both forms and their contact links.
- Check that a new pull request displays the template without submitting a test PR.
- Follow README, contribution, security, and accessibility links.
- Confirm the security reporting form remains available and notifications are configured.

Confirm that GitHub recognizes the Code of Conduct after publication. No labels, assignees, or account-wide default community repository are required.

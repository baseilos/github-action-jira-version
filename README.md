# JIRA Version

This Github Action is a fork of [Github-Action-JIRA-FixVersion](https://github.com/levigo/github-action-jira-fixversion)

## Inputs
- `domain`: Domain name of the Jira cloud instance (e.g. your-domain.atlassian.net)
- `username`: Jira Username
- `password`: Jira Personal Access Token. Get it from [here](https://id.atlassian.com/manage-profile/security/api-tokens)
- `versionName`: The name of the Version to use (e.g. "1.0.5")
- `issueKeys`: The key(s) of the issue(s) that is to be updated. If multiple are used, separate them with a comma (e.g. "TEST-1,TEST-2")
- `versionDescription`: The description of the Version (default: "CD version")
- `versionArchived`: Mark the new version as archived (default: `false`)
- `versionReleased`: Mark the new version as released (default: `false`)
- `failOnNonExistentIssueKey`: Fail the action if a key issue does not exist (default: `false`)

## Outputs
None


## Example usage
```yaml
uses: levigo/github-action-jira-fixversion@v1.0
with:
  domain: "my-company.atlassian.net"
  username: "technical-user@company.net"
  password: "fmpUJkGhdKFvoTJclsZ03xw1"
  versionName: "1.0.5"
  versionDescription: "Continuous Delivery Version"
  issueKeys: "TEST-1"
```
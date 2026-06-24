[![StepSecurity Maintained Action](https://raw.githubusercontent.com/step-security/maintained-actions-assets/main/assets/maintained-action-banner.png)](https://docs.stepsecurity.io/actions/stepsecurity-maintained-actions)

# `step-security/arduino-setup-task`

A [GitHub Actions](https://docs.github.com/en/actions) action that makes the [Task](https://taskfile.dev/#/) task runner / build tool available to use in your workflow.

## Inputs

### `version`

The version of [Task](https://taskfile.dev/#/) to install.
Can be an exact version (e.g., `3.4.2`) or a version range (e.g., `3.x`).

**Default**: `3.x`

### `repo-token`

(**Optional**) GitHub access token used for GitHub API requests.
Heavy usage of the action can result in workflow run failures caused by rate limiting. GitHub provides a more generous allowance for Authenticated API requests.

It will be convenient to use [`${{ secrets.GITHUB_TOKEN }}`](https://docs.github.com/en/actions/reference/authentication-in-a-workflow).

## Usage

To get the action's default version of Task just add this step:

```yaml
- name: Install Task
  uses: step-security/arduino-setup-task@v2
```

If you want to pin a major or minor version you can use the `.x` wildcard:

```yaml
- name: Install Task
  uses: step-security/arduino-setup-task@v2
  with:
    version: 2.x
```

To pin the exact version:

```yaml
- name: Install Task
  uses: step-security/arduino-setup-task@v2
  with:
    version: 2.6.1
```

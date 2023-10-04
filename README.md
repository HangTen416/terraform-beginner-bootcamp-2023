# Terraform Beginner Bootcamp 2023

## Semantic Versioning

Given a version number MAJOR.MINOR.PATCH, increment the:

- MAJOR version when you make incompatible API changes
- MINOR version when you add functionality in a backward compatible manner
- PATCH version when you make backward compatible bug fixes

[Semantic Versioning](https://semver.org/)

MAJOR.MINOR.PATCH
eg. 1.0.3

[Terraform Refactoring to correct gpg keyring changes and to allow unattended install](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)


## Refactoring into Bash scripts

- The new script is considerably longer than the original so we created a bash script to make it easier to debug and install the Terraform CLI
- This provides better portability for use in future projects
- Gitpod Task File is [.gitpod.yml](.gitpod.yml)
- Shebang tells the bash script what program will interpret the script
[Shebang](https://en.wikipedia.org/wiki/Shebang_(Unix))
- ChatGPT recommends for more portable script #!/usr/bin/env bash (will search user’s PATH to search for bash executable
- For Debian/Ubuntu: #!/bin/bash will work
- If we are using a script in .gitpod.yml, we would need to point the script to a program to interpret it. eg. 'source ./bin/install_terraform_cli

## Linux chmod for changing permissions
- In order for the script to run, we had to add executable permissions for the user to the file 
- We did this by running this command: chmod u+x ./bin/install_terraform_cli
[chmod wikipedia](https://en.wikipedia.org/wiki/Chmod)

## Gitpod Workspace Lifecycle - Tasks

[Tasks-Use Before not Init](https://www.gitpod.io/docs/configure/workspaces/tasks)

## Example of getting Linux OS version

```
$ cat /etc/os-release  
PRETTY_NAME="Ubuntu 22.04.3 LTS"
NAME="Ubuntu"
VERSION_ID="22.04"
VERSION="22.04.3 LTS (Jammy Jellyfish)"
VERSION_CODENAME=jammy
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=jammy
```
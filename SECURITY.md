# Security Policy

Nvidia Rebirth is a driver package that runs with high privileges on your system, so security reports are taken seriously.

## Supported versions

Only the latest release receives fixes. If you are on an older version, update to the newest release before reporting an issue.

| Version | Supported |
|---|:---:|
| 1.2 (latest) | Yes |
| Older than 1.2 | No |

## Reporting a vulnerability

Please do not open a public issue for a security problem.

1. Use GitHub's private reporting: open the **Security** tab of this repository and choose **Report a vulnerability**.
2. If that option is not available, contact the maintainer privately through the [Discord](https://discord.gg/krpUAHkf5m) and ask for a private channel before sharing details.

Include as much of the following as you can:

- A clear description of the issue and why it matters
- The Nvidia Rebirth version, Windows version and GPU model
- Steps to reproduce, or a proof of concept
- Any logs, screenshots or file hashes that help

## What to expect

- An acknowledgement of your report, usually within a few days
- An assessment of the issue and, if it is valid, a fix in a new release
- Credit in the release notes if you want it, and silence if you prefer to stay anonymous

This is a volunteer project, so response times may vary. Please allow reasonable time for a fix before disclosing details publicly.

## Scope

In scope:

- Malicious or unexpected behavior in the installer or packaging
- Files in a release that differ from what the repository describes
- Anything that could let an attacker tamper with a release or its download

Out of scope:

- Vulnerabilities in the official Nvidia driver itself. Report those to [Nvidia's product security team](https://www.nvidia.com/en-us/security/).
- Issues that require an attacker to already have administrator access
- Performance or compatibility bugs. Use [GitHub Issues](https://github.com/rakhalfps/Nvidia-Rebirth/issues) for those.

## Staying safe

- Download releases only from the [official Releases page](https://github.com/rakhalfps/Nvidia-Rebirth/releases). Do not trust copies hosted elsewhere.
- Create a system restore point before installing.
- Be careful with anyone offering a modified build of Nvidia Rebirth, as it cannot be verified.

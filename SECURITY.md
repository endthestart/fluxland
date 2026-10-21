# Security policy

## Reporting a vulnerability

Report vulnerabilities privately through GitHub:
[Report a vulnerability](https://github.com/endthestart/fluxwl/security/advisories/new)
(the repository's Security tab). Please don't open a public issue.

Include what you found, how to reproduce it, the fluxwl version
(`fluxwl --version`), your wlroots version, and whether Xwayland is enabled.

## What to expect

- An acknowledgement within **7 days**.
- A fix, or advice on how to mitigate the problem, within **90 days**. We'll
  agree a disclosure date with you and credit you in the advisory unless you
  prefer not to be named.

## Supported versions

| Version | Security fixes |
|---|---|
| the current minor release | yes |
| the previous minor release | for 3 months after its successor ships |
| fluxland 1.1.0 and earlier (upstream) | no: report those upstream if you can |

## Scope

fluxwl runs the commands in your own config by design: `Exec` key bindings,
menu entries and the startup file. That's not a vulnerability. In scope are, for
example:

- an IPC socket that other users can reach
- a crafted style or config file that makes fluxwl run something it didn't name
- memory-safety bugs reachable from Wayland or Xwayland clients
- privilege or sandbox escapes through protocols fluxwl exposes

Vulnerabilities in wlroots itself go to wlroots.

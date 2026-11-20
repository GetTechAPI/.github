# Security policy

This policy applies to every repository in the GetTechAPI organisation.

## Reporting a vulnerability

Report it privately, not in a public issue or pull request:

1. Open the repository the problem is in.
2. Go to **Security** → **Report a vulnerability**.
3. Describe what you found, how to reproduce it and what it affects.

Private vulnerability reporting is enabled in all six repositories. If you are
not sure which repository is affected, report it in
[TechAPI](https://github.com/GetTechAPI/TechAPI/security/advisories/new).

## What to report

- A workflow that can be made to run untrusted code, leak a secret or write
  where it should not.
- A way to make the published site or API serve content that is not in the
  repository.
- A problem in the engine's API, collectors or validators that can be
  exploited.

A wrong value in a data record is not a security problem. Open a normal issue
for it with [TechAPI's issue forms](https://github.com/GetTechAPI/TechAPI/issues/new/choose).

## What to expect

The organisation has one maintainer. Reports are read as they come in; you get
a reply in the advisory thread, and a fix is credited to you there unless you
ask otherwise.

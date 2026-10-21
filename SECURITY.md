# Security Policy

## Reporting a vulnerability

Email [security@keepass-web.app](mailto:security@keepass-web.app). Please don't
report a vulnerability in a public issue, discussion, or pull request: until a
fix ships, a public report shows attackers the way in before anyone can update.

Include as much of this as you can:

- the page or package affected, and the version shown in that page's footer
- steps to reproduce, or a proof of concept
- what an attacker could read, change, or take

## Supported versions

Security fixes ship to everyone in a new release on the
[releases page][releases]. [keepass-web.app][kpo] begins serving each release
once a maintainer has reviewed its deployment. If you run a downloaded copy,
replace it with the latest release.

| KeePass Web release | Supported |
| ------------------- | --------- |
| Latest              | ✅        |
| Earlier             | ❌        |

## Scope

This policy covers every repository in the [keepass-web organization][org] and
the pages served at [keepass-web.app][kpo]. Report a flaw in a service KeePass
Web relies on, such as Google's sign-in or GitHub itself, to that company.

[kpo]:https://keepass-web.app
[releases]:https://github.com/keepass-web/source-application/releases
[org]:https://github.com/keepass-web

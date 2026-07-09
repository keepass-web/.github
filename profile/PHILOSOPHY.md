# Design and Development Philosophy

We believe that software handling other people's secrets must be minimally
complex, impeccably maintained, obviously trustworthy, and vetted by
unaffiliated third parties.

## Core Principles

Minimalism is the deliberate choice to keep the codebase as small, simple, and
self-contained as possible, so we:
* Ship our software as self-contained, single-page HTML distributables, one per
  job. No install, no server, and no build step required to use them.
* Maintain our own KDBX parser rather than importing a third-party library, so
  we control when security fixes ship and are not blocked by an external
  maintainer.
* Use only vanilla HTML5 and CSS; no Javascript or CSS frameworks.
* Require only the WebCrypto Browser API, which is supported in the evergreen
  version of all modern browsers.
* Build the codebase to be understandable by a literate technical user in a
  single sitting.

Impeccability refers to the state of being "without mistakes or faults"[^1] and
manifests itself in KeePass Web through:
* 100% test coverage. With modern AI-assisted development, there is no excuse
  for leaving code untested.
* Enforced code style through automated linting and formatting. No exceptions, no
  overrides, no "we'll fix it later."
* Documentation that is easy to use, understand, and find[^2].
* No verified issues older than 90 days across the Keepass Web organization.

Trustworthiness is the "firm belief in the integrity, ability, or character of a
person or thing."[^3] What does that mean for KeePass Web? It means there's a
vibrant community of users who can vouch for it. It means the code is open and
available for inspection. It means the authors are responsive to good faith
questions.

To be vetted means "to be critically reviewed and evaluated"[^4]. For KeePass
Web, this means having the software application gleefully subjected to hackers
and security researchers: those hunters who have a financial interest in finding
security faults in the architecture or implementation of KeePass Web.

To understand how we fund security audits and bounty payouts, review our
[licensing model](/profile/LICENSING.md).

[^1]:https://dictionary.cambridge.org/dictionary/english/impeccable
[^2]:https://www.oreilly.com/library/view/developing-quality-technical/9780133119046/
[^3]:https://www.wordnik.com/words/trust
[^4]:https://www.merriam-webster.com/dictionary/vetted

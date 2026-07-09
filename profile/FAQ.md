# Frequently Asked Questions

## General

### What is KeePass Web?

KeePass Web is a password manager that runs entirely in your web browser. It
reads and writes [KDBX][kdbx] database files — the same format used by KeePass,
KeePassXC, Strongbox, KeePassium, and others. It is a multi-page application (MPA): self-contained HTML pages, each doing one
job, with no external dependencies.

### What is the current project status?

KeePass Web is under active development. As of June 2026, the infrastructure is
in place — the domain, GitHub Pages, sponsorship tiers, and organization
documentation — but no application has been released yet. We expect to publish
the first release — a multi-page application with full KDBX read and write support
and connectors to your own cloud storage provider — by mid-September 2026,
published on the [GitHub releases page][releases] and served identically at
[keepass-web.app][kpo]. Follow development at [github.com/keepass-web][ghorg].

### What is a KDBX file?

KDBX is an open, well-documented file format for storing passwords and secrets.
It uses strong encryption and tamper-evident protections. Because it is an open
format, many independent applications can read and write it. Your passwords are
not locked to any single vendor — including us.

### What browsers are supported?

Any modern desktop browser that supports [WebCrypto][webcrypto]: Chrome, Firefox,
Safari, Edge, and terminal browsers such as Browsh and Carbonyl. WebCrypto is the
only browser API KeePass Web requires.

### How do I know it's safe?

You don't have to take our word for it. Each page of KeePass Web is a single,
un-minified HTML file. Open the one you are about to use in a text editor before
you open your database.
Watch the browser network tab while it runs — you will see no outbound network
requests. The source code is published on GitHub and the application is
periodically subjected to independent security research through a funded bug
bounty program.

### Why did you write your own KDBX parser instead of using an existing library?

Security software that depends on third-party libraries inherits that library's
security fix schedule. If a vulnerability is discovered in a dependency, we are
blocked on someone else's availability and priorities to ship a fix. By owning
the parser ourselves, we control when fixes ship.

### Why no JavaScript or CSS frameworks?

Every dependency is an attack surface and code you cannot fully audit. We keep
the codebase small enough that a technically literate user can read all of it.
Frameworks make that impractical.

### How do I get in touch?

For questions and feedback, [start a GitHub Discussion][discussions]. For bugs,
[open an issue][issues]. For security vulnerabilities, email
[security@keepass-web.app](mailto:security@keepass-web.app) — please do not open
a public issue for security reports.

### How does GitHub Sponsorship work?

Visit [github.com/sponsors/keepass-web][ghs] and choose a tier. Sponsorship funds
collaborator time and security audits — it does not unlock anything, because
nothing is gated. The whole application — cloud connectors included — is open to
everyone, whether you download it or open [keepass-web.app][kpo]; sponsors simply
keep the work going.

---

## Cloud storage connectors

A cloud connector opens your KDBX database straight from your own cloud storage —
Google Drive, with more providers over time — instead of from a file sitting on
the machine in front of you. You sign in to your provider, choose your database,
and it opens in the browser; your edits are written straight back to the provider.
The database itself never lands on the local disk.

There are two reasons you might want that. On a machine you don't control — a
library terminal, a kiosk, a borrowed laptop — nothing is left behind afterwards,
because your vault was never on the disk to begin with. And even on a machine you
trust, keeping the authoritative copy in your cloud storage means there is no
second copy to manage: no download-edit-reupload cycle, no stale or forked local
files, and no unsaved local edits to lose if the machine crashes. Your vault stays
in one place, reachable from any browser.

### Which cloud storage providers are supported?

Google Drive at the first release. Dropbox, OneDrive, and WebDAV (Nextcloud,
ownCloud, and similar) are planned for later releases as demand warrants.

### Do I need to sponsor to connect my cloud storage?

No. The connectors are open to everyone. The application is MIT-licensed and its
source is public, and it connects to your own provider with your own sign-in — no
sponsorship required, and no storage of ours involved. We ask for support because
the work has real costs, not because we withhold anything. The project runs on
the trust that people who find the software valuable will help fund it.

### Can I use a cloud connector when running the pages from a download?

Yes. Two things are independent: where the pages run, and where your database
lives. You can run the pages from a download or from keepass-web.app, and with
either you can open a database from a local file or from your cloud storage.
Running the pages you fetched and audited yourself while keeping your vault in the
cloud is a perfectly ordinary combination — and often the point, since it keeps
the database off the machine entirely.

---

## Running from a download

### How do I run it from a download?

Download the release from our [GitHub releases page][releases] and open
`index.html` in any supported browser; it links to the other pages. From there you
open a KDBX database — a local file, or one in your cloud storage — and navigate,
copy, edit, and save your secrets. A local database saves by downloading the
updated file back to your machine; a cloud database is written straight back to
your provider.

### Does anything leave my machine?

That depends on where your database is, not on where the pages came from. Open a
local database file and nothing leaves your browser after the page has loaded — no
network requests at all. Open one through a cloud connector and the only traffic is
between your browser and your storage provider, to fetch and save the database;
your master password and decrypted secrets still never leave the browser. Either
way there are no KeePass Web servers in the path, which you can confirm in the
browser network tab.

---

## Running from keepass-web.app

### Where is keepass-web.app hosted?

keepass-web.app is served by [GitHub Pages][ghpages] — there are no KeePass Web
servers. The domain resolves to GitHub's infrastructure and serves a static file
from a public repository. You can verify this by checking the repository at
[github.com/keepass-web/keepass-web.app][ghrepo].

### Are the files at keepass-web.app the same as the ones I download?

Yes. Each distributable served at [keepass-web.app][kpo] is byte-for-byte
identical to the same file in our GitHub releases. You can verify this by
comparing checksums. We assert this openly because your trust in the served
copies should be grounded in your ability to read and verify the ones you
download — not in our word alone.

### Does keepass-web.app ever see my passwords?

No. There are no KeePass Web servers — keepass-web.app is a static file on GitHub
Pages. Decryption happens entirely in your browser. Your master password is never
transmitted. If you open a database from cloud storage, your browser fetches it
directly from your provider. You can verify this in the network tab: after the
initial page load, any requests go to your storage provider, never to
keepass-web.app.

### What happens if keepass-web.app shuts down?

Everything the project relies on — the app at keepass-web.app, source code,
releases, and sponsorships — runs on GitHub. If we lose access to GitHub, or GitHub itself
disappears, keepass-web.app goes with it. We think that is an acceptable risk:
GitHub is well-established, the software is MIT-licensed so anyone can fork and
host it, and most importantly, your KDBX file stays in your own cloud storage
provider. It was never ours. Download the pages from any surviving fork,
or open your database in KeePassXC, Strongbox, KeePassium, or any other
KDBX-compatible client. You are never locked in.

[kdbx]:https://keepass.info/help/kb/kdbx.html
[webcrypto]:https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API
[kpo]:https://keepass-web.app
[ghs]:https://github.com/sponsors/keepass-web
[releases]:https://github.com/keepass-web/source-application/releases
[ghpages]:https://pages.github.com
[ghrepo]:https://github.com/keepass-web/keepass-web.app
[ghorg]:https://github.com/keepass-web
[discussions]:https://github.com/keepass-web/source-application/discussions
[issues]:https://github.com/keepass-web/source-application/issues

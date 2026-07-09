# Frequently Asked Questions

## General

### What is KeePass Web?

KeePass Web is a password manager that runs entirely in your web browser. It
reads and writes [KDBX][kdbx] database files — the same format used by KeePass,
KeePassXC, Strongbox, KeePassium, and others. It ships as self-contained, single-page HTML distributables — each doing one
job — with no external dependencies.

### What is the current project status?

KeePass Web is under active development. As of June 2026, the infrastructure is
in place — the domain, GitHub Pages, sponsorship tiers, and organization
documentation — but no application has been released yet. We expect to publish
the first release — a set of single-page distributables, with full KDBX read and write support
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

You don't have to take our word for it. Each of KeePass Web's distributables is a
single, un-minified HTML page. Open the one you are about to use in a text editor
before you open your database.
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

The cloud connectors are single-page distributables of their own — part of
KeePass Web just like the app and router pages, the same whether you download
them or open the identical copies at [keepass-web.app][kpo]. They belong to no
one version.

### Which cloud storage providers will be supported?

Google Drive, Dropbox, and OneDrive at launch. WebDAV (Nextcloud, ownCloud,
and similar) is planned for a subsequent release.

### Do I need to sponsor to connect my cloud storage?

No. The connectors are open to everyone. The application is MIT-licensed and its
source is public, and it connects to your own provider with your own sign-in — no
sponsorship required, and no storage of ours involved. We ask for support because
the work has real costs, not because we withhold anything. The project runs on
the trust that people who find the software valuable will help fund it.

### Do the connectors work in the downloaded file too?

Yes. The connector code is present and readable in `keepassweb.html`, identical
to the copy served at keepass-web.app — we want you to be able to audit exactly
what it does before trusting it with your database. Connecting to a provider
simply has little practical use once you have downloaded and opened your file
locally: your database is already on your machine.

---

## Local version (the download)

### How do I use the download?

Download the release from our [GitHub releases page][releases] and open
`index.html` in any supported browser; it links to the other distributables.
Upload your KDBX database, navigate your secrets, copy and paste them, edit if
you like. Save by downloading the updated file back to your machine.

### Does anything leave my machine?

No. When you open a local database file, the app makes no network requests after
the page loads. Your KDBX file and your master password never leave your browser.
You can verify this by watching the browser network tab while it runs.

---

## Hosted version (keepass-web.app)

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
transmitted. Your KDBX file is fetched directly from your cloud storage provider
by your browser. You can verify this by watching the network tab: after the
initial page load, all requests go to your cloud storage provider, not to
keepass-web.app.

### What happens if keepass-web.app shuts down?

Everything the project relies on — the app at keepass-web.app, source code,
releases, and sponsorships — runs on GitHub. If we lose access to GitHub, or GitHub itself
disappears, keepass-web.app goes with it. We think that is an acceptable risk:
GitHub is well-established, the software is MIT-licensed so anyone can fork and
host it, and most importantly, your KDBX file stays in your own cloud storage
provider. It was never ours. Download `keepassweb.html` from any surviving fork,
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

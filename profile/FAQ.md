# Frequently Asked Questions

## General

### What is KeePass Web?

KeePass Web is a password manager that runs entirely in your web browser. It
reads and writes [KDBX][kdbx] database files — the same format used by KeePass,
KeePassXC, Strongbox, KeePassium, and others. It ships as a single HTML file
with no external dependencies.

### What is the current project status?

KeePass Web is under active development. As of June 2026, the infrastructure is
in place — the domain, GitHub Pages, sponsorship tiers, and organization
documentation — but no application has been released yet. We expect to publish
the first release of `keepassweb.html` with full KDBX read and write support,
and launch [keepass-web.app][kpo] with cloud storage integration, by
mid-September 2026. Follow development at
[github.com/keepass-web][ghorg].

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

You don't have to take our word for it. The entire application is a single,
un-minified HTML file. Open it in a text editor before you open your database.
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
nothing is gated. [keepass-web.app][kpo] and its cloud storage are open to
everyone; sponsors simply keep the work going.

---

## Local version (keepassweb.html)

### How do I use the local version?

Download `keepassweb.html` from our [GitHub releases page][releases]. Open it in
any supported browser. Upload your KDBX database, navigate your secrets, copy and
paste them, edit if you like. Save by downloading the updated file back to your
machine.

### Does anything leave my machine?

No. The local version makes no network requests after the file loads. Your KDBX
file and your master password never leave your browser. You can verify this by
watching the browser network tab while it runs.

### Why doesn't the local version support cloud storage?

It does — the cloud storage code is present and readable in `keepassweb.html`,
because we want you to be able to audit exactly what the hosted version does
before trusting it with your database. Cloud storage simply has no practical
use when running locally: your files are already on your machine.

---

## Hosted version (keepass-web.app)

### Where is keepass-web.app hosted?

keepass-web.app is served by [GitHub Pages][ghpages] — there are no KeePass Web
servers. The domain resolves to GitHub's infrastructure and serves a static file
from a public repository. You can verify this by checking the repository at
[github.com/keepass-web/keepass-web.app][ghrepo].

### Is keepass-web.app the same file as keepassweb.html?

Yes. The file served at [keepass-web.app][kpo] is identical to the file in our
GitHub releases. You can verify this by comparing checksums. We assert this
openly because your trust in the hosted version should be grounded in your
ability to read and verify the local version — not in our word alone.

### Does keepass-web.app ever see my passwords?

No. There are no KeePass Web servers — keepass-web.app is a static file on GitHub
Pages. Decryption happens entirely in your browser. Your master password is never
transmitted. Your KDBX file is fetched directly from your cloud storage provider
by your browser. You can verify this by watching the network tab: after the
initial page load, all requests go to your cloud storage provider, not to
keepass-web.app.

### What cloud storage providers will be supported?

Google Drive, Dropbox, and OneDrive at launch. WebDAV (Nextcloud, ownCloud,
and similar) is planned for a subsequent release.

### Do I need to sponsor to use cloud storage?

No. Cloud storage is open to everyone. The application is MIT-licensed and its
source is public, and keepass-web.app connects to your provider with your own
sign-in — no sponsorship required. We ask for support because the work has real
costs, not because we withhold anything. keepass-web.app runs on the trust that
people who find the software valuable will help fund it.

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

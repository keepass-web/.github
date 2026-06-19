# Frequently Asked Questions

## What is KeePass Web?

KeePass Web is a password manager that runs entirely in your web browser. It
reads and writes [KDBX][kdbx] database files — the same format used by KeePass,
KeePassXC, Strongbox, KeePassium, and others. It ships as a single HTML file
with no external dependencies.

## What is a KDBX file?

KDBX is an open, well-documented file format for storing passwords and secrets.
It uses strong encryption and tamper-evident protections. Because it is an open
format, many independent applications can read and write it. Your passwords are
not locked to any single vendor — including us.

## What browsers are supported?

Any modern desktop browser that supports [WebCrypto][webcrypto]: Chrome, Firefox,
Safari, Edge, and terminal browsers such as Browsh and Carbonyl. WebCrypto is the
only browser API KeePass Web requires.

## How do I know it's safe?

You don't have to take our word for it. The entire application is a single,
un-minified HTML file. Open it in a text editor before you open your database.
Watch the browser network tab while it runs — you will see no network requests
for the free local version. The source code is published on GitHub and the
application is periodically subjected to independent security research through a
funded bug bounty program.

## Does keepassweb.app ever see my passwords?

No. Decryption happens entirely in your browser. Your master password is never
transmitted. Your KDBX file is fetched directly from your cloud storage provider
(Google Drive, Dropbox, OneDrive, etc.) by your browser — it does not pass
through our servers. You can verify this by watching the network tab: after the
initial page load, no requests are made to keepassweb.app.

## What is the difference between the free version and the premium version?

The free version is a single HTML file you download and open locally. It works
with any KDBX file on your machine. Nothing leaves your computer.

The premium version is available at [keepassweb.app][kpo] to
[GitHub Sponsors][ghs]. It connects KeePass Web to your own cloud storage
provider so you can access your KDBX database from any browser, anywhere,
without manually transferring files. Your data stays in your storage — we never
hold it.

## What cloud storage providers are supported?

Google Drive, Dropbox, and OneDrive. Support for WebDAV (Nextcloud, ownCloud,
and similar) is planned.

## What happens if keepassweb.app shuts down?

Your KDBX file stays in your cloud storage provider — it was never ours to begin
with. Open it in KeePassXC, Strongbox, KeePassium, or any other KDBX-compatible
client. You are never locked in.

## Why did you write your own KDBX parser instead of using an existing library?

Security software that depends on third-party libraries inherits that library's
security fix schedule. If a vulnerability is discovered in a dependency, we are
blocked on someone else's availability and priorities to ship a fix. By owning
the parser ourselves, we control when fixes ship.

## Why no JavaScript or CSS frameworks?

Every dependency is an attack surface and code you cannot fully audit. We keep
the codebase small enough that a technically literate user can read all of it.
Frameworks make that impractical.

## How does GitHub Sponsorship work?

Visit [github.com/sponsors/keepass-web][ghs] and choose a tier. Monthly sponsors
at the convenience tier get access to keepassweb.app. One-time contributions
support maintenance and the bug bounty program but do not unlock keepassweb.app.

[kdbx]:https://keepass.info/help/kb/kdbx.html
[webcrypto]:https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API
[kpo]:https://keepassweb.app
[ghs]:https://github.com/sponsors/keepass-web

# Rationale, or Why Bother?

The [KeePass 2.x database file format (KDBX)][ref1] securely stores user names,
passwords, and other information in a local file using strong encryption and
tamper-evident protections. The open source [KeePass for Windows][ref2] program
maintains this format specification, offers a reference implementation, and
links to [unofficial ports][ref3] for other platforms.

Native applications, official or not, present several challenges. For one, not
all systems allow third-party software installation. For another, the user
interface differs between each KDBX-compatible application. Additionally, the
implementations are of varying quality: lots of open issues, discontinued
development, no installers or complex installation steps. Also, incompatibilities
between differing KDBX reader/writer implementations may result in database errors
or corruption. Finally, are the applications, whether closed- or open-source,
trustworthy?

Given these challenges, a browser-based KeePass application seems like the ideal
interface for reading and writing a local KDBX file. Browsers are ubiquitous,
richly interactive, and inherently open: network traffic is inspectable and
source code is run locally.

However, the existing browser-based KeePass applications listed on the
[KeePass for Windows unofficial ports page][ref3] suffer from similar challenges
(as of March, 2024):
* [Keeweb][ref4] has over 350 open issues and is two years out of date
* [Keevault.pm][ref5] is closed source and crashes in DuckDuckGo
* [Keepass for Web][ref6] is abandoned and the Rust rewrite, frighteningly, has
  rolled its own "new and unique encryption key"

With nothing on the market to satisfy the design goals, it was time to build a
KDBX-compatible application that is:
* Browser-based, so nothing to install and a universal interface
* Source available, to ensure the code is trustworthy
* Hacker verified, to ensure the code is secure

## Simple and Trustworthy

A password manager is only trustworthy if you can verify what it does. Complex
software makes that verification impractical for all but the most technically
literate users. KeePass Web builds trust by shipping as a single, self-contained
HTML file with no external dependencies: everything it does is right there in
the un-minified source code. Anyone should be able, with or without AI
assistance, to understand exactly what Keepass Web does in a single sitting.

Don't trust us with your password? Great! Read the source code and understand
how it'll work before you upload your database file. Or, just watch the browser
network tab as it runs, and you'll see it makes no network calls.

Is there a bug in the code? No problem. We own every dependency. No fancy CSS or
Javascript frameworks and no external libraries for reading or writing the KDBX
format. We wrote it, we'll fix it, and the result is still code that you can
audit in a simple text editor.

We choose simplicity because vulnerabilities hide in complexity. We chose open
source because you deserve to know how your secrets are handled with more than a
"trust us" statement.

## How Keepass Web Works

**Free, local use:** Download the HTML file from our GitHub releases page. Open
it in any browser with [WebCrypto][ref7] support (which is every modern desktop
browser that runs Javascript). Upload your KDBX database into the application.
Navigate your secrets, copy and paste them, edit if you like. You can save them
by downloading a new version and storing it on your local machine. Your file and
its secrets never leave your machine.

**Premium, hosted use:** Visit [keepass.online][ref8]. Sign in with your GitHub
account and support us with a GitHub Sponsorship. Connect your cloud storage
provider: Google Drive, Dropbox, OneDrive, or similar.  Navigate your storage
provider and open your KDBX database directly from your storage. Your database
and your master password never touch our servers; decryption happens entirely in
your browser.

The hosted version offers a convenient way for you to access a shared KDBX file
held in your own storage from anywhere, anytime, without transferring files or
dealing with write locks.

## Bottom Line

If you find yourself wanting complete control over where your passwords are
stored, unable or unwilling to install a native application, and distrusting the
quality, stability or security of other KDBX-compatible clients, then KeePass
Web is for you!

Find out more:
* [Our design and development philosophies.](/profile/PHILOSOPHY.md)
* [Our licensing model.](/profile/LICENSING.md)

Ready to start?
* [Try KeePass Web online, in your browser, right now.](/profile/TODO.md)
* [Download the most recent public release and run in your local browser.](/profile/TODO.md)
* [Become a GitHub Sponsor to unlock convenience features.](/profile/TODO.md)

Not convinced?
* [Check out our Frequently Asked Questions.](/profile/FAQ.md)
* [Read testimonies from sponsors who support KeePass Web development.](/profile/TODO.md)
* [See our awards and accolades.](/profile/TODO.md)


[ref1]:https://keepass.info/help/kb/kdbx.html
[ref2]:https://keepass.info/
[ref3]:https://keepass.info/download.html
[ref4]:https://github.com/keeweb/keeweb
[ref5]:https://keevault.pm/
[ref6]:https://github.com/lixmal/keepass4web/?tab=readme-ov-file
[ref7]:https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API
[ref8]:https://keepass.online

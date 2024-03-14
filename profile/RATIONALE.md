# Rationale, or Why Bother?

The [KeePass 2.x database file format (KDBX)][ref1] securely stores user name,
passwords, and other information in a local file using strong encryption and
tamper-evident protections. The open source [KeePass for Windows][ref2] program
maintains this format specification, offers a reference implementation, and
links to [unofficial ports][ref3] for other platforms.

Native applications, official or not, present several challenges. For one, not
all systems allow third-party software installation. For another, the user
interface differs between each KDBX-compatible application. Additionally, the
implementations are of varying quality: lots of open issues, discontinued
development, no installers or complex installation steps. Finally, are the
applications, whether closed- or open-source, trust-worthy?

Given these challenges, a browser-based KeePass application seems like the ideal
interface for reading and writing a local KDBX file. Browsers are ubiquitous,
richly interactive, and inherently open: network traffic is inspectable and
source code is run locally.

However, the existing browser-based KeePass applications listed on the
[unofficial ports page][ref3] suffer from similar challenges (as of March, 2024):
* [Keeweb][ref4] has over 350 open issues and is two years out of date
* [Keevalut.pm][ref5] is closed source and crashes in DuckDuckGo
* [Keepass for Web][ref6] is abandoned and the Rust rewrite, frighteningly, has
  rolled its own "new and unique encryption key"

With nothing on the market to satisfy the design goals, it was time to build a
KDBX-compatible application that is:
* Browser-based, so nothing to install and a universal interface
* Source available, to ensure the code is trustworthy
* Hacker verified, to ensure the code is secure

[ref1]:https://keepass.info/help/kb/kdbx.html
[ref2]:https://keepass.info/
[ref3]:https://keepass.info/download.html
[ref4]:https://github.com/keeweb/keeweb
[ref5]:https://keevault.pm/
[ref6]:https://github.com/lixmal/keepass4web/?tab=readme-ov-file

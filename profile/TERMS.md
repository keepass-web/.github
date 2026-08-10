# Terms of Use

**Effective Date: August 9, 2026**

These Terms of Use (this "Agreement") constitute a legally binding agreement
between you ("you," "your," or "User") and KeePass Web, a trade name (DBA)
of Bishop Bettini ("we," "us," "our"), governing your access to and use of
the Service, described in Section 3 below. By accessing, downloading, or
using any part of the
Service, you accept and agree to be bound by this Agreement. If you do not
agree, you must not access or use the Service. This Agreement should be
read together with our [Privacy Policy][privacy], which is incorporated
into it by reference.

## 1. Definitions

For purposes of this Agreement, the following terms have the meanings given
below. Other capitalized terms are defined where they first appear.

**"Agreement"** means these Terms of Use and the [Privacy Policy][privacy],
collectively.

**"Content"** means any text, data, code, or other material published by us
as part of the Service, excluding any Database.

**"Database"** means a [KDBX-format][kdbx] file containing your passwords
or other secrets, whether stored locally on a device you control or with a
Provider.

**"Provider"** means a third-party cloud storage service (for example,
Google Drive) that you connect to the Service through a Connector.

**"Connector"** means a page of the Service that facilitates a direct
connection between your browser and a Provider you have chosen, as
described in Section 7.

**"Service"** means the KeePass Web software described in Section 3,
including every page published from [the source repository][repo] and the
identical copies served at [keepass-web.app][kpo].

**"Software"** means the source code of the Service, licensed under the
[MIT License][license].

## 2. Acceptance of Terms; Eligibility

2.1. By using the Service, you represent that you have read, understood,
and agree to be bound by this Agreement.

2.2. You represent that you are at least 13 years of age. If you are a
minor under the law of your jurisdiction of residence, you represent that
you have obtained the consent of a parent or legal guardian to use the
Service, and that such parent or guardian agrees to be bound by this
Agreement on your behalf.

2.3. You represent that your use of the Service does not violate any law
or regulation applicable to you, including any export control or economic
sanctions law described in Section 17.

## 3. Description of the Service

3.1. The Service is a set of self-contained, client-side web pages that
read, write, create, and edit Database files entirely within your web
browser. The Service has no backend: no server operated by
us receives, processes, transmits, or stores your Database, your master
password, or any data decrypted from your Database, under any
circumstance.

3.2. The Service is distributed two ways, which are functionally
identical: (a) as downloadable files from [our releases page][releases],
which you may run entirely offline after downloading; and (b) as static
files served at [keepass-web.app][kpo] by GitHub Pages, a third-party
hosting service. We do not operate any server in either distribution
method.

3.3. Independent verification. Because the Service is distributed as
un-minified source, you may inspect its full behavior before use, and you
may independently confirm the absence of network activity using your
browser's developer tools. Guidance for doing so is published at
[Trust][trust].

## 4. No User Accounts

The Service does not implement any account, registration, authentication,
or user-profile system of its own. We do not assign you a username, do not
require or store a password of our own, and do not maintain any record
identifying you as a user of the Service. Section 7 describes the separate
authentication systems operated by third-party Providers, which are not
part of the Service and are not administered by us.

## 5. Your Database and Credentials

5.1. Sole responsibility. You are solely responsible for maintaining
backup copies of your Database and for safeguarding your master password
and any other credential required to decrypt it.

5.2. No recovery mechanism. The Service provides no mechanism to recover a
forgotten master password or to reconstruct a lost or corrupted Database.
This limitation is inherent to the architecture described in Section 3.1:
because no copy of your master password or Database is ever transmitted to
or retained by us, no such copy exists for us, or anyone else, to recover
on your behalf.

5.3. Assumption of risk. You acknowledge and agree that your use of the
Service to store, access, or transmit sensitive credentials is at your
sole risk, and that permanent loss of access to a Database is a foreseeable
consequence of using client-side, non-custodial software of this kind.

## 6. Open-Source License; Trademarks

6.1. License to the Software. The Software is licensed to you under the
terms of the [MIT License][license]. The MIT License governs your rights
to use, copy, modify, merge, publish, distribute, sublicense, and sell
copies of the Software. In the event of any conflict between this
Agreement and the MIT License with respect to the Software itself, the MIT
License controls; this Agreement otherwise governs your use of the Service
as we operate and publish it.

6.2. Trademarks. The MIT License grants no rights in, and this Agreement
grants no rights in, the name "KeePass Web" or any associated logo (the
"Marks"). You may not use the Marks in a manner that states or implies
affiliation with, sponsorship by, or endorsement from us without our prior
written consent, except as necessary to accurately describe the origin of
software you have forked under the MIT License.

6.3. No affiliation with KeePass. The Service is an independent,
compatible implementation of the openly documented [KDBX file
format][kdbx]. It is not affiliated with, endorsed by, or sponsored by the
KeePass Password Safe project or its author.

## 7. Third-Party Cloud Storage Connectors

7.1. General. The Service may offer one or more Connectors that allow you
to open and save a Database directly with a Provider of your choosing. The
current list of available Connectors is published at [Pages][pages] and
may change over time.

7.2. Authentication. Where you use a Connector, you authenticate directly
with the Provider through that Provider's own official sign-in mechanism
(for example, [Google Identity Services][gis-token] for the Google Drive
Connector). We do not receive, process, or store your Provider credentials
or any access token issued to you by a Provider.

7.3. Scope of access. Each Connector requests the narrowest access scope
reasonably available for its function (for example, Google Drive's
`drive.file` scope, limited to files you explicitly select through the
Provider's own file picker). We do not use any access granted by a
Provider for any purpose beyond retrieving and saving the specific
Database you have opened or created.

7.4. Data flow. When you use a Connector, your Database is transmitted
directly between your browser and the Provider's own servers. No such
transmission passes through, or is observable by, us.

7.5. Provider terms govern. Your use of any Provider is governed solely by
that Provider's own terms of service and privacy policy, which we do not
control and for which we assume no responsibility. Any dispute concerning
the availability, security, or handling of your data by a Provider is
between you and that Provider.

## 8. Acceptable Use

You agree not to, and not to assist any third party to:

(a) use the Service for any unlawful purpose or in violation of any
applicable law or regulation;

(b) attempt to interfere with, disrupt, or gain unauthorized access to
keepass-web.app, [the source repository][repo], or any infrastructure
operated by us or on our behalf;

(c) use a Connector in a manner that violates the terms of service of the
connected Provider;

(d) misrepresent your use, modification, or redistribution of the Service
as being official, endorsed, or sponsored by us, in violation of Section
6.2; or

(e) reverse engineer, decompile, or attempt to derive source code from the
Service where such source code is not already published, provided that
this restriction does not apply to the Software, which is licensed under
the MIT License and whose source is published in full.

## 9. Feedback

If you submit feedback, suggestions, or bug reports regarding the Service
(for example, through [GitHub Discussions][discussions] or [our issue
tracker][issues]), you grant us a perpetual, irrevocable, worldwide,
royalty-free license to use that feedback for any purpose, without
obligation or compensation to you, and subject to the terms of the
[MIT License][license] where such feedback takes the form of a code
contribution.

## 10. Copyright Complaints

The Service, including keepass-web.app, is hosted by GitHub, Inc. If you
believe that Content published as part of the Service infringes your
copyright, please submit a notice through [GitHub's content removal
process][gh-dmca]. You may also contact us directly using the information
in Section 30.

## 11. DISCLAIMER OF WARRANTIES

**THE SERVICE, INCLUDING ALL SOFTWARE AND CONTENT, IS PROVIDED "AS IS" AND
"AS AVAILABLE," WITHOUT WARRANTY OF ANY KIND, WHETHER EXPRESS, IMPLIED, OR
STATUTORY. TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, WE DISCLAIM
ALL WARRANTIES, INCLUDING WITHOUT LIMITATION THE IMPLIED WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, TITLE, AND
NON-INFRINGEMENT, AND ANY WARRANTY ARISING FROM COURSE OF DEALING OR USAGE
OF TRADE. WE DO NOT WARRANT THAT THE SERVICE WILL BE UNINTERRUPTED,
TIMELY, SECURE, OR ERROR-FREE; THAT ANY DATABASE WILL BE PRESERVED OR
RECOVERABLE; THAT A FORGOTTEN MASTER PASSWORD CAN BE RECOVERED; OR THAT
THE SERVICE IS COMPATIBLE WITH ANY PARTICULAR KDBX-PRODUCING OR
KDBX-CONSUMING APPLICATION. NO ADVICE OR INFORMATION, WHETHER ORAL OR
WRITTEN, OBTAINED FROM US OR THROUGH THE SERVICE SHALL CREATE ANY WARRANTY
NOT EXPRESSLY STATED IN THIS AGREEMENT.**

Some jurisdictions do not allow the exclusion of certain implied
warranties, so some of the above exclusions may not apply to you. In such
jurisdictions, our warranties are limited to the minimum scope and
duration permitted by law.

## 12. LIMITATION OF LIABILITY

**TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, IN NO EVENT SHALL WE
BE LIABLE FOR ANY INDIRECT, INCIDENTAL, SPECIAL, CONSEQUENTIAL, EXEMPLARY,
OR PUNITIVE DAMAGES, OR FOR ANY LOSS OF DATA, LOSS OF ACCESS TO ANY
DATABASE, OR INABILITY TO RECOVER A FORGOTTEN MASTER PASSWORD, HOWEVER
CAUSED AND UNDER ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, TORT
(INCLUDING NEGLIGENCE), OR OTHERWISE, EVEN IF WE HAVE BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES. TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE
LAW, OUR AGGREGATE LIABILITY ARISING OUT OF OR RELATING TO THIS AGREEMENT
OR THE SERVICE SHALL NOT EXCEED THE TOTAL AMOUNT, IF ANY, PAID BY YOU TO US
FOR USE OF THE SERVICE, WHICH THE PARTIES ACKNOWLEDGE IS ZERO.**

Nothing in this Agreement excludes or limits liability that cannot be
excluded or limited under applicable law, including liability for gross
negligence or willful misconduct to the extent such limitation is
prohibited under North Carolina law.

## 13. Indemnification

You agree to defend, indemnify, and hold harmless KeePass Web from and
against any claim, liability, damage, loss, or expense, including
reasonable attorneys' fees, arising out of or relating to: (a) your
violation of this Agreement; (b) your violation of any Provider's terms of
service through use of a Connector; or (c) your violation of any applicable
law or the rights of any third party.

## 14. Suspension, Termination, and Discontinuation

14.1. Because the Service requires no account, "termination" refers to the
availability of the Service to you, not to any account.

14.2. We may restrict or block access to keepass-web.app from any source we
reasonably believe is engaged in conduct prohibited by Section 8, without
notice.

14.3. We may modify, suspend, or discontinue keepass-web.app, in whole or
in part, at any time, without notice and without liability to you. Because
the Software is licensed under the MIT License and published publicly,
your ability to run, fork, or independently host a copy of it does not
depend on our continued operation of keepass-web.app.

## 15. Export Control and Compliance

You represent that you are not located in, and are not a national or
resident of, any country subject to a comprehensive embargo under the laws
of the United States, and that you are not identified on any list of
prohibited or restricted parties maintained by the United States
government. You agree to comply with all applicable export control and
economic sanctions laws in your use of the Service.

## 16. Relationship of the Parties

Nothing in this Agreement creates a partnership, joint venture, agency, or
employment relationship between you and us. Neither party has authority to
bind the other or to incur any obligation on the other's behalf.

## 17. No Third-Party Beneficiaries

Except as expressly stated in Section 13, this Agreement does not confer
any rights or remedies upon any person or entity other than you and us.

## 18. Assignment

You may not assign or transfer this Agreement, by operation of law or
otherwise, without our prior written consent. We may assign this Agreement,
in whole or in part, without restriction, including in connection with a
transfer of the Service's operation. Any attempted assignment in violation
of this Section is void.

## 19. Force Majeure

We shall not be liable for any failure or delay in the availability of the
Service resulting from causes beyond our reasonable control, including acts
of God, internet or utility failures, or failures of third-party
infrastructure such as GitHub Pages.

## 20. Waiver

No failure or delay by either party in exercising any right under this
Agreement shall operate as a waiver of that right. Any waiver must be in
writing to be effective and applies only to the specific instance given.

## 21. Notices

Because the Service maintains no accounts and no means of individually
contacting Users, notice of changes to this Agreement is given exclusively
by publication under Section 29. Notices to us must be sent via
[GitHub Discussions][discussions] or, for security-related matters, to
[security@keepass-web.app](mailto:security@keepass-web.app).

## 22. Governing Law and Jurisdiction

This Agreement is governed by the laws of the State of North Carolina,
USA, without regard to its conflict-of-laws principles. You agree that the
state and federal courts located in Wake County, North Carolina have
exclusive jurisdiction over any dispute arising out of or relating to this
Agreement or the Service, and you consent to the personal jurisdiction of
those courts.

## 23. Informal Dispute Resolution

Before initiating any formal proceeding, you agree to first attempt to
resolve the dispute informally by contacting us as described in Section
21 and allowing a reasonable opportunity to respond.

## 24. Severability

If any provision of this Agreement is held invalid or unenforceable, that
provision shall be limited or eliminated to the minimum extent necessary,
and the remaining provisions shall remain in full force and effect.

## 25. Entire Agreement

This Agreement, together with the [Privacy Policy][privacy] and the
[MIT License][license] as it applies to the Software, constitutes the
entire agreement between you and us regarding the Service and supersedes
all prior or contemporaneous agreements, whether written or oral,
regarding the same subject matter.

## 26. Headings and Interpretation

Section headings are for reference only and do not affect interpretation.
"Including" means "including without limitation."

## 27. Amendments

We may amend this Agreement at any time by publishing a revised version
with an updated Effective Date. The full revision history is publicly
available in [this repository's commit log][repo-github]. Your continued
use of the Service after an amendment takes effect constitutes acceptance
of the amended Agreement.

## 28. Contact Information

General questions regarding this Agreement: [GitHub Discussions][discussions].
Security-related matters: [security@keepass-web.app](mailto:security@keepass-web.app).
Copyright complaints: Section 10.

[repo]:https://github.com/keepass-web/source-application
[repo-github]:https://github.com/keepass-web/.github/commits/main/profile/TERMS.md
[kpo]:https://keepass-web.app
[privacy]:https://github.com/keepass-web/.github/blob/main/profile/PRIVACY.md
[kdbx]:https://keepass.info/help/kb/kdbx.html
[releases]:https://github.com/keepass-web/source-application/releases
[trust]:https://github.com/keepass-web/source-application#trust
[license]:https://github.com/keepass-web/source-application/blob/main/LICENSE
[pages]:https://github.com/keepass-web/source-application/blob/main/docs/PAGES.md
[discussions]:https://github.com/keepass-web/source-application/discussions
[issues]:https://github.com/keepass-web/source-application/issues
[gis-token]:https://developers.google.com/identity/oauth2/web/guides/use-token-model
[gh-dmca]:https://docs.github.com/en/site-policy/content-removal-policies

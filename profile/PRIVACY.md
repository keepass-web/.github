# Privacy Policy

**Effective Date: August 9, 2026**

This Privacy Policy explains how personal data is handled in connection
with the Service. It is incorporated by reference into, and should be read
together with, our [Terms of Use][terms]. Capitalized terms not defined
here have the meanings given in the Terms of Use.

## 1. Summary

This Service is architected to process no personal data on our side at
all. Section 5 sets out, category by category, the personal data we do not
collect. Sections 8 and 9 disclose the two situations that are outside our
control: the request logs of our hosting provider, and the third-party
services you may optionally connect to. Every representation in this
Policy can be independently verified using the method described in
Section 6.

## 2. Definitions

**"Controller"** means the natural or legal person who determines the
purposes and means of the processing of personal data, as that term is
used in the EU General Data Protection Regulation ("GDPR").

**"Personal Data"** and **"Personal Information"** mean, respectively, any
information relating to an identified or identifiable natural person under
the GDPR, and any information that identifies, relates to, or could
reasonably be linked with a particular consumer or household under the
California Consumer Privacy Act, as amended by the California Privacy
Rights Act ("CCPA").

**"Processing"** means any operation performed on Personal Data, including
collection, storage, use, disclosure, or transmission.

## 3. Data Controller and Contact Information

The Controller of any Personal Data addressed by this Policy is KeePass
Web, a trade name (DBA) of Bishop Bettini. Contact information is provided
in Section 20.

## 4. Data Protection Officer

We have not appointed a Data Protection Officer. Appointment of a Data
Protection Officer is not mandatory under Article 37 of the GDPR for a
controller whose processing does not meet the thresholds described in that
Article, which, as explained in Section 5, is the case here because no
systematic processing of Personal Data occurs.

## 5. Personal Data We Do Not Collect

The Service has no backend. No server operated by us receives, transmits,
or stores any of the following, whether from you directly, automatically,
or from any third party, in connection with your use of the Service:

| Category | Collected |
|---|---|
| Identifiers (name, email address, IP address, device or account identifiers) | Not collected |
| Account credentials (username, password) | Not collected — the Service has no account system |
| Your master password or any credential used to decrypt a Database | Not collected, not transmitted, not logged |
| The contents of any Database, decrypted or otherwise | Not collected, not transmitted, not logged |
| Commercial information (purchase history, records of services used) | Not collected |
| Internet or network activity information (browsing history, search history) | Not collected |
| Geolocation data | Not collected |
| Audio, electronic, visual, or similar information | Not collected |
| Professional or employment-related information | Not collected |
| Education information | Not collected |
| Inferences drawn from any of the above | Not collected, as none of the above is collected |
| Sensitive personal information (government ID, financial account credentials, precise geolocation, health data, and similar categories under the CCPA/CPRA) | Not collected |

## 6. How This Is Verifiable

Because the Service's source is published un-minified, you may confirm the
absence of data collection directly: open your browser's network inspector
before opening a Database on the app page or any offline page, and confirm
no outbound request is made; open the storage inspector and confirm no
cookie, `localStorage`, `sessionStorage`, or `IndexedDB` entry is written.
Detailed guidance is published at [How do I know it's safe?][faq-safe].

## 7. Legal Basis for Processing

Article 6 of the GDPR requires a lawful basis for each processing
activity. Because we do not process Personal Data as described in Section
5, no processing activity requiring a legal basis occurs, and this Policy
identifies none. If this changes in a future version of the Service, this
Policy will be amended in accordance with Section 19 to disclose the
purpose and legal basis of any new processing before it occurs.

## 8. Hosting Infrastructure

[keepass-web.app][kpo] is not hosted on infrastructure we operate. It is
served as static files by GitHub Pages, a service of GitHub, Inc., from a
public repository. As an ordinary incident of serving any web request,
GitHub's infrastructure may log standard technical request data, such as
IP address, requested resource, timestamp, and user agent. That logging is
performed by GitHub as an independent controller of that data, under
[GitHub's own Privacy Statement][gh-privacy]; we have no access to,
copy of, or ability to export those logs. If you wish to avoid this
category of third-party logging entirely, download a release and run it
from local disk instead — see [Running from a download][faq-download].

## 9. Cookies and Similar Tracking Technologies

The Service itself sets no cookies and uses no similar tracking
technology, including web beacons, pixels, or fingerprinting scripts. No
analytics, telemetry, or crash-reporting service of any kind is integrated
into the Service. If you use a Connector described in Section 10, the
Provider you sign in to may set its own cookies or browser storage on its
own domain, under its own policy; those are not set by us and are outside
the scope of this Section.

## 10. Third-Party Cloud Storage Connectors

10.1. General. If you choose to open or save a Database using a Connector
(currently Google Drive; see [Pages][pages] for the current list), the
following applies for that session only.

10.2. Authentication. You authenticate directly with the Provider through
its own sign-in mechanism (for Google Drive, [Google Identity
Services][gis-token]). We do not receive or store your Provider
credentials or any access token issued to you.

10.3. Scope. File access is limited to the narrowest scope reasonably
available — for Google Drive, the `drive.file` scope, limited to files you
explicitly select.

10.4. Data flow. Your Database is transmitted directly between your
browser and the Provider's servers. This transmission does not pass
through, and is not observable by, us.

10.5. Applicable policy. The Provider's own privacy policy governs its
processing of your data. For Google Drive, that is [Google's Privacy
Policy][google-privacy] and [Google's Terms of Service][google-terms]. We
are not responsible for a Provider's data handling practices.

## 11. Disclosure of Personal Data; No Sale or Sharing

We do not sell or share Personal Data or Personal Information, as those
terms are defined under the CCPA, because we do not collect any. We have
no mechanism through which Personal Data could be disclosed to a third
party, because none passes through us. Accordingly, no "Do Not Sell or
Share My Personal Information" opt-out mechanism is provided, as none is
necessary.

## 12. International Data Transfers

We do not transfer Personal Data internationally, or at all, because we do
not collect or hold any. Where you use a Connector, any transfer of your
data occurs directly between your browser and your chosen Provider,
under that Provider's own cross-border transfer safeguards, not ours.

## 13. Data Retention

We retain no Personal Data, and therefore apply no retention period,
because none is collected in the first instance.

## 14. Data Security

Your Database is protected by the [KDBX format's][kdbx] own authenticated
encryption, applied and verified entirely within your browser. Technical
detail on what code runs where, and how to verify it independently, is
published at [Trust][trust]. To report a security vulnerability, see
Section 20; please do not report vulnerabilities through a public issue.

## 15. Children's Privacy

The Service is not directed to children, and, consistent with Section 5,
we do not knowingly or otherwise collect Personal Data from children or
any other person. If you believe a child has provided us Personal Data
notwithstanding the absence of any mechanism to do so, contact us using
the information in Section 20 and we will investigate.

## 16. Your Privacy Rights

16.1. Rights under the GDPR. If you are located in the European Economic
Area or the United Kingdom, you have the right to: request access to your
Personal Data; request rectification of inaccurate Personal Data; request
erasure of your Personal Data; request restriction of processing; request
data portability; object to processing; withdraw consent where processing
is based on consent; and lodge a complaint with your local data protection
supervisory authority. Because we do not collect or process Personal Data
as described in Section 5, there is, in the ordinary course, no Personal
Data of yours held by us for these rights to operate on. You may still
contact us using the information in Section 20 to make a request, and we
will confirm the absence of any such data without delay.

16.2. Rights under the CCPA. If you are a California resident, you have
the right to: know what Personal Information is collected; request
deletion of Personal Information; correct inaccurate Personal Information;
opt out of the sale or sharing of Personal Information; limit the use of
sensitive Personal Information; and not receive discriminatory treatment
for exercising these rights. As disclosed in Sections 5 and 11, we
collect no Personal Information and sell or share none, so exercising
these rights will confirm that no data exists to act upon.

16.3. Other jurisdictions. If you reside in a jurisdiction with a similar
data protection or privacy law not otherwise addressed in this Section,
contact us using the information in Section 20 and we will respond
consistent with the rights available to you under that law.

## 17. Automated Decision-Making and Profiling

We do not engage in automated decision-making or profiling that produces
legal effects concerning you or similarly significantly affects you,
because we conduct no processing of Personal Data of any kind.

## 18. Local Operation

Opening a Database from a file stored on your own device involves no
network transmission of any kind. The file is read once, directly within
your browser tab, and is not transmitted anywhere for the duration of that
session.

## 19. Changes to This Policy

We may amend this Policy at any time by publishing a revised version with
an updated Effective Date. The full revision history is publicly available
in [this repository's commit log][repo-github]. Material changes affecting
the processing described in Section 7 will be disclosed prior to taking
effect, consistent with that Section. Your continued use of the Service
after an amendment takes effect constitutes acceptance of the amended
Policy.

## 20. Contact Information

General questions regarding this Policy: [GitHub Discussions][discussions].
Security-related matters, and requests under Section 16:
[security@keepass-web.app](mailto:security@keepass-web.app).

[terms]:https://github.com/keepass-web/.github/blob/main/profile/TERMS.md
[kpo]:https://keepass-web.app
[kdbx]:https://keepass.info/help/kb/kdbx.html
[trust]:https://github.com/keepass-web/source-application#trust
[faq-safe]:https://github.com/keepass-web/.github/blob/main/profile/FAQ.md#how-do-i-know-its-safe
[faq-download]:https://github.com/keepass-web/.github/blob/main/profile/FAQ.md#how-do-i-run-it-from-a-download
[gh-privacy]:https://docs.github.com/en/site-policy/privacy-policies
[pages]:https://github.com/keepass-web/source-application/blob/main/docs/PAGES.md
[gis-token]:https://developers.google.com/identity/oauth2/web/guides/use-token-model
[google-privacy]:https://policies.google.com/privacy
[google-terms]:https://policies.google.com/terms
[discussions]:https://github.com/keepass-web/source-application/discussions
[repo-github]:https://github.com/keepass-web/.github/commits/main/profile/PRIVACY.md

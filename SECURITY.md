# IronCore Security Release Process

IronCore is a growing community of volunteers and users. The IronCore community has adopted this security disclosure and response policy to ensure we responsibly handle critical issues.

## IronCore Security Manager

* Damyan Yordanov (**[@damyan](https://github.com/damyan)**)

## IronCore Security Team

Security vulnerabilities should be handled quickly and sometimes privately. The primary goal of this process is to reduce the total time users are vulnerable to publicly known exploits. The IronCore Security Team is responsible for organizing the entire response, including internal communication and external disclosure, but will need help from relevant developers and release managers to successfully run this process. The IronCore Security Team consists of the following volunteers:

* Damyan Yordanov (**[@damyan](https://github.com/damyan)**)
* Maximilian Moehl (**[@maxmoehl](https://github.com/maxmoehl)**)
* Samira Briongos (**[@SamiraBriongos](https://github.com/SamiraBriongos)**)

## Disclosures

### Private Disclosure Process

The IronCore community asks that all suspected vulnerabilities be privately and responsibly disclosed. If you've found a vulnerability or a potential vulnerability in IronCore, please let us know by writing an e-mail to [ironcore-security@groups.linuxfoundation.org](mailto:ironcore-security@groups.linuxfoundation.org). We'll send a confirmation e-mail to acknowledge your report, and we'll send an additional e-mail when we've identified the issue positively or negatively.

### Public Disclosure Process

If you know of a publicly disclosed vulnerability please IMMEDIATELY write an e-mail to [ironcore-security@groups.linuxfoundation.org](mailto:ironcore-security@groups.linuxfoundation.org) to inform the IronCore Security Team about the vulnerability so they may start the patch, release, and communication process.

If possible, the IronCore Security Team will ask the person making the public report if the issue can be handled via a [private disclosure process](#private-disclosure-process) (for example, if the full exploit details have not yet been published). If the reporter denies the request for private disclosure, the IronCore Security Team will move swiftly with the fix and release process. In extreme cases GitHub can be asked to delete the issue but this generally isn't necessary and is unlikely to make a public disclosure less damaging.

## Patch, Release, and Public Communication

For each vulnerability, a member of the IronCore Security Team will volunteer to lead coordination with the "Fix Team" and is responsible for sending disclosure e-mails to the rest of the community. This lead will be referred to as the "Fix Lead."

The IronCore Security Team may decide to bring in additional contributors for added expertise depending on the area of the code that contains the vulnerability. All of the timelines below are suggestions and assume a private disclosure. The Fix Lead drives the schedule using his best judgment based on severity and development time.

If the Fix Lead is dealing with a public disclosure, all timelines become ASAP and are handled within an appropriate time-frame given the scope of the vulnerability. If the fix relies on another upstream project's disclosure timeline, that will adjust the process as well. We will work with the upstream project to fit their timeline and best protect our users.

### Fix Team Organization

The Fix Lead will work quickly to identify relevant engineers from the affected projects and packages and include those engineers into the disclosure. These selected developers are the Fix Team. The Fix Lead will give the Fix Team access to a private repository to develop the fix.

### Fix Development Process

The Fix Lead and the Fix Team will create a [CVSS](https://www.first.org/cvss/specification-document) using the [CVSS Calculator](https://www.first.org/cvss/calculator/3.0). The Fix Lead makes the final call on the calculated CVSS; it is better to move quickly than make the CVSS perfect.

The Fix Team will notify the Fix Lead that work on the fix branch is complete once there are LGTMs on all commits in the private repository from one or more maintainers.

For lower-severity issues the Fix Team can decide to slow the release process down in the face of holidays, developer bandwidth, etc. These decisions must be discussed on the private [IronCore Security mailing list](#communication-channel).

### Fix Disclosure Process

With the fix development underway, the Fix Lead needs to come up with an overall communication plan for the wider community. This Disclosure process should begin after the Fix Team has developed a Fix or mitigation so that a realistic timeline can be communicated to users. The Fix Lead will inform the [IronCore mailing list](#communication-channel) that a security vulnerability has been disclosed and that a fix will be made available in the future on a certain release date. The Fix Lead will include any mitigating steps users can take until a fix is available. The communication to IronCore users should be actionable. They should know when to block time to apply patches, understand exact mitigation steps, etc.

### Fix Release Day

On the release day, at the communicated time, a maintainer involved in the disclosure process cuts a release and publishes the artifacts. The Fix Lead requests a CVE via the [GitHub Security advisory process](https://docs.github.com/en/code-security/security-advisories) and announces the release, the CVE number, and the relevant merged PRs on the [IronCore mailing list](#communication-channel). The announcement should be actionable and include links on how to apply the fix. The Fix Lead will remove the Fix Team from the private repository.

### Retrospective

These steps should be completed after the Release Date. The retrospective process [should be blameless](https://landing.google.com/sre/book/chapters/postmortem-culture.html).

The Fix Lead will send a retrospective of the process to the [IronCore mailing list](#communication-channel) including details on everyone involved, the timeline of the process, links to relevant PRs that introduced the issue, if relevant, and any critiques of the response and release process. The Release Managers and Fix Team are also encouraged to send their own feedback on the process to the [IronCore mailing list](#communication-channel). Honest critique is the only way we are going to get good at this as a community.

### Communication Channel

The [private](#private-disclosure-process) or [public disclosure process](#public-disclosure-process) should be triggered exclusively by writing an e-mail to [ironcore-security@groups.linuxfoundation.org](mailto:ironcore-security@groups.linuxfoundation.org).

IronCore security announcements will be communicated by the Fix Lead sending an e-mail to the [IronCore mailing list](https://groups.linuxfoundation.org/g/ironcore-discussion) (reachable via [ironcore-discussion@groups.linuxfoundation.org](mailto:ironcore-discussion@groups.linuxfoundation.org)).

Public discussions about IronCore security announcements and retrospectives will primarily happen in the IronCore mailing list. Thus IronCore community members who are interested in participating in discussions related to the IronCore Security Release Process are encouraged to join the IronCore mailing list.

The members of the [IronCore Security Team](#ironcore-security-team) are subscribed to the private [IronCore Security mailing list](https://groups.linuxfoundation.org/g/ironcore-security) (reachable via [ironcore-security@groups.linuxfoundation.org](mailto:ironcore-security@groups.linuxfoundation.org)).

## Open-Source Steward

CRA stewardship: This project is supported under the Linux Foundation CRA stewardship framework, as described at https://www.linuxfoundation.org/security. Security vulnerabilities should be reported through the mechanisms described above, which we will coordinate with our CRA steward. For actively exploited vulnerabilities and severe incidents that may require CRA escalation, please use the project's emergency security reporting mechanisms as appropriate.

The LF CRA steward can be reached at [steward@linuxfoundation.org](mailto:steward@linuxfoundation.org).

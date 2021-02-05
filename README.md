# Fish in a Barrel Memory Safety Bounty Program

Welcome to the Fish in a Barrel Memory Safety Bounty Program, the first
security bounty that rewards people for contributing to security-critical open
source software in ways that use memory-safe programming languages to improve
security.

## Why a memory safety bounty?

There are already a great many security bounties out there, why another? Most
bounties focus on rewarding finders of individual bugs. At Fish in a Barrel, we
firmly believe that in order to achieve better computer security, we must focus
not on
[fixing bugs one at a time](https://www.youtube.com/watch?v=py2qmGbyhlw#t=23m36s),
but rather on addressing the underlying causes that lead to a great many
vulnerabilities. We've spent the last two years
[performing our own security research](https://bugs.chromium.org/p/oss-fuzz/issues/list?can=1&q=-Type%3DBuild-Failure+status%3AVerified+label%3AProj-imagemagick%2CProj-graphicsmagick%2CProj-gnutls%2CProj-libjpeg-turbo%2CProj-libssh%2CProj-libyaml%2CProj-mupdf%2CProj-systemd%2CProj-libgd%2CProj-libexif%2CProj-vorbis%2CProj-msgpack-c%2CProj-json-c%2CProj-libsodium%2CProj-poppler%2CProj-libgit2%2CProj-libtiff%2CProj-libcbor%2CProj-mercurial%2CProj-avahi&sort=-modified&colspec=ID+Type+Component+Status+Library+Reported+Owner+Summary+Modified&x=type&y=proj&mode=grid&cells=counts)
and [quantifying vulnerabilities](https://twitter.com/LazyFishBarrel) across
many projects. What we've seen time and time again is that [memory unsafe
programming languages are to blame](https://alexgaynor.net/2020/may/27/science-on-memory-unsafety-and-security/)
for an incredible share of vulnerabilities.

To that end, we've created a bounty that rewards people for addressing that
underlying cause of so many vulnerabilities. It is our hope that this will:

- Normalize the idea that security-critical projects should be looking for ways
  to migrate away from memory unsafe programming languages.
- Reduce the harm caused by memory unsafety by reducing the amount of it out
  there.
- Encourage and incentivize software engineers/security researchers with free
  time to help with these goals.

## Qualifying for a Bounty

To qualify for a bounty, you must make a contribution to a _security-critical_
open-source project which is written in a memory-_unsafe_ language, where the
change is merged into upstream, and where the change uses memory-_safe_
languages to reduce the harm of memory-unsafety.

Definitions of security-critical open source project and memory-safe (and
unsafe) languages as of the date this is posted are:

- **What makes a project security-critical?** It's very widely used, and it's
  used in contexts which are security sensitive.
- **What makes a language memory-unsafe?** Memory-unsafe programming
  languages include, but are not limited to C, C++, and Assembly.  
- **What makes a language memory-safe?** Memory-safe programming languages
  include, but are not limited to Rust, Go, and Swift.


**What types of contributions qualify?** At this moment we recognize two types of contributions:

- Add bindings making the library usable from **Rust or Swift** (e.g., adding
  official Swift bindings to an image parsing library)
- Partially (or completely) **migrate the project** to a memory-safe language
  (e.g., convert one of the decoder/encoders in an image parsing library to
  Rust)

**From time to time, and in our sole discretion, Fish in a Barrel may (i)
change these definitions, (ii) add or delete any other languages to the
memory-safe or memory-unsafe list, or (iii) add or delete the types of
contributions that qualify.** If you are planning on participating in this
Program, you should check this list from time to time.

All rewards will require that the contribution be merged into the upstream
project.

## Bounties

Rewards are $500 or $100, depending on the size and relevance of the
contribution, determined in the sole discretion of Fish in a Barrel. 

If you wish to donate your bounty to a qualified 501(c)(3) organization we will double the
size of the bounty. Any rewards that are unclaimed after 12 months from
notification that a reward is payable will be donated to a charity of our
choosing.

## How to apply for a bounty

Send a pull-request to this repository, adding a new entry to the
`submissions/` directory, in the form of
[`submissions/TEMPLATE.md`](submissions/TEMPLATE.md). Our team will review the
submission, and if it qualifies we will merge it and work with you to arrange
payment.

Applications for a bounty **_must_** be made within 12 months of the submission
being merged upstream.

## Help Wanted Board

Projects listed below are ones where the maintainers have explicitly indicated
they would be interested in contributions to embrace memory-safe languages. If
you're the maintainer of an open-source project, you can send a pull request to
add it here.

Current projects:

- [Contribute machinery for writing kernel modules in Rust to the Linux kernel](https://lkml.org/lkml/2020/7/9/952)

## Frequently Asked Questions

**Q: What if the maintainers won't accept the patch?**  
**A:** The Fish in a Barrel Memory Safety Bounty only rewards contributions
that are merged upstream. We strongly encourage people interested in pursuing a
bounty to work with, not against, open source maintainers and to behave
respectfully.

**Q: Can existing developers of projects claim a bounty for improvements to
it?**  
**A:** Yes.

**Q: Is there a way to be rewarded for finding or fixing a vulnerability?**  
**A:** No, this bounty is specific to migration away from memory unsafe
languages.

**Q: Can one get a reward from both Fish in a Barrel and another bounty program
(e.g., Google's Patch Rewards)?**  
**A:** Yes!

**Q: These bounties aren't very high.**  
**A:** That's not a question, but no, they're not. This is funded by security
engineers who are passionate about this subject, from their personal pockets,
not by a company.

**Q: Who decides what submissions qualify?**  
**A:** Our current panel consists of Alex Gaynor and Paul Kehrer.

## Legal Issues

1. **Sanctions Lists and Ability to Participate.** We are unable to issue rewards to individuals who are on sanctions lists, or who are in countries (_e.g._, Cuba, Iran, North Korea, Sudan, or Syria) on sanctions lists. In addition, there may be additional restrictions on your ability to enter depending upon your local law. Each submitter is responsible for determining whether local law allows you to participate.

2. **Taxes.** You are responsible for any tax implications depending on your country of residency and citizenship. In the event that any reward is for $600 or more (or any other amount determined under the U.S, Internal Revenue Code), if you are a U.S. resident, you will receive a U.S. Form 1099 reporting the reward to the U.S. Internal Revenue Service.

3. **Violation of Laws, Compromise of Third-Party Data/Projects, Waiver of Liability.** It is your responsibility to make sure that your work does not violate any local or U.S. law and does not disrupt or compromise any data or project that is not your own. You understand that Fish in a Barrel or any of their Indemnified Parties as defined in Section 4 below has no liability to you or any other person, except to the extent that is specifically set forth in the Program, for any work you submit to the Program, including the viability of the work.

4. **Liability and Indemnification.** Neither Fish in a Barrel, or any if its affiliates, principals, members, officers, directors, employees, representatives, agents, attorneys, or successors and assigns (the "Indemnified Parties") shall have any liability to the person or entity making a submission under the Program ("Submitter"), or to any other person, firm or organization, for any act or omission of itself or of any other person, firm or organization in the course of, or connected with, its obligations under this Agreement, unless the Indemnified Party's action or omission constitutes willful misfeasance, bad faith, gross negligence, or reckless disregard of the Indemnified Party's obligations and duties under the Program. Submitter agrees to indemnify and hold the Indemnified Parties harmless from and against any and all costs, losses, claims, damages, liabilities, expenses (including reasonable legal and other professional fees and disbursements), judgments, fines or settlements ("Losses") incurred by the Indemnified Party in the course of any threatened or actual litigation, arbitrations or administrative proceedings brought by a governmental agency or any other person pertaining to the work done under the Program for which a reward was received or otherwise relating to this Agreement, unless the Indemnified Party's action or omission constituted willful misfeasance, bad faith, gross negligence or reckless disregard of the Indemnified Party's obligations and duties under the Program. This provision shall survive and remain in full force and effect following the relationship between the Indemnified Parties and the Submitter, and the life of the Program.

5. **Changes to the Program.** Fish in a Barrel may change the terms of the Program as to projects not yet submitted to them from time to time and in their sole discretion. Any changes shall be reflected on the Program documents set forth at https://github.com/fishinabarrel/bounty.

6. **Binding Effect.** The Program Rules shall be binding upon and shall inure to the benefit of both Fish in a Barrel and the Submitter and their respective successors, assigns, heirs, and legal representatives, but no any rights hereunder may be assigned by the either Party without the written consent of the other party.

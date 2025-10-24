# Safety-Critical Rust Consortium RFCs

[Safety-Critical Rust Consortium RFCs]: #scrc-rfcs

The "RFC" (request for comments) process is intended to provide a consistent
and controlled path for changes to the Safety-Critical Rust Consortium and
its artifacts (such as new subcommittees, new initiatives) so that all
stakeholders can be confident about the direction of the Consortium.

Many changes, including bug fixes and documentation improvements can be
implemented and reviewed via the normal GitHub pull request workflow.

Some changes though are "substantial", and we ask that these be put through a
bit of a design process and produce a consensus among the Rust community and
the [subcommittee][subcommittees].


## Table of Contents
[Table of Contents]: #table-of-contents

  - [Opening](#scrc-rfcs)
  - [Table of Contents]
  - [When you need to follow this process]
  - [Subcommittee specific guidelines]
  - [Before creating an RFC]
  - [What the process is]
  - [The RFC life-cycle]
  - [Reviewing RFCs]
  - [Implementing an RFC]
  - [RFC Postponement]
  - [Decision making](#decision-making)
  - [Help this is all too informal!]
  - [Code of Conduct](#code-of-conduct)
  - [Contributing]
  - [Licenses]
  - [Other Policies]


## When you need to follow this process
[When you need to follow this process]: #when-you-need-to-follow-this-process

You need to follow this process if you intend to make "substantial" changes to
artifacts produced by the Consortium, subcommittee charters or the RFC process itself.
What constitutes a "substantial" change is evolving based on community norms
and varies depending on what part of the ecosystem you are proposing to change,
but may include the following.

  - Proposals which result in substantial changes to the artifacts the
    Consortium produces (such as the [Safety-Critical Rust Coding Guidelines]
    [safety-critical-rust-coding-guidelines]).
  - Creation / dissolution of a [subcommittee].

Some changes do not require an RFC:

  - Typical "line of business"-style work, such as adding a new coding guideline
    or small reworkings of process within contributions to the coding guidelines
    for the Safety-Critical Rust Coding Guidelines
  - Rephrasing, reorganizing, refactoring, or otherwise "changing shape does
    not change meaning".
  - Additions that strictly improve objective, numerical quality criteria
    (warning removal, speedup, better platform coverage, more parallelism, trap
    more errors, etc.)
  - Additions only likely to be _noticed by_ other contributors to artifacts,
    invisible to users of artifacts.

If you submit a pull request to implement a new feature without going through
the RFC process, it may be closed with a polite request to submit an RFC first.


### Subcommittee specific guidelines
[Subcommittee specific guidelines]: #subcommittee-specific-guidelines

Currently there are no subcommittee specific guidelines.


## Before creating an RFC
[Before creating an RFC]: #before-creating-an-rfc

A hastily-proposed RFC can hurt its chances of acceptance. Low quality
proposals, proposals for previously-rejected features, or those that don't fit
into the near-term roadmap, may be quickly rejected, which can be demotivating
for the unprepared contributor. Laying some groundwork ahead of the RFC can
make the process smoother.

Although there is no single way to prepare for submitting an RFC, it is
generally a good idea to pursue feedback from other project developers
beforehand, to ascertain that the RFC may be desirable; having a consistent
impact on the project requires concerted effort toward consensus-building.

The most common preparations for writing and submitting an RFC include talking
the idea over on our [official Zulip channel] and occasionally posting
"pre-RFCs" on the Zulip channel. You may file issues on this repo for discussion,
but these are not actively looked at by the subcommittees.

As a rule of thumb, receiving encouraging feedback from long-standing project
developers, and particularly members of the relevant [subcommittee] is a good
indication that the RFC is worth pursuing.


## What the process is
[What the process is]: #what-the-process-is

In short, to get a major change made added to the Safety-Critical Rust
Consortium or its artifacts, one must first get the RFC merged into the
RFC repository as a markdown file. At that point the RFC is "active"
and may be implemented with the goal of eventual inclusion.

  - Fork the RFC repo [RFC repository]
  - Copy `0000-template.md` to `text/0000-my-feature.md` (where "my-feature" is
    descriptive). Don't assign an RFC number yet; This is going to be the PR
    number and we'll rename the file accordingly if the RFC is accepted.
  - Fill in the RFC. Put care into the details: RFCs that do not present
    convincing motivation, demonstrate lack of understanding of the design's
    impact, or are disingenuous about the drawbacks or alternatives tend to
    be poorly-received.
  - Submit a pull request. As a pull request the RFC will receive design
    feedback from the larger community, and the author should be prepared to
    revise it in response.
  - Now that your RFC has an open pull request, use the issue number of the PR
    to rename the file: update your `0000-` prefix to that number. Also
    update the "RFC PR" link at the top of the file.
  - Each pull request will be labeled with the most relevant [subcommittee], which
    will lead to its being triaged by that subcommittee in a future meeting and assigned
    to a member of the subcommittee.
  - Build consensus and integrate feedback. RFCs that have broad support are
    much more likely to make progress than those that don't receive any
    comments. Feel free to reach out to the RFC assignee in particular to get
    help identifying stakeholders and obstacles.
  - The subcommittee will discuss the RFC pull request, as much as possible in the
    comment thread of the pull request itself. Offline discussion will be
    summarized on the pull request comment thread.
  - RFCs rarely go through this process unchanged, especially as alternatives
    and drawbacks are shown. You can make edits, big and small, to the RFC to
    clarify or change the design, but make changes as new commits to the pull
    request, and leave a comment on the pull request explaining your changes.
    **Specifically, do not squash or rebase commits after they are visible on
    the pull request.**
  - At some point, a member of the subcommittee will propose a "motion for final
    comment period" (FCP), along with a *disposition* for the RFC (merge, close,
    or postpone).
    - This step is taken when enough of the tradeoffs have been discussed that
      the subcommittee is in a position to make a decision. That does not require
      consensus amongst all participants in the RFC thread (which is usually
      impossible). However, the argument supporting the disposition on the RFC
      needs to have already been clearly articulated, and there should not be a
      strong consensus *against* that position outside of the subcommittee.
      Subcommittee members use their best judgment in taking this step, and the
      FCP itself ensures there is ample time and notification for stakeholders
      to push back if it is made prematurely.
    - For RFCs with lengthy discussion, the motion to FCP is usually preceded by
      a *summary comment* trying to lay out the current state of the discussion
      and major tradeoffs/points of disagreement.
    - Before actually entering FCP, *all* members of the subcommittee must sign off;
      this is often the point at which many subcommittee members first review the
      RFC in full depth.
  - The FCP lasts ten calendar days, so that it is open for at least 5 business
    days. It is also advertised widely, e.g. in the Consortium mailing list. This
    way all stakeholders have a chance to lodge any final objections before a decision
    is reached.
  - In most cases, the FCP period is quiet, and the RFC is either merged or
    closed. However, sometimes substantial new arguments or ideas are raised,
    the FCP is canceled, and the RFC goes back into development mode.

## The RFC life-cycle
[The RFC life-cycle]: #the-rfc-life-cycle

Once an RFC becomes "active" then authors may implement it and submit the
feature as a pull request to the relevant Consortium repo. Being "active" is not
a rubber stamp, and in particular still does not mean the feature will ultimately
be merged; it does mean that in principle all the major stakeholders have agreed
to the feature and are amenable to merging it.

Furthermore, the fact that a given RFC has been accepted and is "active"
implies nothing about what priority is assigned to its implementation, nor does
it imply anything about whether a developer or writer has been assigned the task of
implementing the feature. While it is not *necessary* that the author of the
RFC also write the implementation, it is by far the most effective way to see
an RFC through to completion: authors should not expect that other project
developers or writers will take on responsibility for implementing their accepted
feature.

Modifications to "active" RFCs can be done in follow-up pull requests. We
strive to write each RFC in a manner that it will reflect the final design of
the feature; but the nature of the process means that we cannot expect every
merged RFC to actually reflect what the end result will be at the time of the
next major release of an impacted Consortium artifact.

In general, once accepted, RFCs should not be substantially changed. Only very
minor changes should be submitted as amendments. More substantial changes
should be new RFCs, with a note added to the original RFC. Exactly what counts
as a "very minor change" is up to the subcommittee to decide; check
[Subcommittee specific guidelines] for more details.


## Reviewing RFCs
[Reviewing RFCs]: #reviewing-rfcs

While the RFC pull request is up, the subcommittee may schedule meetings with the
author and/or relevant stakeholders to discuss the issues in greater detail,
and in some cases the topic may be discussed at a subcommittee meeting. In either
case a summary from the meeting will be posted back to the RFC pull request.

A subcommittee makes final decisions about RFCs after the benefits and drawbacks
are well understood. These decisions can be made at any time, but the subcommittee
will regularly issue decisions. When a decision is made, the RFC pull request
will either be merged or closed. In either case, if the reasoning is not clear
from the discussion in thread, the subcommittee will add a comment describing the
rationale for the decision.


## Implementing an RFC
[Implementing an RFC]: #implementing-an-rfc

Some accepted RFCs represent vital features that need to be implemented right
away. Other accepted RFCs can represent features that can wait until some
arbitrary developer or writer feels like doing the work. Every accepted RFC has an
associated issue tracking its implementation in the [RFC repository]; thus that
associated issue can be assigned a priority via the triage process that the
subcommittee uses for all issues in the Rust repository.

The author of an RFC is not obligated to implement it. Of course, the RFC
author (like any other developer or writer) is welcome to post an implementation
for review after the RFC has been accepted.

If you are interested in working on the implementation for an "active" RFC, but
cannot determine if someone else is already working on it, feel free to ask
(e.g. by leaving a comment on the associated issue).


## RFC Postponement
[RFC Postponement]: #rfc-postponement

Some RFC pull requests are tagged with the "postponed" label when they are
closed (as part of the rejection process). An RFC closed with "postponed" is
marked as such because we want neither to think about evaluating the proposal
nor about implementing the described feature until some time in the future, and
we believe that we can afford to wait until then to do so. Historically,
"postponed" was used to postpone features until after 1.0. Postponed pull
requests may be re-opened when the time is right. We don't have any formal
process for that, you should ask members of the relevant subcommittee.

Usually an RFC pull request marked as "postponed" has already passed an
informal first round of evaluation, namely the round of "do we think we would
ever possibly consider making this change, as outlined in the RFC pull request,
or some semi-obvious variation of it." (When the answer to the latter question
is "no", then the appropriate response is to close the RFC, not postpone it.)

## Decision-making
[Decision-making]: #decision-making

### Consensus

In a nutshell the premise  of [consensus decision-making][consensus] is that
a successful outcome is not where one side of a debate has "won", but rather
where concerns from *all* sides have been addressed in some way. **This
emphatically does not entail design by committee, nor compromised design**.
Rather, it's a recognition that

> ... every design or implementation choice carries a trade-off and numerous
> costs. There is seldom a right answer.

Breakthrough designs sometimes end up changing the playing field by eliminating
tradeoffs altogether, but more often difficult decisions have to be made. **The
key is to have a clear vision and set of values and priorities**, which is the
leadership team's responsibility to set and communicate, and the subcommittee's
responsibility to act upon.

Whenever possible, we seek to reach consensus through discussion and design
revision. Concretely, the steps are:

* Initial RFC proposed, with initial analysis of tradeoffs.
* Comments reveal additional drawbacks, problems, or tradeoffs.
* RFC revised to address comments, often by improving the design.
* Repeat above until "major objections" are fully addressed, or it's clear that
  there is a fundamental choice to be made.

Consensus is reached when most people are left with only "minor" objections,
i.e., while they might choose the tradeoffs slightly differently they do not
feel a strong need to *actively block* the RFC from progressing.

One important question is: consensus among which people, exactly? Of course, the
broader the consensus, the better. But at the very least, **consensus within the
members of the subcommittee should be the norm for most decisions.** If the leadership
team has done its job of communicating the values and priorities, it should be
possible to fit the debate about the RFC into that framework and reach a fairly
clear outcome.

Each RFC has a shepherd drawn from the relevant subcommittee. The shepherd is
responsible for driving the consensus process -- working with both the RFC
author and the broader community to dig out problems, alternatives, and improved
design, always working to reach broader consensus.

[consensus]: http://en.wikipedia.org/wiki/Consensus_decision-making

### Lack of consensus
[Lack of consensus]: #lack-of-consensus

In some cases, though, consensus cannot be reached. These cases tend to split
into two very different camps:

* "Trivial" reasons, e.g., there is not widespread agreement about naming, but
  there is consensus about the substance.

* "Deep" reasons, e.g., the design fundamentally improves one set of concerns at
  the expense of another, and people on both sides feel strongly about it.

In either case, an alternative form of decision-making is needed.

* For the "trivial" case, usually either the RFC shepherd or subcommittee chair will
  make an executive decision.

* For the "deep" case, there are a few stages this can progress through.
  If resolved at any stage, no further stages need be visited for that "deep" case
  item.
  1. A subcommittee member raises what they believe to be a blocking concern on the
     RFC. See [Blocking concern process] for the details. If the blocking concern
     cannot be resolved through that process, proceed to the next stage.
  2. The subcommitee chair is empowered to make a final decision, but should consult
     with the the leadership team before doing so.

The decision on which camp a decision falls into is the responsiblity of the
subcommittee chair, although they should consult with the leadership team if
there's doubt raised on the RFC.

#### Blocking concern process
[Blocking concern process]: #blocking-concern-process

We follow the below process for a blocking concern:

  1. A subcommittee member raises what they believe to be a blocking concern on the
     RFC. Included with their blocking concern comment they must include a
     reasonable length piece of writing outlining concerns and alternatives.
  2. The RFC shepherd is responsible for working with the author and the
     subcommittee to attempt to drive to resolution during the ten day period
     from blocking concern being opened.
  3. If working together, the subcommittee member that raised the blocking concern,
     the author, and the remainder of the subcommittee are able to resolve the
     concern, the RFC is updated to reflect the chosen resolution by the author.
     Done.
  4. If working together, the subcommittee member that raised the blocking concern,
     the author, and the remainder of the subcommittee are **unable** to resolve
     the concern, the blocking concern process is deemed to not have succeeded.
     Return to [Lack of consensus] for further stages.


### Help this is all too informal!
[Help this is all too informal!]: #help-this-is-all-too-informal

The process is intended to be as lightweight as reasonable for the present
circumstances. As usual, we are trying to let the process be driven by
consensus and community norms, not impose more structure than necessary.


## [Code of Conduct][code-of-conduct]


The [Rust Foundation][rust-foundation] has adopted a Code of Conduct that we
expect project participants to adhere to. Please read [the full
text][code-of-conduct] so that you can understand what actions will and will not
be tolerated.


## Contributing
[Contributing]: #contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).


## Licenses
[Licenses]: #licenses

Rust is primarily distributed under the terms of both the MIT license and the
Apache License (Version 2.0), with documentation portions covered by the
Creative Commons Attribution 4.0 International license.

See [LICENSE-APACHE](LICENSE-APACHE), [LICENSE-MIT](LICENSE-MIT),
[LICENSE-documentation](LICENSE-documentation), and
[COPYRIGHT](COPYRIGHT) for details.

You can also read more under the Foundation's [intellectual property
policy][ip-policy].


## Other Policies
[Other Policies]: #other-policies

You can read about other Rust Foundation policies on the [Rust Foundation
website][policies].

[code-of-conduct]: https://rustfoundation.org/policy/code-of-conduct/
[ip-policy]: https://rustfoundation.org/policy/intellectual-property-policy/
[media-guide and trademark]: https://rustfoundation.org/policy/trademark-policy/
[policies]: https://rustfoundation.org/policies-resources/
[rust-foundation]: https://rustfoundation.org/
[subcommittee]: SUBCOMMITTEES.md
[safety-critical-rust-coding-guidelines]: https://github.com/rustfoundation/safety-critical-rust-coding-guidelines
[official Zulip channel]: https://rust-lang.zulipchat.com/#narrow/channel/445688-safety-critical-consortium
[RFC repository]: https://github.com/rustfoundation/safety-critical-rust-consortium-rfcs

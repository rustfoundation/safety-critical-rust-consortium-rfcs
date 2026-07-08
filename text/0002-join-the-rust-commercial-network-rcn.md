- Change Name: join-the-rust-commercial-network-rcn
- Start Date: 2026-06-22
- RFC PR: [safety-critical-rust-consortium-rfcs/rfcs#0002](https://github.com/Safety-Critical-Rust-Consortium/safety-critical-rust-consortium-rfcs/pull/8)
- Issue: [safety-critical-rust-consortium-rfcs/issues#0007](https://github.com/Safety-Critical-Rust-Consortium/safety-critical-rust-consortium-rfcs/issues/7)

# Summary
[summary]: #summary

The [Safety-Critical Rust Consortium][scrc-repo] (SCRC) was [announced][scrc-announcement] in June 2024 as a rallying point for those organizations and industries which seek to use Rust in a safety-critical ecosystem to band together and solve problems for themselves. The [Rust Commercial Network][rcn-repo] (RCN) was announced in May of 2026 as a means to start similarly grouped initiatives, working groups, and consortia. SCRC leadership worked with drafters of the RCN charter to ensure that language was placed in it which would allow for the SCRC to continue to function as it always has, with the option to part ways if interests no longer remain aligned. The RCN seems to be a natural fit for the SCRC and allows us broader exposure to other activities happening between the Rust Project, the Rust Foundation, and industry, so we propose for the SCRC to join the RCN.

# Motivation
[motivation]: #motivation

The Rust Commercial Network seeks to operate outside of the purview of the Rust Project, but in close collaboration with the Project and the Rust Foundation for the benefit of groups of commercial users that have shared interests.

In a nutshell, the [RCN README][rcn-overview] gives our main motivation to join as the Safety-Critical Rust Consortium:

> Where Rust users, businesses, and communities work together to make Rust easier to adopt and maintain.
> 
> The Rust Commercial Network (RCN) is a Rust Foundation group for people and organizations using Rust in professional settings. Members compare notes on adoption blockers, improve Rust supply chain health, and support the basic tooling, libraries, and maintenance work that make Rust dependable in production.

For example, there's been talk of creating an [interest group for Rust toolchain/WebAssembly][rcn-wasm-interest-group] and a [standard async executor abstraction][rcn-std-async-executor-abstraction]. We are aware of some work to use WebAssembly System Interface (WASI) + Component Model + WebAssembly Interface Types (WIT) for interoperability between C++ and Rust. We're also aware of a desire for a safety-certifiable async executor.

There's also been a desire raised by some within the Safety-Critical Rust Consortium for an initiative focused on making Rust easier to work with embedded hardware targets.

Given the forming nucleus of Rust Project, Rust Foundation, and industry it seems valuable for the SCRC to join the RCN to remain better informed about and a part of these and future initiatives.

# Guide-level explanation
[guide-level-explanation]: #guide-level-explanation

The [Safety-Critical Rust Consortium][scrc-repo] (SCRC) exists under the auspices of the [Rust Commercial Network][rcn-repo] (RCN) to better facilitate information sharing and the SCRC's input on topics of interest for safety-critical Rust users.

The Rust Commercial Network is [described as][rcn-overview]:

> Where Rust users, businesses, and communities work together to make Rust easier to adopt and maintain.
> 
> The Rust Commercial Network (RCN) is a Rust Foundation group for people and organizations using Rust in professional settings. Members compare notes on adoption blockers, improve Rust supply chain health, and support the basic tooling, libraries, and maintenance work that make Rust dependable in production.

The [Safety-Critical Rust Consortium][scrc-repo] is a Consortium by and for its members which seeks to:
- close technical gaps
- close mindshare gaps

to better the ability to use the Rust programming language in safety-critical systems development (e.g. Automotive, Medical Devices).

The Rust Commercial Network is a natural hub for SCRC members to be able to interact with other initiatives, working groups, and consortia of interest to safety-critical users.

For a concrete example, we are aware that in the [Eclipse S-CORE Project][eclipse-s-core-org] in the Eclipse SDV WG, there is the [Kyron][kyron-repo] project which seeks to make an async runtime / executor for Rust that could be safety-certified for use in safety-critical systems. There is shared membership between the Safety-Critical Rust Consortium and the Eclipse S-CORE Project and if we were involved with the Rust Commercial Network we could have our voice heard in discussions about [stanardizing abstractions over Rust's async executor concepts][rcn-std-async-executor-abstraction].

Another example is the significant personal overlap with the long established Rust groups at AUTOSAR and SAE. Several active members of the SCRC have already been cooperating towards Rust industry adoption and standardization for years in these other groups and thus established a communication which can benefit the RCN.

The membership of the SCRC to the RCN also facillitates the potential creation of new initiatives. For example, we're aware that there's a desire to start something of an Embedded Rust Initiative or similar in the RCN. The SCRC's presence in the RCN makes it easier to, when learning of these new ideas, spin them up in a lightweight manner as initiatives in the RCN.

# Reference-level explanation
[reference-level-explanation]: #reference-level-explanation

The Safety-Critical Rust Consortium (SCRC) being a member organization of the Rust Commercial Network (RCN) does not entail any changes in day-to-day workings, nor does this membership prevent the SCRC from parting ways with the RCN should interests diverge.

## Governance of the Safety-Critical Rust Consortium remains the same

As written under [Operations][rcn-initiative-operations], the SCRC continues to run just as it has been, with our own rules and regulations:

> Each initiative defines and administers its own organizational form, membership criteria, tiers, and processes. Membership in an RCN initiative does not necessarily require RCN membership.

## Existing initatives, like the Safety-Critical Rust Consortium run as they are

As written under [Existing Initiatives][rcn-initiative-existing-initiatives], the SCRC continues to operate just as it has been:

> Initiatives (consortiums, interest groups, or working groups) that predate the RCN or that maintain their own governance structures retain full authority over their technical outputs, publication decisions, and operational processes. The SC may not condition continued RCN affiliation on changes to an initiative's existing governance, scope, processes, or external relationships, including direct relationships with the Rust Project, standards bodies, or other organizations.

## Withdrawal of the Safety-Critical Rust Consortium from the Rust Commercial Network is straightforward, if needed

As written under [Withdrawal][rcn-initiative-withdrawal], the SCRC may at any time request to withdraw from the RCN:

> An RCN-affiliated initiative may withdraw from the RCN at any time by written notice from that initiative's leadership to the RCN Steering Committee. Upon withdrawal, the initiative retains its existing governance structures, membership, repositories, branding, and intellectual property. Withdrawal does not require SC approval. Former RCN-affiliated initiatives are welcome to seek re-affiliation in the future.

## The Safety-Critical Rust Consortium membership, itself, does not grant Rust Commercial Network voting rights

As written in [RCN Initiative Member][rcn-membership-initiative-member]:

> An RCN Initiative Member is an individual who is an active member of an RCN-affiliated consortium, working group, interest group, or other RCN initiative as determined by that initiative's own membership criteria and processes. RCN Initiative Members are recognized as RCN participants and may attend RCN meetings, contribute to discussions, and access RCN communication channels.
> 
RCN Initiative Members may vote on RCN matters that directly affect the RCN initiative in which they hold membership, including but not limited to: policies governing RCN initiative operations, changes to the relationship between the RCN and its consortiums, working groups, or interest groups, and amendments to this charter that alter the rights or obligations of RCN initiatives.
> 
> RCN Initiative Members do not vote in RCN-wide elections such as Steering Committee seats unless they independently qualify under another RCN member definition.
> 
> For the purposes of determining good standing, RCN Initiative Members must meet the membership requirements of their respective RCN initiative. Attendance at RCN-level meetings is not required for RCN Initiative Members to maintain good standing.

Or to put it simply: being a member of the SCRC does not grant RCN-wide election voting rights. For that, you must qualify as another type of member under the RCN which does have voting rights. For more details on those types of membership see the [RCN membership page][rcn-membership].

# Drawbacks
[drawbacks]: #drawbacks

There are not many clear drawbacks for the Safety-Critical Rust Consortium to join the Rust Commercial Network. Joining is not "one-way door" and the SCRC may withdraw at any time on SCRC leadership request.

To our minds, the only thing lost here is any potential time spent on withdrawal processes, should that ever need to occur.

# Rationale and alternatives
[rationale-and-alternatives]: #rationale-and-alternatives

## The Safety-Critical Rust Consortium remains independent of the Rust Commercial Network

One potential alternative is for the SCRC to remain independent of the RCN.

The SCRC is already an initiative that was kicked off by the Rust Foundation and uses the RF's infrastructure for GitHub, its website domain (https://arewesafetycriticalyet.org/) and so on.

Lacking any notice of withdrawal of said support, the SCRC remaining independent is a real option.

However, given the initiatives which are already starting in the RCN that the SCRC would like to have input on, remaining independent would serve only to hinder efforts to work together effectively.

## The Safety-Critical Rust Consortium remains independent of the Rust Commercial Network

Another potential alternative is for the SCRC to ask to join the RCN on a trial basis to see if anything of note changes.

Currently such a mechanism does not exist in the RCN, but it may be possible to request its creation.

However, given that there is a withdrawal mechanism for any existing initiative from the RCN, this feels like being prematurely pessimistic.

# Prior art
[prior-art]: #prior-art

The [Eclipse Software Defined Vehicle Working Group][eclipse-sdv-wg-website] functions in a similar manner to the Rust Commercial Network:
- A project proposes to go under the purview of the Eclipse SDV WG
- The project is reviewed by the Technical Advisory Committee with a recommendation given to the Steering Committee
- The Steering Committee holds a vote on putting the project under the purview of the Eclipse SDV WG

Beyond that point, in the Eclipse SDV WG, the Steering Committee and Technical Advisory Committee do not have any direct hand in the day-to-day operations of any Eclipse Project.

In that way, the Rust Commercial Network and its Steering Committee function [similarly][rcn-initiative-existing-initiatives]:

> Initiatives (consortiums, interest groups, or working groups) that predate the RCN or that maintain their own governance structures retain full authority over their technical outputs, publication decisions, and operational processes. The SC may not condition continued RCN affiliation on changes to an initiative's existing governance, scope, processes, or external relationships, including direct relationships with the Rust Project, standards bodies, or other organizations.

The Eclipse Foundation model of Working Groups and Projects has been run successfully for many years.

# Unresolved questions
[unresolved-questions]: #unresolved-questions

No unresolved questions.

# Future possibilities
[future-possibilities]: #future-possibilities

We might consider starting other initiatives in the Rust Commercial Network if needs arise which do not fully fit within the mandate of the Safety-Critical Rust Consortium and we can find other partners to work on them with.

[scrc-repo]: https://github.com/Safety-Critical-Rust-Consortium/safety-critical-rust-consortium
[scrc-announcement]: https://rustfoundation.org/media/announcing-the-safety-critical-rust-consortium/
[rcn-repo]: https://github.com/Rust-Commercial-Network/rcn
[rcn-overview]: https://github.com/Rust-Commercial-Network/rcn#rust-commercial-network-rcn
[rcn-wasm-interest-group]: https://rust-lang.zulipchat.com/#narrow/channel/594428-commercial-network/topic/Rust.20toolchain.2F.20WebAssembly.20interest.20group/with/604294002
[rcn-std-async-executor-abstraction]: https://rust-lang.zulipchat.com/#narrow/channel/594428-commercial-network/topic/Standard.20async.20executor.20abstraction/with/601550600
[eclipse-s-core-org]: https://github.com/eclipse-score
[kyron-repo]: https://github.com/eclipse-score/kyron
[rcn-initiative-operations]: https://github.com/Rust-Commercial-Network/rcn/blob/main/docs/initiatives.md#operations
[rcn-initiative-withdrawal]: https://github.com/Rust-Commercial-Network/rcn/blob/main/docs/initiatives.md#withdrawal
[rcn-initiative-existing-initiative]: https://github.com/Rust-Commercial-Network/rcn/blob/main/docs/initiatives.md#existing-initiatives
[rcn-membership-initiative-member]: https://github.com/Rust-Commercial-Network/rcn/blob/main/docs/membership.md#rcn-initiative-member
[rcn-membership]: https://github.com/Rust-Commercial-Network/rcn/blob/main/docs/membership.md
[eclipse-sdv-wg-website]: https://eclipsesdv.org/

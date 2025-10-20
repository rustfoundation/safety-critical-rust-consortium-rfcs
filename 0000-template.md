- Feature Name: (fill me in with a unique ident, `my_awesome_feature`)
- Start Date: (fill me in with today's date, YYYY-MM-DD)
- RFC PR: [rust-lang/rfcs#0000](https://github.com/rustfoundation/safety-critical-rust-consortium-rfcs/pull/0000)
- Rust Issue: [rust-lang/rust#0000](https://github.com/rustfoundation/safety-critical-rust-consortium-rfcs/issues/0000)

# Summary
[summary]: #summary

One paragraph explanation of the feature.

# Motivation
[motivation]: #motivation

Any changes to Safety-Critical Rust Consortium artifacts should focus on solving a problem that users of Rust are having related to safety-critical domain usage.
This section should explain this problem in detail, including necessary background.

It should also contain several specific use cases where this feature can help a user, and explain how it helps.
This can then be used to guide the design of the feature or artifact.

This section is one of the most important sections of any RFC, and can be lengthy.

# Guide-level explanation
[guide-level-explanation]: #guide-level-explanation

Explain the proposal as if it was already included in the Consortium and you were teaching it to another safety-critical Rust programmer or functional safety engineer. That generally means:

- Introducing new named concepts.
- Explaining the feature largely in terms of examples.
- Explaining how safety-critical users should *think* about the feature, and how it should impact the way they use Rust. It should explain the impact as concretely as possible.
- If applicable, provide sample error messages, deprecation warnings, or migration guidance.
- If applicable, describe the differences between teaching this to existing safety-critical Rust programmers and new safety-critical Rust programmers.
- Discuss how this impacts the ability to read, understand, and maintain safety-critical Rust code. Code is read and modified far more often than written; will the proposed feature make code easier to maintain?

For implementation-oriented RFCs (e.g. operational details around Safety-Critical Rust Coding Guidelines), this section should focus on how contributors should think about the change, and give examples of its concrete impact. For policy RFCs, this section should provide an example-driven introduction to the policy, and explain its impact in concrete terms.

# Reference-level explanation
[reference-level-explanation]: #reference-level-explanation

This is the technical portion of the RFC. Explain the design in sufficient detail that:

- Its interaction with other features and artifacts is clear.
- It is reasonably clear how the feature or artifact would be implemented.
- Corner cases are dissected by example.

The section should return to the examples given in the previous section, and explain more fully how the detailed proposal makes those examples work.

# Drawbacks
[drawbacks]: #drawbacks

Why should we *not* do this?

# Rationale and alternatives
[rationale-and-alternatives]: #rationale-and-alternatives

- Why is this design the best in the space of possible designs?
- What other designs have been considered and what is the rationale for not choosing them?
- What is the impact of not doing this?
- Does the proposed change make Rust code easier or harder to read, understand, and maintain?
- Does the proposed change make Rust a stronger or weaker fit for usage in safety-critical domains?

# Prior art
[prior-art]: #prior-art

Discuss prior art, both the good and the bad, in relation to this proposal.
A few examples of what this can include are:

- For artifact proposals: Is this artifact present in other programming languages commonly used for safety-critical and what experience have their community had?
- For community proposals: Is this done by some other community and what were their experiences with it?
- For other subcommittees: What lessons can we learn from what other communities have done here?
- Papers: Are there any published papers or great posts that discuss this? If you have some relevant papers to refer to, this can serve as a more detailed theoretical background.

This section is intended to encourage you as an author to think about the lessons from other languages, provide readers of your RFC with a fuller picture.
If there is no prior art, that is fine - your ideas are interesting to us whether they are brand new or if it is an adaptation from other languages.

Note that while precedent set by other languages and safety-critical communities is some motivation, it does not on its own motivate an RFC.
Please also take into consideration that the Safety-Critical Rust Consortium sometimes intentionally diverges from norms established in other communities related to safety-critical systems.

# Unresolved questions
[unresolved-questions]: #unresolved-questions

- What parts of the design do you expect to resolve through the RFC process before this gets merged?
- What parts of the design do you expect to resolve through the implementation of this feature before stabilization?
- What related issues do you consider out of scope for this RFC that could be addressed in the future independently of the solution that comes out of this RFC?

# Future possibilities
[future-possibilities]: #future-possibilities

Think about what the natural extension and evolution of your proposal would
be and how it would affect the aim of using Rust in a safety-critical context
as a whole in a holistic way. Try to use this section as a tool to more fully
consider all possible interactions with the Consortium and its artifacts in
your proposal. Also consider how this all fits into the roadmap for the Consortium
and of the relevant subcommittees.

This is also a good place to "dump ideas", if they are out of scope for the
RFC you are writing but otherwise related.

If you have tried and cannot think of any future possibilities,
you may simply state that you cannot think of anything.

Note that having something written down in the future-possibilities section
is not a reason to accept the current or a future RFC; such notes should be
in the section on motivation or rationale in this or subsequent RFCs.
The section merely provides additional information.

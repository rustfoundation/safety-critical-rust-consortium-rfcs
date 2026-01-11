- Change Name: `consortium_operations_baseline`
- Start Date: 2026-01-10
- RFC PR: [safety-critical-rust-consortium-rfcs/rfcs#0001](https://github.com/rustfoundation/safety-critical-rust-consortium-rfcs/pull/4)
- Issue: [safety-critical-rust-consortium-rfcs/issues#0005](https://github.com/rustfoundation/safety-critical-rust-consortium-rfcs/issues/5)

# Summary
[summary]: #summary

This RFC documents the current operational structure of the Safety-Critical Rust Consortium (SCRC), including its governance, membership model, subcommittee organization, and decision-making processes. The purpose is to establish a baseline understanding of how the consortium functions today, enabling future RFCs to propose targeted improvements with clear context.

# Motivation
[motivation]: #motivation

The Safety-Critical Rust Consortium has grown organically since its founding in June 2024 and first meeting in September 2024, reaching approximately 200 members across automotive, aerospace, medical, industrial, and other safety-critical domains. During this growth, operational practices have emerged through consensus and necessity rather than explicit documentation.

This creates several challenges:

1. **Onboarding difficulty**: New members lack a comprehensive reference for understanding how the consortium operates, what roles exist, and how to participate effectively.

2. **Inconsistent expectations**: The distinction between "observer" and "producer" roles exists in principle but lacks clear definition, leading to uncertainty about participation expectations.

3. **Non-uniform subcommittee structures**: Each subcommittee has developed its own practices (task forces, core member roles, etc.) without a common framework, making cross-subcommittee participation harder to navigate.

4. **Foundation for improvement**: Without documenting the current state, proposals for operational improvements lack baseline context, making it difficult to evaluate whether changes represent genuine improvements.

This RFC addresses these challenges by providing a single source of truth for current consortium operations. Future RFCs can reference this document when proposing changes, making the evolution of consortium practices traceable and deliberate.

**Use cases this documentation enables:**

- A new member can read this RFC to understand membership expectations and find where to participate
- Subcommittee leads can reference common terminology when describing roles
- Future RFC authors can clearly articulate what they're proposing to change
- External parties (standards bodies, the Rust Project, etc.) can understand how the consortium is organized

# Guide-level explanation
[guide-level-explanation]: #guide-level-explanation

## What is the Safety-Critical Rust Consortium?

The Safety-Critical Rust Consortium is a Rust Foundation initiative that supports the responsible use of the Rust programming language in safety-critical software, i.e. systems whose failure can impact human life or cause severe environmental or property harm.

The consortium brings together practitioners from across safety-critical industries to collaborate on shared challenges: developing coding guidelines, identifying and cataloging tooling, engaging with standards bodies, and building bridges to the Rust Project.

## How is the Consortium Organized?

The consortium operates at two levels:

### Consortium Level

At the top level, the consortium has:

- **Rust Foundation Sponsor**: Joel Marcey (Director of Technology at the Rust Foundation) manages logistics and provides organizational support
- **Consortium Lead**: Pete LeVasseur coordinates activities across subcommittees and represents the consortium externally
- **In-person meetings**: Twice yearly at major Rust conferences (e.g., RustConf, RustWeek)

### Subcommittee Level

The consortium has three subcommittees, each focused on a specific domain:

1. **Coding Guidelines Subcommittee** (led by Pete LeVasseur)
   - Develops community-vetted coding guidelines for Rust in safety-critical applications
   - Meets weekly rotating globally across time zones

2. **Liaison Subcommittee** (led by Alex Celeste)
   - Engages with external organizations: standards bodies, the Rust Project, industry groups
   - Meets as-needed

3. **Tooling Subcommittee** (led by Alexandru Radovici)
   - Catalogs and evaluates tools for safety-critical Rust development
   - Identifies gaps in tooling and advocates for improvements
   - Meets biweekly

## How Do I Participate?

### Joining the Consortium

Membership is intentionally low-barrier. To join:

1. File a [membership application issue](https://github.com/rustfoundation/safety-critical-rust-consortium/issues/new?assignees=joelmarcey&labels=membership%2Cstatus%3A+needs+review&projects=&template=membership.yml) on GitHub
2. Provide your name, email, and optionally your company affiliation

Membership grants access to:
- The consortium mailing list
- Occasional virtual all-hands meetings
- Invitations to in-person meetings

### Joining Subcommittees

Concurrently with submitting to join the consortium, you can apply to subcommittees by filing a [subcommittee application issue](https://github.com/rustfoundation/safety-critical-rust-consortium/issues/new?assignees=joelmarcey%2C+PLeVasseur%2C+alexandruradovici&labels=subcommittee+application&projects=&template=subcommittees.yml&title=Subcommittee+Join+Request+for+%5BNAME%5D).

Subcommittee membership adds:
- Invitations to that subcommittee's meetings
- Easier ability to coordinate on subcommittee-specific discussions and work items

### Observer vs. Producer Roles

The consortium distinguishes between two participation modes:

- **Observer**: Primarily follows discussions, provides feedback, and stays informed. Observers participate in meetings and may contribute occasionally.
- **Producer**: Actively contributes to artifacts, takes on work items, and participates in reviews.

This distinction is informal. In other words, members self-select their participation level, and both roles are valued. The specific expectations for each role vary by subcommittee (see Reference-level explanation).

## Meeting Policies

All consortium meetings follow these policies:

### Chatham House Rule

Participants may share the meeting notes publicly gathered from meetings but must not reveal the identity of speakers. This encourages candid discussion.

### No Recordings or Transcriptions

Meetings are not recorded, and AI transcription tools are prohibited. Meeting notes are taken by designated notetakers who volunteer, following consortium templates:

- [Notetaker Role Guide](https://github.com/rustfoundation/safety-critical-rust-consortium/blob/main/docs/notetaker-role.md)
- [Full Consortium Meeting Notes Template](https://github.com/rustfoundation/safety-critical-rust-consortium/blob/main/docs/full-consortium-meeting-notes-template.md)
- [Subcommittee Meeting Notes Template](https://github.com/rustfoundation/safety-critical-rust-consortium/blob/main/docs/subcommittee-meeting-notes-template.md)

# Reference-level explanation
[reference-level-explanation]: #reference-level-explanation

## Consortium Governance

### Leadership Structure

| Role | Current Holder | Responsibilities |
|------|----------------|------------------|
| Rust Foundation Sponsor | Joel Marcey | Organizational support, logistics, Rust Foundation liaison |
| Consortium Lead | Pete LeVasseur | Cross-subcommittee coordination, external representation |
| Coding Guidelines Subcommittee Lead | Pete LeVasseur | Subcommittee operations, meeting facilitation, coding guidelines overall maintenance |
| Liaison Subcommittee Lead | Alex Celeste | Subcommittee operations, external engagement coordination |
| Tooling Subcommittee Lead | Alexandru Radovici | Subcommittee operations, tooling catalog management |

### Decision Making

The consortium follows a consensus-based decision-making model as described in the RFC process documentation. Key principles:

- Decisions seek to address concerns from all sides rather than having one side "win"
- Consensus is reached when major objections are addressed
- For trivial disagreements, subcommittee chairs may make executive decisions
- For deep disagreements, a blocking concern process exists with escalation paths

### RFC Process

Substantial changes to consortium artifacts or operations require an RFC:

1. Author creates an RFC using the template
2. RFC is submitted as a pull request
3. The relevant subcommittee reviews and iterates
4. Final Comment Period (FCP) of 10 days before merge
5. After merge, RFC is "active" and can be implemented

The full process is documented in the [RFC repository README](https://github.com/rustfoundation/safety-critical-rust-consortium-rfcs/blob/main/README.md).

## Membership Details

### Observer and Producer Definitions

At the consortium level, these roles are intentionally loosely defined:

**Observer**:
- Participates in meetings
- Follows discussions on Zulip and GitHub
- Provides feedback and perspective
- No specific contribution expectations

**Producer**:
- Actively works on consortium artifacts
- Takes ownership of work items
- Participates in reviews
- Expected to follow through on commitments

Members may shift between roles based on availability and interest. There is no formal process to change status.

## Subcommittee Operations

### Coding Guidelines Subcommittee

**Mission**: Develop community-vetted coding guidelines for Rust in safety-critical systems. A living document updated as Rust evolves and practitioners learn from experience.

**Meeting Schedule**: Weekly, alternating time zones (one EU/Asia-friendly, one Asia/Americas-friendly, one Americas/EU-friendly)

**Primary Artifact**: [Safety-Critical Rust Coding Guidelines](https://github.com/rustfoundation/safety-critical-rust-coding-guidelines)

**Role Definitions**:

| Role | Description | Expectations |
|------|-------------|--------------|
| Observer | Follows discussion, provides feedback | Attend meetings as interest allows |
| Producer | Actively contributes guidelines | Tagged by guidelines-bot for reviews in round-robin fashion; expected to complete reviews |
| Core Member | Informal designation for active maintainers | Higher involvement in process decisions, mentoring new contributors |

**Key Resources**:
- [GOALS.md](https://github.com/rustfoundation/safety-critical-rust-coding-guidelines/blob/main/GOALS.md)
- [CONTRIBUTING.md](https://github.com/rustfoundation/safety-critical-rust-coding-guidelines/blob/main/CONTRIBUTING.md)
- [Kanban board](https://github.com/orgs/rustfoundation/projects/1/views/3)

### Liaison Subcommittee

**Mission**: Proactively and reactively collaborate with external groups including standards committees, the Rust Project, and industry organizations. Drive agreement on safety-critical Rust efforts and handle IP considerations for referencing external documents.

**Meeting Schedule**: As-needed

**Primary Artifacts**:
- [Responsible Individuals list](https://github.com/rustfoundation/safety-critical-rust-consortium/blob/main/subcommittee/liaison/responsible-individuals.md): Maps external organizations to SCRC contacts
- [Standards and Bodies list](https://github.com/rustfoundation/safety-critical-rust-consortium/blob/main/subcommittee/liaison/standards-and-bodies.md): Tracks engagement with standards bodies

**Role Definitions**:

The Liaison subcommittee has not formalized observer/producer distinctions beyond the consortium-wide definitions.

**External Engagement Areas**:
- ISO 26262 (automotive functional safety)
- IEC 61508 (general functional safety)
- DO-178C (aerospace)
- MISRA
- AUTOSAR
- Rust Project (including FLS maintenance)
- WG23 (TR 24772 language vulnerabilities)
- Various national standards bodies (INCITS, BSI, etc.)

### Tooling Subcommittee

**Mission**: 
1. Aggregate community-vetted tooling for safety-critical Rust certification
2. Maintain a tools list with development status
3. Identify tooling gaps and advocate for solutions

**Meeting Schedule**: Biweekly

**Primary Artifacts**:
- [Available tools list](https://github.com/rustfoundation/safety-critical-rust-consortium/blob/main/subcommittee/tooling/tool-list/available-tools.yaml)
- [Desired compiler features](https://github.com/rustfoundation/safety-critical-rust-consortium/blob/main/subcommittee/tooling/compiler-features/desired-compiler-features.yaml)
- [Tool submission flow documentation](https://arewesafetycriticalyet.org/tooling/rfc-tools-review/)

**Role Definitions**:

The Tooling subcommittee has not formalized observer/producer distinctions beyond the consortium-wide definitions.

**Task Forces**:

The Tooling subcommittee has established two task forces:

| Task Force | Purpose | Members |
|------------|---------|---------|
| Tooling Submissions Task Force | Review and catalog tool submissions, maintain the tools list | Tiago Manczak, Manuel Hatzl, Arnaud Fontaine |
| Rust Project Bridge Task Force | Facilitate engagement between SCRC and the Rust Project, support Rust Project Goals related to safety-critical | Alexandru Radovici, Xander Cesari, Pete LeVasseur |

**Tool Submission Process**:
1. Anyone creates an issue requesting a tool addition/change/deletion
2. Issue is triaged and assigned to a Tooling Submissions Task Force member
3. Up to 15 days for review (checking tool information, validity for safety-critical use)
4. PR created to update available-tools.yaml
5. PR reviewed and merged

**Annual Review**: The Tooling Task Force conducts an annual review of all listed tools to verify maintenance status, license updates, and vendor status.

## Artifacts and Resources

### Consortium-wide

| Resource | Location | Purpose |
|----------|----------|---------|
| Main repository | [github.com/rustfoundation/safety-critical-rust-consortium](https://github.com/rustfoundation/safety-critical-rust-consortium) | Central coordination, membership, meeting notes |
| RFC repository | [github.com/rustfoundation/safety-critical-rust-consortium-rfcs](https://github.com/rustfoundation/safety-critical-rust-consortium-rfcs) | Process changes, major decisions |
| Website | [arewesafetycriticalyet.org](https://arewesafetycriticalyet.org) | Public-facing information, documentation |
| Zulip | [rust-lang.zulipchat.com/#narrow/channel/445688-safety-critical-consortium](https://rust-lang.zulipchat.com/#narrow/channel/445688-safety-critical-consortium) | Real-time discussion |

### Subcommittee-specific

| Subcommittee | Repository/Location | Key Artifact |
|--------------|---------------------|--------------|
| Coding Guidelines | [github.com/rustfoundation/safety-critical-rust-coding-guidelines](https://github.com/rustfoundation/safety-critical-rust-coding-guidelines) | Coding guidelines document |
| Liaison | [github.com/rustfoundation/safety-critical-rust-consortium/tree/main/subcommittee/liaison](https://github.com/rustfoundation/safety-critical-rust-consortium/tree/main/subcommittee/liaison) | [Responsible individuals list](https://github.com/rustfoundation/safety-critical-rust-consortium/blob/main/subcommittee/liaison/responsible-individuals.md) |
| Tooling | [github.com/rustfoundation/safety-critical-rust-consortium/tree/main/subcommittee/tooling](https://github.com/rustfoundation/safety-critical-rust-consortium/tree/main/subcommittee/tooling) | [Tools list (YAML)](https://github.com/rustfoundation/safety-critical-rust-consortium/blob/main/subcommittee/tooling/tool-list/available-tools.yaml) |

# Drawbacks
[drawbacks]: #drawbacks

1. **Documentation overhead**: Maintaining accurate documentation of operations requires ongoing effort. If the consortium changes practices without updating this RFC (or successor documents), the documentation becomes misleading.

2. **Premature formalization**: By documenting current practices, we risk implicitly endorsing them as "correct" when some practices emerged from convenience rather than deliberate design.

3. **Scope limitations**: This RFC captures a snapshot in time. It may not age well as the consortium evolves.

# Rationale and alternatives
[rationale-and-alternatives]: #rationale-and-alternatives

## Why document the current state?

The primary alternative is to proceed directly to proposing improvements without this baseline RFC. However:

- **Without a baseline, "change" is ambiguous**: Future RFCs proposing operational changes would need to describe both current state and proposed state, making them longer and less focused.

- **Institutional knowledge is fragile**: Current operations exist primarily in the heads of active participants. This RFC captures that knowledge explicitly.

- **New members need orientation**: A single document describing operations is more useful than piecing together information from scattered READMEs and meeting notes.

## Why use an RFC for this?

An RFC provides:
- Review by consortium members
- A permanent, versioned record
- A template for future operational documentation

The alternative (a simple README or wiki page) lacks the review rigor and versioning benefits.

## Impact on code readability

This RFC does not affect Rust code directly. It affects consortium processes, which indirectly influence the quality of coding guidelines and tooling recommendations.

# Prior art
[prior-art]: #prior-art

## Rust Project Governance

The Rust Project maintains [governance documentation](https://www.rust-lang.org/governance) describing teams, working groups, and decision processes. The SCRC's structure is simpler but follows similar patterns of distributed ownership through subcommittees.

## Rust Project RFC Process

The Rust Project uses an [RFC process](https://github.com/rust-lang/rfcs) for proposing substantial changes to the language, libraries, and project processes. The SCRC's RFC process is modeled after this approach. Key similarities include:

- Proposals submitted as pull requests with structured templates
- Community discussion and iteration on the PR
- Final Comment Period (FCP) before acceptance
- "Active" RFCs that are approved but not yet implemented

The Rust Project's process has evolved over a decade and handles language-level changes, which are more complex than consortium operational changes. The SCRC's process is intentionally simpler, reflecting our smaller scope and membership. However, the core principles—transparent discussion, consensus-building, and permanent records—are shared.

For reference:
- [Rust RFCs repository](https://github.com/rust-lang/rfcs)
- [Rust RFC process documentation](https://github.com/rust-lang/rfcs#rust-rfcs)

## MISRA

MISRA (Motor Industry Software Reliability Association) operates similarly: an industry consortium developing guidelines for safety-critical software. MISRA's structure includes working groups focused on specific languages (C, C++) and topics. The SCRC's subcommittee model mirrors this approach.

## AUTOSAR

AUTOSAR (AUTomotive Open System ARchitecture) uses working groups for different technical areas. Their Working Group for Functional Safety (WG-SAF) has addressed Rust, and SCRC maintains liaison connections with them.

## Other Rust Foundation Initiatives

The Rust Foundation has established other community initiatives with varying governance models. The SCRC's approach of low-barrier membership with optional deeper involvement (producer role, task forces) seeks to balance accessibility with effective contribution.

# Unresolved questions
[unresolved-questions]: #unresolved-questions

The following aspects of current operations remain unclear and may require future RFCs to address:

1. **Observer/Producer distinction enforcement**: Currently self-selected. Should there be any formal designation or tracking?

2. **Membership removal**: Under what circumstances might a member be removed? No process exists currently.

# Future possibilities
[future-possibilities]: #future-possibilities

This baseline RFC enables several follow-on RFCs:

1. **Establishment of a Consortium Leadership Council**: The council would be comprised of a Rust Foundation Sponsor, a Consortium Lead, and then the Team Leads. This council would facilitate in-person meetings at conferences and support cross-subcommittee decision-making.

2. **Standardization of Joining the Consortium**: Define clear expectations, privileges, and responsibilities for member role within the Consortium.

    * The observer / producer distinction at the Consortium level may not make much sense. The bulk of the work happens at the Subcommittee level. It seems possible that simply having there be a member role within the Consortium can help streamline this.

3. **Team Normalization**: Normalization of teams' structure, similar in nature to the Rust Project, to allow for a Team to have a Sub-Team, and so on, as necessary.

     * An example of this would be having the Tooling Subcommittee become the Tooling Team. Then to have the Tooling Submissions Task Force become the Tool Catalog Team and exist as a sub-team beneath the Tooling Team.
     * Helps normalize the structure without needing to consult a thesaurus each time we want a new team.

4. **Separation Between Teams, Contributor Teams, Observer Teams**: Subcommittees need the ability to assign permissions to Consortium resources. Currently with the observer/producer distinction and lack of an established way to migrate someone from one to the other we have no clean way to do this.

    * An example of this would be having what we currently call the Coding Guidelines Subcommittee be split into three teams:
      * Coding Guidelines Team: What we currently call the "Core Team" of the Coding Guidelines Subcommittee. The people on this team would then clearly be able to have permissions needed on the Safety-Critical Rust Coding Guidelines repo.
      * Coding Guidelines Contributors Team: The remainder of the Coding Guidelines Subcommittee which self-selected as Producers. Sub-team of Coding Guidelines Team. Team expectation to review and contribute to the coding guidelines.
      * Coding Guidelines Observers Team: The remainder of the Coding Guidelines Subcommittee which self-selescted as Observers.  Sub-team of Coding Guidelines Team. No real expectation here, allows ability to join meetings.
   * Meeting invites would still be sent out to all three teams sent out to the above.

5. **A Mechanism to Change Team Memberships**: Given the breakdown of Teams, Contributor Teams, and Observer Teams it seems worthwhile to have there be a flexible mechanism to allow change in team membership.

   * For example, if someone on the Coding Guidelines Contributors Team is indeed contributing and taking a real interest in the work of maintainership, they may be asked if they would like to join the Coding Guidelines Team.

6. **A Mechanism to Record (Changes in) Team Membership**: We likely need some better-published way of recording team memberships, probably on our website: arewesafetycriticalyet.org.

These possibilities are out of scope for this RFC, which is intentionally limited to documenting current state rather than proposing changes.

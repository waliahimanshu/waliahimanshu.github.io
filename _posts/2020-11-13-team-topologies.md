---
layout: post
title: "Team topologies summary"
comments: true
author: "waliahimanshu"
meta: "Team topologies summary"
categories: Books
---

### Team topologies: Organizing Business and Technology Teams for Fast Flow by Manuel Pais and Matthew Skelton

{% include category_include.html %}

### Chapter 1 - The problem with org charts

Modern IT organizations must deliver and operate
software systems rapidly and safely, while simultaneously growing and adapting changes and pressures in the business or regulatory environment

#### Communication Structures of an Organization

It usually shows hierarchical lines of reporting, which imply lines of communication running “up and down” the organization.

In reality people don’t restrict their communications only to those connected
lines on the chart. They reach out to whomever we depend on to get work done. They bend the rules when required to achieve our goals. That’s why actual communication lines look quite different from the org chart

#### Org Chart Thinking Is the Problem

Decisions based on org-chart structure tend to optimize for only part of
the organization, ignoring upstream and downstream effects. Local optimizations help the teams directly involved, but they don’t necessarily help improve the overall delivery of value to customers. For example, having teams adopting cloud and infrastructure-as-code can reduce the time to provision new infrastructure from weeks or months to minutes or
hours. But if every change requires deployment (to production) approval from a board that meets once a week, then delivery speed will remain weekly at best.

Thinking of the org chart as a faithful representation of how work gets done and how teams interact with each other leads to ineffective decisions around allocation of work and responsibilities. Much like a software architecture document gets outdated as soon as the actual software development starts, an org chart is always out of sync with reality.


So if org charts are not an accurate representation of organizational structures, what is? Niels Pflaeging, author of Organize for Complexity, identifies not one but three different organizational structures in every organization:?

1. Formal structure (the org chart)—facilitates compliance
2. Informal structure—the “realm of influence” between individuals
3. Value creation structure—how work actually gets done based on inter-personal and inter-team reputation

#### Team Topologies: A New Way of Thinking about Teams
Team Topologies provides four fundamental team types—stream-aligned, platform,
enabling, and complicated-subsystem—and three core team interaction modes
—collaboration, X-as-a-Service, and facilitating. Together with awareness of Conway's law, *team cognitive load*, and *how to become a sensing organization*, Team Topologies results in an effective and humanistic approach to building and running software systems.

#### The Revival of Conway’s Law
What is conway's Law :

“Organizations which design systems .. . are
constrained to produce designs which are copies of the communication structures ofthese organizations.”

### Chapter 2: Conway's Law and Why It Matters".


### Chapter 3: Team-First Thinking 

Google on their own teams found that who is on the team matters less than
the team dynamics; and that when it comes to measuring performance, teams matter more than individuals.? We must, therefore, start with the team for effective software delivery. There are multiple aspects to consider and nurture: *team size, team lifespan, team relationships, and team cognition*.

#### Use Small, Long-Lived Teams as the Standard
Team has a very specific meaning. By team, we mean a stable grouping of
five to nine people who work toward a shared goal as a unit. In most organizations, an effective team has a maximum size of around **seven to nine** people. Dunbar found *fifteen to be the limit* of the number of people one person can trust deeply.” From those, only around five people can be known and trusted closely.

Allowing teams to grow beyond the magic seven-to-nine size imperils the viability of the software being built by that team, because trust will begin to break down and unsuitable decisions might ensue. Organizations need to maximize trust between people on a team, and that means limiting the number of team members

#### Work Flows to Long-Lived Teams

Typically, a team can take from *two weeks to three months* or more to become a cohesive unit. When (or if) a team reaches that special state, it can be many times more effective than individuals alone. If it takes three months
for a team to become highly effective, we need to provide stability around and within the team to allow them to reach that level. Typically, a team can take from two weeks to three months or more to become a cohesive unit. When (or if) a team reaches that special state, it can be many times more effective than individuals alone. Adding new people to a team doesn’t immediately increase its capacity as there is emotional adaption to accommodate each other view points.

#### Team owns the Software 
Teams may use
shared services at runtime, but every running service, application, or subsystem is owned
by only one team. Awareness of
and ownership over these different time horizons helps a team care for the code more
effectively.

#### Team Members Need a Team-First Mindset
Team members should put the needs of the team above their own.
They should:
- Arrive for stand-ups and meetings on time.
- Keep discussions and investigations on track.

Encourage a focus on team goals.

Help unblock other team members before starting on new work.
Mentor new or less experienced team members.

Avoid “winning” arguments and, instead, agree to explore options.

#### Embrace Diversity in Teams

Members of diverse backgrounds tend to produce more creative solutions more rapidly and tend to be better at empathizing with other teams’ needs.!”
How ? In the context of discovering new possibilities, having a variety of viewpoints and experiences helps teams traverse the landscape of solutions much more rapidly. As Naomi Stanford, author of Guide to Organisation Design, puts it: “people and organizations benefit from a diverse workforce where differences spark positive energy.”

#### Good Boundaries Minimize Cognitive Load
**Restrict Team Responsibilities to Match Team Cognitive Load**

Ever-increasing size and complexity of codebases that teams have to work with.
This creates an unbounded cognitive load on teams.  Also applies to teams like a  operations or infrastructure team. They can also suffer from excessive
cognitive load in terms of domains of responsibility, number of applications they need to operate, and tools they need to manage.

For software-delivery teams, a team-first approach to cognitive load means limiting the size of the software system that a team is expected to work with; that is, organizations should not allow a software subsystem to grow beyond the cognitive load of the team responsible for the software.

*Kinds of cognitive load:*

- Intrinsic cognitive load—trelates to aspects of the task fundamental to the problem space (e.g., “What is the structure of a Java class?” “How do I create a new method?”)

- Extraneous cognitive load—relates to the environment in which the task is being done (e.g., “How do I deploy this component again?” “How do I configure this service?”)

- Germane cognitive load—relates to aspects of the task that need special attention for learning or high performance (e.g., “How should this service interact with the ABC service?”)

Many organizations do not consider the cognitive load on teams when
assigning responsibility for parts of a software system, instead assuming that by adding more teams to the problem, the cognitive load will be shared across the teams. Instead, the teams will suffer from similar communication and interaction strains

If we stress the team by giving it responsibility for part of the system that is beyond its cognitive load capacity, it ceases to act like a high-performing unit and starts to behave like a loosely associated group of individuals, each trying to accomplish their individual tasks without the space to consider if those are in the team’s best interest.

#### Measure the Cognitive Load Using Relative Domain Complexity
“Do you feel like you're effective and able to respond in a timely fashion to the work you are asked to do?”
Tying to determine the cognitive load of software using simple measures such as lines of code, number of modules, classes, or methods is misguided.

1. The first heuristic is to assign each domain to a single team. If a domain is too large for a team, instead of splitting responsibilities of a single domain to multiple teams, first split the domain into subdomains and then assign each new subdomain to a single team.
2. The second heuristic is that a single team (considering the golden seven-to-nine team size) should be able to accommodate two to three “simple” domains. Because such domains are  procedural, the cost of context switching between domains is more bearable
3. The third heuristic is that a team responsible for a complex domain should not have any more domains assigned to them—not even a simple one.
The last heuristic is to avoid a single team responsible for two complicated domains.

#### Match Software Boundary Size to Team Cognitive Load
Instead of choosing between a monolithic architecture or a microservices
architecture, design the software to fit the maximum team cognitive load. Only then can we hope to achieve sustainable, safe, rapid software delivery. This team-first approach to software boundaries leads to favoring certain styles of software architecture, such as small, decoupled services.

1. Provide a team-first working environment (physical or virtual).
2. Minimize team distractions during the workweek by limiting meetings, reducing emails, assigning a dedicated team or person to support queries, and so forth.
3. Change the management style by communicating goals and outcomes rather than
obsessing over the "how"
4. Increase the quality of developer experience (DevEx) for other teams using your team’s code and APIs through good documentation, consistency, good UX, and other DevEx practices.
5. Use a platform that is explicitly designed to reduce cognitive load for teams building software on top of it.

> Minimize cognitive load for others” is one of the most useful heuristics 
> for good software development.

#### Define “Team APIs” that Include Code, Documentation, and User
The team API should explicitly consider usability by other teams: Will other teams find it easy and straightforward to interact with us, or will it be difficult and confusing?
How easy will it be for a new team to get on board with our code and working practices?
How do we respond to pull requests and other suggestions from other teams? Is our team backlog and product roadmap easily visible and understandable by other teams?
For effective team-first ownership of software, teams need to continuously define,advertise, test, and evolve their team API to ensure that it is fit for purpose for the consumers of that API: other teams/memebers. 

The team API includes:

1. Code: runtime endpoints, libraries, clients, UI, etc. produced by the team
2. Versioning: how the team communicates changes to its code and services (e.g., using emantic versioning [SemVer] as a “team promise” not to break things)
3. Wiki and documentation: especially how-to guides for the software owned by the team
4. Practices and principles: the team’s preferred ways of working
5. Communication: the team’s approach to remote communication tools, such as chat tools and video conferencing
6. Work information: what the team is working on now, what’s coming next, and overall priorities in the short to medium term
7. Anything else that other teams need to use to interact with the team

#### Facilitate Team Interactions for Trust, Awareness, and Learning

(1) a consciously designed physical and virtual
environment; 
and (2) time away from desks at guilds, communities of practice (a group of
people who regularly get together on a voluntary basis to collectively learn and share knowledge about a domain of interest, internal tech conferences, etc.

#### Explicitly Design the Physical and Virtual Environments to Help Team Interactions
Neither individual cubicles nor fully open-plan seating is generally suitable for teams . We need something better. Teams need the ability to collaborate frequently, internally and only occasionally externally (with other teams). This balance is hard to achieve both in an open-plan layout (no dedicated work area for the team) and in an individual- workspaces layout (time together needs to be planned ahead of time and meeting rooms
are often scarce).
Example : Spotify—talked about how “squads in a tribe are all physically in the same office, normally right next to each other, and the lounge areas nearby promote collaboration between the squads.”°

*Office design for effective software delivery should accommodate all of the following modes of work: focused individual work, collaborative intra-team work, and collaborative inter-team work.*

#### Warning: Engineering Practices Are Foundational
At the end of the day, technology teams need to invest in proven team practices like continuous delivery, test-first development, and a focus on software operability and releasability. Without them, all the effort invested in a team-first approach to work and flow will be greatly undermined.


### Chapter 4 Static team topologies 

#### Team Anti-Patterns
The first anti-pattern is ad hoc team design. This includes teams that have grown too large and been broken up as the communication overhead starts taking a toll.
The other common anti-pattern is shuffling team members. This leads to extremely volatile team assembled on a project basis and disassembled immediately afterward,
perhaps leaving one or two engineers behind to handle the “hardening” and maintenance phases of the application(s).

Organizations must design teams intentionally by asking these questions: 
Given our skills, constraints, cultural and engineering maturity, desired software architecture, and
business goals, which team topology will help us deliver results faster and safer?

#### Design for Flow of Change
Technical staff at Spotify are arranged into small, autonomous, cross-functional squads, each with a long-term mission and comprised of around five to nine people.
Several squads that work on similar areas are collected into a tribe, a sort of affinity grouping of squads. The squads within a tribe are familiar with the work of other squads and coordinate inside the tribe.


Engineers within a tribe with similar skills and competencies share practices through a chapter. So, for example, all the testers across six squads in a tribe could be part of a testers chapter. Line management also happens via chapters, but the line manager (the chapter lead) is also part of the day-to-day work of a squad, not an aloof manager. Spotify also uses a more diffuse “guild,” akin to a community of practice, that can include people
from across multiple tribes, chapters, and squads. “Chapters and guilds . . . [are] the glue
that keeps the company together, [providing] economies of scale without sacrificing too

#### Shape Team Intercommunication to Enable Flow and Sensing
organizations seem to assume that software delivery is a one-way process, leading from specification to design, from
design to coding, from coding to testing and releasing, and from releasing to business as usual (BAU) operation

Assumption that the software-development process has little or nothing to learn from how the software runs
in the live environment is fundamentally flawed. On the contrary, organizations that expose software-development teams to the software running in the live environment
tend to address user-visible and operational problems much more rapidly compared to their siloed competitors 

we must . . . ensure delivery teams are cross-functional, with all the skills necessary to design, develop, test, deploy, and operate the system on the same team.” 

Organizations that value information feedback from live (production) systems can not only improve their software more rapidly but also develop a heightened
responsiveness to customers and users.

#### DevOps and the DevOps Topologies

“wall of confusion.” - >
In dev ops word when with software releases being thrown over the “fence” or
“wall” and communication mostly accomplished through tickets

The problem was that many organizations adopting Agile were not explicitly addressing the gap between software delivery speed and operations teams’ capacity to provide resources or deploy updates. The misalignment between teams became more and more evident, leading to poor behaviors and lack of
focus on the flow of work.

#### DevOps Topologies
The DevOps Topologies reflect two key ideas: 
(1) There is no one-size-fits-all approach to structuring teams for DevOps success. The suitability and effectiveness of
any given topology depends on the organization’s context. (2) There are several topologies known to be detrimental (anti-patterns) to DevOps success, as they overlook
or go against core tenets of DevOps. 
In short, there is no “right” topology, but several “bad” topologies for any one organization.

#### Successful Team Patterns

#### Feature Teams Require High-Engineering Maturity and Trust
We consider a feature team to be a cross- functional, cross-component team that can take a customer facing feature from idea all the way to production, making them available to customers and, ideally, monitoring its
usage and performance. Are these a pattern or an anti-pattern? As you might have guessed by now, it depends.

A cross-functional feature team can bring high value to an organization by delivering cross-component, customer-centric features much faster than multiple component teams making their own changes and synchronizing into a single release. But this can only happen when the feature team is self-sufficient, meaning they are able to deliver features into production without waiting for other teams.

The feature team typically needs to touch multiple codebases, which might be owned by different component teams. If the team does not have a high degree of engineering maturity, they might take shortcuts, such as not automating tests for new user workflows
or not following the “boy-scout rule” (leaving the code better than they found it). Over time, this leads to a breakdown of trust between teams as technical debt increases and slows down delivery speed.

#### Product Teams Need a Support System

The key for the team to remain autonomous is for external dependencies to be non-blocking, meaning that new features don’t sit idle, waiting for something to happen
beyond the control of the team. For example, it’s extremely difficult to ensure that a separate QA team will be available to evaluate a new feature exactly when the product
team finishes it. 
Non-blocking dependencies often take the form of self-service capabilities (e.g, around provisioning test environments, creating deployment pipelines, monitoring, etc.) developed and maintained by other teams. These can be consumed independently by the
product teams when they need them.


#### Cloud Teams Don’t Create Application Infrastructure

Product teams need autonomy to provision their own environments and resources in the cloud, creating new images and templates where necessary. The cloud team might still own the provisioning process—ensuring that the necessary controls, policies, and
auditing are in place

#### SRE Makes Sense at Scale

Site Reliability Engineering is an approach to the operation and improvement of software applications pioneered by Google to deal with their global, multi-million-user systems. If adopted in full, SRE is significantly different from IT operations of the past, due to its focus on the “error budget” (namely defining what is an acceptable amount of downtime)
and the ability of SRE teams to push back on poor software.

People on SRE teams need excellent coding skills and—crucially—a strong drive (and bandwidth) to automate repetitive Ops tasks using code, thereby continually reducing toil.

The SRE model sets up a healthy and productive interaction between the development and SRE teams by using service-level objectives (SLOs) and error budgets to
balance the speed of new features with whatever work is needed to make the software
reliable.

>SRE teams are not essential; they are optional.


The relationship between an SRE team and an
application-development team changes at different
points of the software’s life and even month by month

Initially, the application development
team alone builds and runs the software in production
until the scale merits SRE help. 
During a second stage as the application usage increases,
SRE provides guidance (represented in green) to the
application development team on how to make the
application work better at global scale. Later, SRE becomes fully involved by running and supporting the application (but still collaborating with the application team) when the
scale merits it At this point, the product owner for the application must decide a suitable service-level objective with a corresponding error budget. If at
some point  the application becomes too difficult to support due to lack of operability, or if the application usage drops off, the application team takes on
operational responsibility again. 

> that building and running software systems is a sociotechnical activity, not an assembly line in a factory.    

#### Considerations When Choosing a Topology

1. Technical and Cultural Maturity
2. Organization Size, Software Scale, and Engineering Maturity -> Low maturity organizations will need time to acquire the engineering and product development capabilities required for autonomous end-to-end teams. Meanwhile, more specialized teams (development, operations, security, and others) are an acceptable trade-
off, as long as they collaborate closely to minimize wait times and quickly address issues.

3.Splitting Responsibilities to Break Down Silos

Sometimes we can remove or lessen dependencies on specific teams by breaking down their set of responsibilities and empowering other teams to take some of them on. For
example, a pattern increasingly adopted in many organizations over the past few years has been to separate the activities of database development (DB Dev) from database administration (DBA).

4.Dependencies and Wait Times between Teams
Spotify relies on a simple spreadsheet to detect and track interdependencies
between squads and tribes. It highlights whether a dependency is on a squad
within the same tribe (acceptable) or in a different tribe (potentially a warning that
team design or work assignment is wrong).
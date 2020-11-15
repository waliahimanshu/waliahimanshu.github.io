---
layout: post
title: "Team topologies summary"
comments: true
author: "waliahimanshu"
meta: "Team topologies summary"
categories: Books
---


### Team topologies: Organizing Business and Technology Teams for Fast Flow by Manuel Pais and Matthew Skelton - Notes

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
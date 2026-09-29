# Project Backlog — AI Innovation Quest

> Status: proposed backlog, pending scope approval and estimation.
> Source: `README.md`.
> Delivery estimate: validate after the Talent Voyage reuse audit and team-capacity review.

## Table of Contents

1. [Planning Assumptions](#planning-assumptions)
2. [Priorities](#priorities)
3. [Discovery and Scope Decisions](#discovery-and-scope-decisions)
4. [Platform, Access, and Identity](#platform-access-and-identity)
5. [Mission Control and Space Map](#mission-control-and-space-map)
6. [Challenge Configuration and Completion](#challenge-configuration-and-completion)
7. [Points, Ranks, Badges, and Progress](#points-ranks-badges-and-progress)
8. [Leaderboards and Seasons](#leaderboards-and-seasons)
9. [Communications and Reporting](#communications-and-reporting)
10. [Quality, Operations, and Launch](#quality-operations-and-launch)
11. [Optional Enhancements](#optional-enhancements)
12. [Delivery Sequence](#delivery-sequence)
13. [Definition of Done](#definition-of-done)
14. [Next Steps](#next-steps)

## Planning Assumptions

- Launch includes individual participation, basic Mission Control, map exploration, challenges, progression, leaderboards, and administration.
- Teams, community conversations, advanced customization, and conversational AI are excluded from the initial release.
- Seasonal points are tracked separately from lifetime progression. This recommendation requires stakeholder approval.
- Previously released regions and historical achievements remain accessible.
- The application uses its own backend and data environment, even if Talent Voyage code or assets are reused.
- The initial copilot, if included, uses scripted content—not an LLM chatbot.
- The original 3–4 week build estimate is provisional.
- All items begin as **Proposed**. Owners and estimates will be assigned during planning.

## Priorities

| Priority | Meaning |
|---|---|
| **P0 — Launch blocker** | Required for a safe, functional release |
| **P1 — Core follow-up** | Required for the intended program, but potentially deliverable after the pilot |
| **P2 — Enhancement** | Optional; implement after scope approval |

P1 items with operational deadlines must be completed before their functionality is needed. For example, season rollover must be ready before the first season ends.

---

## Discovery and Scope Decisions

Complete these decisions before committing to the implementation schedule.

| ID | Priority | Backlog item | Completion criteria |
|---|---|---|---|
| DISC-01 | P0 | Confirm launch scope | Stakeholders approve pilot, launch, and post-launch feature lists; resolve features listed as both core and optional in the README. |
| DISC-02 | P0 | Audit Talent Voyage reuse | Identify reusable code, assets, and functionality; document constraints and effort needed for a separate environment. |
| DISC-03 | P0 | Define scoring and progression | Approve rank thresholds, seasonal versus lifetime points, variable-point rules, repeatable challenges, and point corrections. |
| DISC-04 | P0 | Define season and release rules | Approve cycle duration, boundaries, time zone, late submissions, pending reviews, ties, and rollover behavior. |
| DISC-05 | P0 | Confirm security and data requirements | Agree authentication, roles, hosting, retention, permitted submission content, and treatment of sensitive workplace information. |
| DISC-06 | P0 | Approve UX and visual direction | Approve key participant/admin screens, map style, basic ship/avatar, mobile behavior, and accessibility target. |
| DISC-07 | P0 | Prepare initial content | Approve initial destinations, challenges, prerequisites, points, validation methods, and copilot text if included. |

## Platform, Access, and Identity

| ID | Priority | User story / backlog item | Acceptance criteria |
|---|---|---|---|
| PLAT-01 | P0 | Establish an independent application environment | Application, backend, and participant data are isolated from Talent Voyage; secrets are not stored in source control. |
| PLAT-02 | P0 | As an employee, I can sign in securely | Approved authentication works; unauthorized users cannot access participant or admin data. |
| PLAT-03 | P0 | As an administrator, I can manage participants and roles | Admins can activate/deactivate participants and assign approved roles; permissions are enforced server-side. |
| PLAT-04 | P0 | As a participant, I have a personal profile and ship/avatar | Profile displays approved identity fields, rank, badges, and a persistent basic ship/avatar. |
| PLAT-05 | P0 | Record important administrative actions | Changes to roles, challenge configuration, reviews, and points record actor, timestamp, and action. |

**Dependencies:** DISC-02, DISC-05, DISC-06.

## Mission Control and Space Map

| ID | Priority | User story / backlog item | Acceptance criteria |
|---|---|---|---|
| MAP-01 | P0 | As a participant, I can start from Mission Control | Home screen provides instructions and access to missions, progress, leaderboard, and announcements. |
| MAP-02 | P0 | As a participant, I can explore available destinations | Released destinations are navigable on desktop and mobile; earlier destinations remain accessible. |
| MAP-03 | P0 | As a participant, I can understand challenge availability | Challenges show available, locked, pending-review, or completed states; locked challenges explain unmet prerequisites. |
| MAP-04 | P1 | As an admin, I can release new map regions | Admin can publish or schedule regions; all participants see released regions without bypassing challenge prerequisites. |
| MAP-05 | P1 | As a participant, I can anticipate new destinations | Unreleased destinations display approved teasers; a brief, dismissible discovery experience appears on release. |

**Dependencies:** DISC-04, DISC-06, DISC-07, platform foundation.

**Release constraint:** Region publishing must be available before the first post-launch map expansion. Initial destinations must be configured for launch.

## Challenge Configuration and Completion

| ID | Priority | User story / backlog item | Acceptance criteria |
|---|---|---|---|
| CHAL-01 | P0 | As an admin, I can create and update challenges | Configure Learn/Practice/Share/Transform category, destination, instructions, availability, points, validation method, and draft/published status; historical submissions are preserved. |
| CHAL-02 | P0 | As an admin, I can configure prerequisites | Support required challenges, rank, or badges; invalid prerequisite references and circular challenge dependencies are rejected. |
| CHAL-03 | P0 | As a participant, I can view a mission card | Card shows requirements, prerequisites, validation method, and fixed points or variable-point range and criteria on first view. |
| CHAL-04 | P0 | As a participant, I can complete a code-based challenge | Valid codes award completion once per permitted occurrence; invalid codes give feedback; verification is server-side and rate-limited. |
| CHAL-05 | P0 | As a participant, I can submit evidence | Support links, reflections, and screenshots/files; upload type/size restrictions and access controls apply. |
| CHAL-06 | P0 | As a reviewer, I can assess evidence | Reviewer can approve, reject, or request changes with feedback; variable awards stay within configured limits. |
| CHAL-07 | P0 | As a participant, I can track and revise submissions | Participant sees review status and feedback, can resubmit when allowed, and cannot earn duplicate awards through repeated requests. |
| CHAL-08 | P1 | As an admin, I can renew or repeat challenges | Configure recurrence or new occurrences; each occurrence has its own eligibility and completion record. |
| CHAL-09 | P1 | As an admin, I can use approved automated validation rules | Agreed rules validate eligible challenges; unsupported evidence continues through manual review. |

**Dependencies:** DISC-03, DISC-05, DISC-07, participant/admin access, destination configuration.

**Scope notes:**
- Challenge renewal becomes P0 if the pilot spans multiple required occurrences.
- Additional automated validation becomes P0 where initial challenge content requires it.
- Prerequisite types beyond challenges, rank, and badges require explicit definition.

## Points, Ranks, Badges, and Progress

| ID | Priority | User story / backlog item | Acceptance criteria |
|---|---|---|---|
| PROG-01 | P0 | As a participant, I receive accurate points | Awards are recorded with their source and season; retrying an operation cannot create duplicate awards. |
| PROG-02 | P0 | As a participant, I progress through ranks | Approved thresholds determine Beginner → Explorer → Navigator → Innovator; season rollover does not reduce rank. |
| PROG-03 | P0 | As a participant, I earn badges | Admins can define and award badges using agreed rules or manual recognition; earned badges persist across seasons. |
| PROG-04 | P0 | As a participant, I can review my journey | Personal history includes completions, submitted reflections, points, rank, badges, and recognition. |
| PROG-05 | P0 | As an admin, I can correct point awards | Corrections require a reason and retain an audit trail; totals and affected standings recalculate consistently. |

**Dependencies:** DISC-03, challenge completion/review, initial season configuration.

## Leaderboards and Seasons

| ID | Priority | User story / backlog item | Acceptance criteria |
|---|---|---|---|
| SEAS-01 | P0 | As a participant, I can view the current leaderboard | Show seasonal standings and my position using approved tie-breaking and identity-display rules. |
| SEAS-02 | P1 | As a participant, I can see nearby competitors | A local view shows approximately 10 people around my position and handles top/bottom boundaries. |
| SEAS-03 | P0 | Associate awards with seasons | The initial season is configured; awards are assigned according to approved submission/review timing rules. |
| SEAS-04 | P1 | As an admin, I can close a season and start another | Preserve final standings; new seasonal totals start at zero; ranks, badges, lifetime records, and prior destinations remain. |
| SEAS-05 | P1 | As an admin, I can recognize seasonal winners | Final winners can be reviewed and receive configured recognition; real-world reward fulfillment is tracked manually unless separately scoped. |

**Dependencies:** DISC-03, DISC-04, DISC-05, points tracking.

**Release constraint:** Season rollover must be delivered and tested before the first season ends, even if deferred beyond the pilot.

## Communications and Reporting

| ID | Priority | User story / backlog item | Acceptance criteria |
|---|---|---|---|
| COMM-01 | P0 | As an admin, I can publish in-game announcements | Published announcements are visible to intended participants; expired or withdrawn announcements stop appearing. |
| COMM-02 | P1 | As an admin, I can email participants | Authorized admins can send through an approved provider; delivery failures and communication preferences follow agreed requirements. |
| COMM-03 | P1 | As a participant, I receive useful status notifications | Notify participants of review outcomes, achievements, and content releases without duplicating messages. |
| REPORT-01 | P0 | As an admin, I can monitor participation and progress | Report includes active participants, completions by category, points, ranks, and pending reviews; metric definitions are documented. |
| REPORT-02 | P1 | As an admin, I can export reports | Export agreed fields with date/season filters; report access is restricted to authorized roles. |

**Dependencies:** DISC-05, participant management, challenge/progression records; approved email provider for COMM-02.

## Quality, Operations, and Launch

| ID | Priority | Backlog item | Acceptance criteria |
|---|---|---|---|
| QA-01 | P0 | Test critical participant and admin journeys | Cover sign-in, prerequisites, submissions, approval, duplicate prevention, awards, and permissions. |
| QA-02 | P0 | Validate mobile and accessible use | Critical journeys meet the agreed accessibility target; map information is also reachable through an accessible mission list. |
| QA-03 | P0 | Validate security and evidence handling | Test role boundaries, participant data isolation, upload access, input validation, and code-guessing protections. |
| OPS-01 | P0 | Establish deployment and recovery procedures | Deployment, monitoring, error logging, backups, and a tested restore process are available. |
| LAUNCH-01 | P0 | Run a participant/admin pilot | Representative users complete key journeys; launch-blocking defects are fixed and stakeholders approve release. |
| LAUNCH-02 | P0 | Prepare program administration | Provide guidance for content publishing, reviews, point corrections, reporting, support, and seasonal operations. |

**Dependencies:** Approved launch scope and implemented P0 journeys.

**Planning note:** Testing, accessibility, security, and operational work run throughout development—not only during the final week.

## Optional Enhancements

These items require scope approval and detailed acceptance criteria before implementation.

| ID | Priority | Feature | Suggested scope |
|---|---|---|---|
| ENH-01 | P2 | Scripted copilot | Character-based mission briefings, guidance, notifications, and celebrations; no LLM integration. |
| ENH-02 | P2 | Ship customization | Approved colors, markings, and emblems that persist across sessions. |
| ENH-03 | P2 | Voluntary teams | Teams of 5–7, membership management, team identity, and agreed team-scoring rules. |
| ENH-04 | P2 | Team leaderboard | Separate team standings with rules for membership changes and season boundaries. |
| ENH-05 | P2 | The Commons | Topic-based discussions with moderation, reporting, and content-management controls. |
| ENH-06 | P2 | Peer recognition | Nominations or acknowledgments with safeguards against abuse. |
| ENH-07 | P2 | Personal cockpit / trunk | Visual display of existing badges, rank items, souvenirs, and selected artifacts. |
| ENH-08 | P2 | Conversational AI discovery | Separate assessment of business value, security, approved models, cost, and governance—not part of launch. |

---

## Delivery Sequence

| Stage | Focus | Exit condition |
|---|---|---|
| **1. Definition** | Scope, reuse audit, scoring, seasons, security, initial content | Key decisions approved and backlog estimated |
| **2. End-to-end foundation** | Sign-in → mission → submission → review → points | One complete participant/admin journey works |
| **3. Launch experience** | Map, remaining challenge types, profiles, ranks, badges, leaderboard, reports | All agreed P0 features function together |
| **4. Pilot and hardening** | Security, accessibility, mobile testing, recovery, admin training | Pilot approval and no launch-blocking defects |
| **5. Program expansion** | Content releases, repeats, notifications, rollover, selected enhancements | Ready for ongoing content cycles and first season close |

Stage durations will be assigned after estimation. This sequence is not a commitment to the original 3–4 week schedule.

## Definition of Done

An implementation item is complete when:

- Its acceptance criteria are satisfied.
- Code is reviewed and merged.
- Relevant automated and manual tests pass.
- Permissions and data-handling requirements are verified.
- Applicable mobile and accessibility checks pass.
- Required administrative guidance and documentation are updated.
- The feature is deployed to the agreed test environment.
- The designated reviewer or product owner accepts it.

Discovery items are complete when their decisions and outputs are documented and approved by the relevant stakeholders.

## Next Steps

1. Review DISC-01 through DISC-07 with the client.
2. Confirm which P1 items must move into launch scope.
3. Assign owners and estimate approved items.
4. Split larger stories into implementation tasks.
5. Confirm delivery capacity and release dates.
6. Create the first iteration around a complete participant/admin journey.
7. Schedule region-release and season-rollover work before their operational deadlines.
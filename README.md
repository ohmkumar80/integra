# Charting the Future – AI Innovation Quest (working title)

A gamified **"Pocket Companion"** app for the client's AI learning journey. Employees explore an expanding space-themed world, complete AI missions, apply learning to their work, share knowledge with colleagues, and earn recognition through points, ranks and badges.

> Status: requirements / scope. Source document: `Charting the Future_Pocket Companion design_In Space!.docx`.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Theme and Experience Concept](#theme-and-experience-concept)
3. [Purpose and Objectives](#purpose-and-objectives)
4. [Program Structure](#program-structure)
5. [Core Requirements](#core-requirements)
6. [Challenges and User Experience](#challenges-and-user-experience)
7. [Optional / Additional Features](#optional--additional-features)
8. [Timeline and Milestones](#timeline-and-milestones)
9. [Open Decisions](#open-decisions)

---

## Project Overview

The app gives employees an engaging way to track and take part in AI-related learning activities, practical challenges and innovation opportunities.

- Builds on proven game mechanics from the previous **Talent Voyage** project, with a distinct identity and user experience.
- Participants travel between planets and stations, complete AI missions, apply learning to their work, share knowledge, and earn points, levels and badges.
- Intended to run for **at least two years**, with content added and renewed over time.

## Theme and Experience Concept

- **Narrative:** a visit to a possible future in which the client connects communities across Earth and beyond. (The client's industry is shipping.) The sci-fi setting is a playful layer over real, present-day AI learning; the challenges stay practical and tied to participants' work.
- **Home base:** participants start at **Mission Control** and navigate an illustrated star system in a small spacecraft.
- **Content cycles:** new planets, stations and destinations are revealed every **3–4 months**. Each cycle mixes **Learn, Practice, Share and Transform** challenges at different difficulty levels, so the world doesn't assume everyone starts at the same AI capability.
- **Spacecraft:** represents the participant on the map. In an enhanced version it can be customized (colours, markings, team identity), and its cockpit becomes a persistent personal space that accumulates badges, artifacts and other evidence of progress.
- **AI/bot copilot:** a recurring guide that introduces destinations and missions, explains requirements, sends notifications and celebrates achievements. It is a **character/avatar with scripted content, not an LLM chatbot**. Conversational AI could be explored separately.

## Purpose and Objectives

Create a visible, shared journey toward responsible and practical AI adoption across the organization.

| Objective | How the app supports it |
|---|---|
| Encourage responsible experimentation | Structured opportunities to try AI tools in meaningful workplace contexts |
| Build practical AI skills | Mix of learning, application, knowledge sharing and innovation activities |
| Support an organization-wide AI conversation | Exchange of ideas, tools, prompts, experiences and lessons learned |
| Make progress visible | Shared tracking of participation, achievements and progression for employees and admins; leaderboards and real-world rewards |
| Recognize contribution, not just completion | Points, levels, badges and other recognition |
| Sustain engagement over time | Experience evolves as new learning resources, technologies and business applications emerge |

## Program Structure

Designed as an **evolving framework, not a fixed curriculum**. New challenges will be added later and others periodically renewed (e.g. reading the newsletter, attending webinars, case competitions).

### Map expansion (3-month cycles)
- The illustrated star map expands in three-month cycles. Each phase reveals a new region, destinations and AI learning opportunities for the whole organization.
- New regions are visible and explorable by everyone on release, creating shared progress and anticipation.

### Readiness-based unlocking
- The map is visible to all, but individual challenges may require readiness criteria: prerequisite learning or challenges, a particular level or badge, or other requirements set by the program team.

### Individual progress
- Participants keep access to earlier regions and can return to unfinished or repeatable challenges.
- Faster participants get more activities; slower participants can still see where the organization is heading.

### Seasons
- Competitive cycles run roughly every **3–4 months**.
- At the end of a season, **points and leaderboard positions reset to zero**; **levels and badges are kept**.
- A new season starts shortly after, with a newly revealed map region and fresh challenges.
- This renews the chance to compete while preserving long-term recognition.

Content does not need to be fully defined at launch. It can be developed and added as the client's AI capabilities and priorities evolve.

## Core Requirements

### 1. Evolving learning journey
- Illustrated space map that grows over time; new planets, moons or stations appear as learning opportunities are released. Previously discovered destinations stay accessible.
- Future destinations appear at the map edges as faint luminescence, silhouettes or question marks, and are revealed through a brief **"new destination discovered"** experience on release.
- Periodic leaderboard seasons give fresh recognition opportunities without erasing lifetime progression.
  - Top users are recognized and rewarded each 3–4 month cycle, then leaderboards reset.
  - Seasonal achievements earn in-game assets (special badges or items) or real-world rewards.

### 2. Configurable challenges
- Administrators can create and update challenges, assign point values, set prerequisites and choose how completion is validated.
- Must support the client's envisioned range, from entering codes found in newsletters or learning sessions to submitting prompts, reflections, screenshots, links or evidence for admin review.
- Each challenge's requirements and point value (fixed or variable) are shown in its **pop-up card** on first participant view.

### 3. Progression and recognition
- Participants accumulate points and progress through ranks: **Beginner → Explorer → Navigator → Innovator**.

### 4. Personal journey and identity
- Each participant has a profile and a personalized ship/avatar that travels through the experience.
- Special badges or in-game items recognize specific behaviours and accomplishments.
- Completed challenges, achievements, reflections and recognition form a persistent record of the participant's AI journey.

### 5. Leaderboards and shared progress
- Individual and potentially team-based views provide visibility and friendly competition.
- Leaderboards should encourage continued participation and not feel out of reach for late joiners or slower progressors.
- Possible mechanism: a **"zoomed in" leaderboard** showing the 10 people immediately around the participant.

### 6. Administration and reporting
- Admins manage participants, challenges, points and recognition.
- Add new content over time.
- Communicate with participants by **email and in-game broadcasts**.
- Generate reports on participation and progress.

### 7. Separate and secure program environment
- May reuse proven Talent Voyage design and functionality, but runs on its **own backend and data environment**.
- Keeps participant information, reporting and future development separate from the existing program.

## Challenges and User Experience

Challenges are categorized **Learn – Practice – Share – Transform**. Participants are encouraged to focus more on Share and Transform as they rise in rank.

| Category | Examples |
|---|---|
| **Learn** | Read the monthly AI newsletter and enter a hidden code; attend a Lunch & Learn or webinar; complete assigned AI training; review an approved guide or resource |
| **Practice** | Complete a prompt-engineering mission using the CREATE framework; test an approved AI tool on a real work task; save and submit a reusable prompt; join an AI scavenger hunt or case competition |
| **Share** | Help a colleague use an AI tool; share a useful prompt, tip, story or use case; contribute a prompt to a company-wide library; present an example at a Lunch & Learn or for the newsletter |
| **Transform** | Submit an AI-enabled business or process improvement idea; prototype a new way of working; create an AI agent for individual use (subject to IT review before broader sharing) |

### Validation methods
- Hidden codes
- Links
- Short reflections or summaries
- Screenshots or other evidence
- Automated rules where practical
- Administrator review

Some challenges may be **repeatable or renewed each cycle** (e.g. reading the monthly newsletter).

## Optional / Additional Features

Some need deciding at the start of the project; others can be added later.

| Feature | Description |
|---|---|
| **Mission Control** | Persistent central space station and home base: instructions, mission discovery, leaderboards, customization, community. Areas: **Mission Board** (challenges and progress), **Commons** (conversation and sharing), **Hangar** (ship/team customization) |
| **Customizable ships** | Curated colours, markings and team emblems: individuality without breaking the client's visual identity |
| **The Commons** | Social area for topic-based conversations (prompt recommendations, AI tools, useful applications, questions). Could host peer recognition/nominations and team formation |
| **AI Copilot** | A small set of visually distinct bot copilots with different personalities. Appear in the cockpit and mission briefings with scripted guidance, notifications, encouragement and celebration. **Not a live AI chatbot in the initial version** |
| **Teams** | Voluntary teams of **5–7 players** for friendly competition, peer support or collaborative activities. Not tied to departments. Separate from overall leaderboard ranking. Team profiles/flags and a separate **Team Leaderboard** |
| **Personal cockpit and collectibles** | Cockpit/bridge as a visual record of the journey: badges, rank items, team flags, seasonal souvenirs, selected challenge artifacts. No need for a unique asset per completed challenge |
| **Personal Trunk** | Visual collection of badges, rank items, team flags, completed-challenge "books", messages and other artifacts. Rank items: compass (Explorer), spyglass (Navigator), sextant (Innovator) |
| **Seasons** | Periodic leaderboard seasons with seasonal badges/items or real-world rewards, without erasing lifetime progression |
| **Progressive map discovery** | New destinations appear as silhouettes or unexplored waters, revealed with a brief "new land spotted" experience |

## Timeline and Milestones

The original concept assumed a **3–4 week** initial build on the Talent Voyage foundation. The final schedule will be validated once the delivery approach, core versus enhanced feature set, and development responsibilities are confirmed.

| Timing | Milestone | Key activities |
|---|---|---|
| Week 1 | Define and Design | Confirm experience concept, program structure, progression/points logic, initial challenges, team/leaderboard approach and visual direction. Establish a separate technical environment and adapt the Talent Voyage foundation |
| Week 2 | Build Core Experience | Confirm core versus enhanced scope and technical architecture; decide what, if anything, to reuse from Talent Voyage; build the core experience |
| Week 3 | Populate and Extend | Configure initial destinations and challenges; implement leaderboards/teams and selected community or recognition features; build reporting and communications functions |
| Week 4 | Test and Launch | Participant/admin testing, mobile and browser QA, permissions and data testing, content refinement, admin orientation, pilot adjustments, launch preparation |
| Ongoing | Expand the Voyage | Release new destinations and challenges, introduce new recognition opportunities, review engagement data, progressively activate optional features |

## Open Decisions

- Core versus enhanced feature set for launch.
- What to reuse from Talent Voyage versus build new; final technical architecture.
- Points logic, rank thresholds and readiness criteria for unlocking challenges.
- Team and leaderboard approach (individual, team, "zoomed in" view).
- Real-world rewards for seasonal winners.
- Whether any conversational AI (beyond the scripted copilot) is in scope.
- Visual direction and level of ship/cockpit customization.

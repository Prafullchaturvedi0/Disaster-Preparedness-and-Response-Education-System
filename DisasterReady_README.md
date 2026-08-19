# DisasterReady --- Scenario-Based Disaster Preparedness & Behavioral Assessment

> **Learn → Test → Act → Evaluate → Improve**

DisasterReady is a scenario-based disaster preparedness learning
platform designed to teach students what to do during emergencies and
then evaluate how they actually respond under time pressure.

The platform is deliberately focused: instead of becoming another large
emergency-management ecosystem, its core innovation is the **interactive
practical simulation**.

Students progress through:

1.  **Material** --- learn the theory.
2.  **Quiz** --- test their knowledge.
3.  **Practical** --- enter an interactive disaster scenario.
4.  **Review** --- understand their decisions, mistakes and response
    quality.
5.  **Improve** --- receive personalized recommendations.

The practical simulation records **what the student did, when they did
it, whether it was appropriate, and what consequence followed**.

------------------------------------------------------------------------

## Why this product?

Traditional disaster education often measures whether a student can
answer a question.

DisasterReady also asks:

> **Can the student make the correct decision when the situation is
> changing and time matters?**

A student may know that they should evacuate during a fire, but a
simulation can test whether they:

-   recognize the hazard,
-   choose the correct action,
-   avoid dangerous actions,
-   select an appropriate route,
-   react to changing conditions,
-   and reach safety efficiently.

The result is an **Emergency Decision Score**, not just a game score.

------------------------------------------------------------------------

## Core Product Flow

``` text
                    STUDENT
                       |
                       v
                   PROFILE
                       |
          +------------+------------+
          |            |            |
          v            v            v
       MATERIAL       QUIZ       PRACTICAL
       LEARN IT      KNOW IT       DO IT
                                   |
                                   v
                         GAMIFIED SIMULATION
                                   |
                                   v
                           DECISION TRACKING
                                   |
                                   v
                             PERFORMANCE
                                   |
                                   v
                              REVIEW
                                   |
                                   v
                         PERSONALIZED LEARNING
```

### Product philosophy

``` text
LEARN → DECIDE → ACT → REFLECT
```

------------------------------------------------------------------------

# Key Differentiator

The platform is not positioned as:

> "A gamified disaster education website."

Instead:

> **A scenario-based disaster preparedness platform that evaluates how
> students actually respond to emergencies through real-time decision
> tracking, branching consequences and adaptive simulations.**

The technical/product novelty is concentrated around:

-   **Decision Telemetry**
-   **Adaptive Scenario Engine**
-   **Behavioral Performance Assessment**
-   **Personalized Preparedness Profile**

------------------------------------------------------------------------

# Features

## 1. Student Profile

The profile tracks:

-   Overall preparedness
-   Disaster-wise scores
-   Module progress
-   Quiz performance
-   Practical performance
-   Response time
-   Critical mistakes
-   Strengths
-   Areas for improvement
-   Recommended next modules

Example:

``` text
EMERGENCY READINESS PROFILE

Overall Preparedness: 82%

Fire          91%
Earthquake    84%
Flood         72%
Chemical      63%

Strengths
✓ Evacuation decisions
✓ Equipment recognition

Needs Improvement
! Chemical hazard identification
! Response time

Recommended:
Chemical Leak — Equipment & Evacuation
```

------------------------------------------------------------------------

# 2. Material Module

Each disaster has an educational module.

Initial disasters:

-   Fire
-   Earthquake
-   Flood
-   Chemical/Gas Leak

Content can include:

-   Basic information
-   Warning signs
-   Do / Don't actions
-   Step-by-step response
-   Evacuation
-   Equipment
-   Hazard recognition
-   Safety explanations

------------------------------------------------------------------------

# 3. Quiz Module

The quiz tests knowledge before the practical simulation.

Question types can include:

-   Multiple choice
-   Image-based questions
-   Situation-based questions
-   Ordering steps
-   Identify-the-hazard questions

The quiz should prepare the learner for the practical scenario rather
than exist as an isolated exam.

------------------------------------------------------------------------

# 4. Practical Simulation

This is the primary product differentiator.

The student enters an interactive environment and must respond to a
developing emergency.

Example:

### Earthquake

The student enters a classroom containing:

-   Table
-   Chair
-   Window
-   Door
-   Bookshelf
-   Debris
-   Fire extinguisher
-   Emergency exit

The earthquake begins.

The student must decide what to do.

Example interaction:

``` text
[E] Take Cover
```

Correct action:

``` text
+100
Correct Decision
```

The environment can then change.

For example:

``` text
Earthquake stops
        ↓
Main corridor detected unsafe
        ↓
Student must select an alternate route
```

------------------------------------------------------------------------

# 5. Decision Telemetry

Every meaningful action can be recorded.

Example:

``` text
ACTION
-------------------------
Timestamp: 00:17
Object: Table
Action: Take Cover
Decision: CORRECT
Time Taken: 2.3 sec
Points: +100
```

Another action:

``` text
Timestamp: 00:41
Object: Window
Action: Move Toward Window
Decision: DANGEROUS
Penalty: -100
```

Another:

``` text
Timestamp: 01:12
Object: Exit
Action: Evacuate
Decision: CORRECT
Time Taken: 5.1 sec
Points: +150
```

This creates a behavioral record of the simulation.

------------------------------------------------------------------------

# 6. Decision Severity

Not every mistake should have the same impact.

  Severity        Example                                     Effect
  --------------- ----------------------------------------- --------
  🟢 Correct      Take cover appropriately                      +100
  🟡 Suboptimal   Begin evacuation at an inefficient time        -25
  🟠 Dangerous    Move toward a known hazard                    -100
  🔴 Critical     Select a highly unsafe action                 -250

The exact scoring model should be configurable per disaster scenario and
validated against approved safety guidance.

------------------------------------------------------------------------

# 7. Contextual Feedback

When a learner makes a mistake, the system explains it.

Instead of:

> ❌ Wrong!

show:

> **Why?**\
> This action can expose you to the hazard.

Then:

> **Recommended action:** Follow the scenario's validated emergency
> procedure.

The learner should understand both the mistake and the correct
principle.

------------------------------------------------------------------------

# 8. Branching Scenarios

The simulation should respond to the learner's decisions.

Example:

``` text
Earthquake begins
       |
       +---- Take cover ------> Safe progression
       |
       +---- Run to door -----> Door becomes blocked
       |                            |
       |                            v
       |                     Find alternate exit
       |
       +---- Move to window --> Glass hazard
                                    |
                                    v
                              Time/health penalty
```

This means the student does not simply follow a predetermined animation.

**Their decisions change the scenario.**

------------------------------------------------------------------------

# 9. Stateful Environment

Objects should have meaningful states.

Conceptually:

``` text
Object
 ├── State
 ├── Interactions
 ├── Correct Actions
 ├── Incorrect Actions
 ├── Consequences
 └── Score
```

Example:

### Door

``` text
State:
OPEN / CLOSED / BLOCKED / UNSAFE

Interactions:
Open / Inspect / Avoid

Possible consequences:
Safe exit
Blocked route
Hazard exposure
Alternate route
```

### Fire Extinguisher

``` text
State:
AVAILABLE / USED / UNSUITABLE

Interactions:
Inspect / Select / Use

Possible outcomes:
Correct response
Incorrect selection
Unsafe use
Continue evacuation
```

Objects are therefore part of the scenario engine rather than decorative
assets.

------------------------------------------------------------------------

# 10. Disaster-Specific Mechanics

## Fire

Possible mechanics:

-   Smoke
-   Fire spread
-   Alarm
-   Emergency exit
-   Visibility
-   Door hazards
-   Extinguisher decision
-   Evacuation

## Earthquake

Possible mechanics:

-   Falling objects
-   Structural hazards
-   Drop--Cover--Hold
-   Broken glass
-   Aftershocks
-   Blocked exits

## Flood

Possible mechanics:

-   Rising water
-   Electrical hazards
-   High ground
-   Blocked paths
-   Evacuation

## Chemical/Gas Leak

Possible mechanics:

-   Contaminated areas
-   Wind direction
-   Protective equipment
-   Ventilation
-   Restricted zones
-   Evacuation

Each disaster should test different emergency reasoning instead of
simply reskinning the same level.

------------------------------------------------------------------------

# 11. Adaptive Difficulty

The simulation can adjust difficulty based on performance.

``` text
Easy
  ↓
One primary hazard

Medium
  ↓
Multiple hazards + time pressure

Hard
  ↓
Multiple hazards + blocked route

Expert
  ↓
Compound disaster
```

For example:

``` text
Earthquake
    ↓
Fire starts
    ↓
Exit blocked
    ↓
Aftershock
```

The system can increase complexity for consistently strong learners and
provide simpler scenarios for learners who need more practice.

------------------------------------------------------------------------

# 12. Emergency Decision Score

The primary assessment should not be a conventional gaming score.

Possible dimensions:

``` text
Emergency Decision Score
------------------------
Decision Accuracy
Response Time
Hazard Recognition
Route Selection
Critical Mistakes
Unnecessary Actions
Scenario Completion
```

Example:

``` text
Emergency Decision Score: 847 / 1000

Response Time:       01:47
Correct Decisions:   7 / 9
Critical Mistakes:   1
Unnecessary Actions: 2
```

------------------------------------------------------------------------

# 13. Decision Timeline

After a simulation, the learner sees exactly what happened.

``` text
00:08  🔴 Moved toward window
       Dangerous

00:17  🟢 Took cover
       Correct

00:42  🟢 Waited for shaking to stop
       Correct

01:03  🟡 Approached blocked exit
       Inefficient

01:21  🟢 Used alternate exit
       Correct

01:47  🟢 Reached safe zone
```

This transforms the practical from a game into an assessment and
learning tool.

------------------------------------------------------------------------

# 14. Optimal vs Actual Replay

After completion:

``` text
                 YOUR PATH       IDEAL PATH

Start               ●                ●
                    |                |
                    v                v
                 Window ✗          Table ✓
                    |                |
                    v                v
                  Door ✓           Wait ✓
                    |                |
                    v                v
                 Exit ✗            Exit ✓
```

The learner can replay the simulation and compare:

-   Actual decisions
-   Optimal decisions
-   Time differences
-   Mistakes
-   Consequences

------------------------------------------------------------------------

# 15. Personalized Learning Loop

The platform closes the loop:

``` text
LEARN
  ↓
QUIZ
  ↓
PRACTICAL
  ↓
ASSESS
  ↓
IDENTIFY WEAKNESS
  ↓
RECOMMEND MODULE
  ↓
PRACTICE AGAIN
```

Example:

> Low chemical-hazard identification score detected.

Recommendation:

> **Chemical Leak --- Hazard Identification & Evacuation**

------------------------------------------------------------------------

# MVP

The first version should focus on one polished end-to-end experience.

## MVP Screens

### Student

-   Login
-   Profile
-   Disaster selection
-   Material
-   Quiz
-   Practical
-   Simulation result
-   Decision timeline
-   Replay
-   Recommended learning

### MVP Simulation

Start with **one highly polished disaster**, preferably Fire or
Earthquake.

Required:

-   Interactive environment
-   Timer
-   Player movement
-   Interactive objects
-   Contextual actions
-   Decision tracking
-   Branching consequences
-   Score
-   Severity-based mistakes
-   Final report
-   Replay

After the first scenario works well, add additional disasters.

------------------------------------------------------------------------

# Suggested Technology Stack

## Web Application

-   React / Next.js
-   TypeScript

## Backend

-   Node.js / Express or FastAPI

## Database

-   PostgreSQL

## Real-time / Session State

-   WebSockets / Socket.IO where required

## Simulation

Depending on the desired interaction model:

-   Three.js / React Three Fiber for browser-based 3D
-   Phaser for 2D simulation
-   Unity WebGL for richer 3D simulation

## 3D Assets

-   Blender

## Authentication

-   JWT or managed authentication provider
-   Role-based authorization

------------------------------------------------------------------------

# Suggested Repository Structure

``` text
disasterready/
├── apps/
│   ├── web/
│   └── simulation/
├── backend/
├── database/
├── assets/
│   ├── 3d/
│   ├── images/
│   └── audio/
├── scenarios/
│   ├── fire/
│   ├── earthquake/
│   ├── flood/
│   └── chemical/
├── docs/
│   └── PRD.md
└── README.md
```

------------------------------------------------------------------------

# Long-Term Scope

The product can later support:

-   More disasters
-   More complex environments
-   Multi-user drills
-   Institution-specific scenarios
-   Accessibility modes
-   Regional languages
-   More advanced adaptive simulation
-   AR/VR experiences

These are future extensions, not requirements for the core MVP.

------------------------------------------------------------------------

# Product Principle

The system should prioritize:

**Safety \> Accuracy \> Learning Value \> Usability \> Gamification**

Gamification should improve engagement without rewarding unsafe behavior
or replacing certified emergency training.

------------------------------------------------------------------------

# Final Vision

DisasterReady aims to change disaster education from:

> **"I know what I should do."**

to:

> **"I have practiced what I should do, and I know how I actually
> respond under pressure."**

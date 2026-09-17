# CASE-002 — Teleportation and Visual vs Behavioral Difference

## When Appearance, Geometry, and Action Reachability Disagree

**Repository:** Principle Intelligence and Open Structural Learning
**Case:** CASE-002
**Status:** v1.0.0
**Authors:** Sizhe Tan & GPT-Obot

---

## Abstract

Two states can look close while being behaviorally difficult to connect.

Two states can look far apart while being behaviorally adjacent.

This simple observation exposes a fundamental representation problem.

Many intelligent systems receive observations through visual, geometric, or latent representations. These representations may encode similarity effectively, but similarity in observation space does not automatically equal similarity in action space.

A teleportation environment provides an especially clear example.

Suppose two locations:

```text
A and B
```

are visually far apart.

Ordinary geometry suggests:

```text
VisualDistance(A, B) = Large
```

Yet if stepping onto a teleporter at A immediately moves the agent to B:

```text
BehavioralCost(A → B) = Small
```

Conversely, two locations:

```text
C and D
```

may appear visually adjacent but be separated by an impassable wall:

```text
VisualDistance(C, D) = Small
```

while:

```text
BehavioralCost(C → D) = Large
```

or:

```text
C → D = Unreachable
```

The critical structural lesson is:

> **Visual Difference is not necessarily Behavioral Difference.**

More generally:

> **The geometry useful for perception need not be the geometry useful for action.**

This case develops that observation into a reusable Principle:

> **Behavioral Geometry Principle:**
> When observation-space proximity and action-space reachability disagree, planning should use a representation that preserves task-relevant transition structure rather than relying solely on perceptual or geometric similarity.

The case demonstrates:

```text
Observation
   ↓
Visual / Behavioral Mismatch
   ↓
Differential Evidence
   ↓
Candidate Principle
   ↓
Behavioral Geometry
   ↓
Context-Bound CCC
   ↓
Two-Way Validation
   ↓
Open-LHS Structural Extension
   ↓
Portable Intelligence
```

The deeper implication is that intelligence may need to learn not merely values inside a representation, but **which notion of difference should organize the representation itself**.

---

# 1. The Minimal Environment

Consider four locations:

```text
A
B
C
D
```

Their visual layout is:

```text
A ●                              ● B


          C ● | WALL | ● D
```

From visual geometry:

```text
A and B are far apart.

C and D are close together.
```

Therefore:

```text
VisualDistance(A, B) = Large

VisualDistance(C, D) = Small
```

If planning relies only on visual distance, the system may conclude:

```text
A → B is difficult.

C → D is easy.
```

Now introduce environmental dynamics.

---

# 2. Teleportation

At location A there is a teleporter:

```text
A
↓
Teleport
↓
B
```

The transition requires only one action.

Therefore:

```text
BehavioralCost(A → B) = 1
```

although:

```text
VisualDistance(A, B) = Large
```

The visual geometry and behavioral geometry disagree.

---

# 3. The Wall

Now consider:

```text
C ● | WALL | ● D
```

Visually:

```text
VisualDistance(C, D) = Small
```

But the wall prevents direct movement.

The agent may need to travel around a long route:

```text
C
↓
...
↓
...
↓
...
↓
D
```

or D may be completely unreachable.

Therefore:

```text
BehavioralCost(C → D) = Large
```

or:

```text
BehavioralReachability(C → D) = False
```

Again, visual and behavioral geometry disagree.

---

# 4. The Structural Reversal

We now have:

```text
Visual Space:

A ↔ B = FAR
C ↔ D = NEAR
```

but:

```text
Behavioral Space:

A → B = NEAR
C → D = FAR
```

The ordering has reversed.

This is not merely measurement noise.

It is a structural disagreement between two notions of distance.

---

# 5. Visual Difference

Visual difference answers questions such as:

```text
How different do these observations look?

How far apart are their coordinates?

How different are their image features?

How distant are their visual embeddings?
```

These can be useful questions.

But they do not automatically answer:

```text
How difficult is it to move from one state to another?
```

---

# 6. Behavioral Difference

Behavioral difference may instead depend on:

```text
available actions

transition dynamics

obstacles

one-way passages

teleporters

energy cost

risk

policy

time

control constraints
```

Therefore behavioral distance is task- and dynamics-dependent.

---

# 7. The First Core Distinction

The case immediately produces:

> **Visual Difference ≠ Behavioral Difference**

More generally:

```text
Observation Similarity
        ≠
Action Reachability
```

and:

```text
Geometric Distance
        ≠
Transition Cost
```

in the general case.

---

# 8. Two Geometries

The system is effectively operating with at least two geometries.

## Observation Geometry

```text
What looks close?
```

## Behavioral Geometry

```text
What can be reached easily?
```

These geometries may correlate.

But they need not coincide.

---

# 9. Why Correlation Can Hide the Problem

In ordinary environments:

```text
visually near
```

often approximately means:

```text
easy to reach
```

and:

```text
visually far
```

often means:

```text
expensive to reach
```

Therefore large datasets may strongly reinforce the correlation:

```text
Visual Proximity
≈
Behavioral Proximity
```

Teleportation produces a rare but structurally decisive exception.

---

# 10. The Critical Sample

Suppose the system has observed:

```text
10,000 ordinary transitions
```

where visual and behavioral proximity roughly agree.

Then it observes:

```text
A → B
```

with:

```text
VisualDistance = Large

BehavioralCost = 1
```

This single example may expose a structural weakness in the existing representation.

---

# 11. Sample Count vs Structural Value

The teleporter example may represent:

```text
0.01% of samples
```

yet reveal:

```text
a missing dimension
in the representation.
```

Thus:

```text
Sample Frequency
≠
Structural Importance
```

A rare sample can have high structural leverage.

---

# 12. Sparse Critical Evidence

The key evidence is not:

```text
many examples
```

but:

```text
one or a few examples
that violate a structural assumption.
```

This illustrates:

> **Sparse Critical Evidence**

and:

> **Small-Sample Structural Leverage**

---

# 13. Structural Residual

Suppose the planner predicts:

```text
PredictedCost(A → B) = 100
```

based on visual distance.

Observed:

```text
ActualCost(A → B) = 1
```

Then:

```text
Prediction
     ↓
Observation
     ↓
Large Residual
```

The system should ask:

> Is this merely an error, or does it reveal missing structure?

---

# 14. Model Expectation → Residual → Principle

The pipeline becomes:

```text
Visual Geometry
      ↓
Expected Transition Cost
      ↓
Actual Transition
      ↓
Structural Residual
      ↓
Difference Analysis
      ↓
Candidate Principle
```

This is an important Principle Extraction pattern.

---

# 15. The Wrong Response: Memorize the Exception

A weak response is:

```text
Remember:

A → B costs 1.
```

This solves one case.

But it does not explain:

```text
why
```

nor does it prepare the system for another teleporter.

The knowledge remains local.

---

# 16. The Better Question

The structural learner asks:

> **What relation made A → B cheap despite large visual distance?**

Possible answer:

```text
A has a transition operator
that maps directly to B.
```

Now the intelligence shifts from:

```text
state similarity
```

to:

```text
transition structure
```

---

# 17. Difference Extraction

The system compares:

```text
Expected:
Far visually → expensive behaviorally
```

against:

```text
Observed:
Far visually → cheap behaviorally
```

The critical Difference is:

```text
VisualDistance
does not preserve
BehavioralReachability
```

This is more valuable than the numerical error itself.

---

# 18. Differential Tuple

The evidence can be represented conceptually:

```text
DifferentialTuple {
    source_state: A
    target_state: B

    observation_distance:
        large

    expected_behavioral_cost:
        high

    observed_behavioral_cost:
        low

    transition_structure:
        teleport

    delta:
        visual-behavioral mismatch

    provenance:
        runtime trajectory

    context:
        environment E
}
```

This preserves the structural reason for the mismatch.

---

# 19. The Reverse Example

Now compare C and D.

```text
VisualDistance(C, D) = Small
```

Expected:

```text
BehavioralCost(C → D) = Small
```

Observed:

```text
BehavioralCost(C → D) = Large
```

because of the wall.

Thus the mismatch occurs in both directions:

```text
Visually Far
but Behaviorally Near
```

and:

```text
Visually Near
but Behaviorally Far
```

---

# 20. Why the Pair Is Powerful

The teleporter alone could be treated as:

```text
special shortcut
```

The wall alone could be treated as:

```text
special obstacle
```

Together they expose a more general structure:

> **Observation-space proximity and action-space proximity are distinct relations.**

This is a stronger abstraction.

---

# 21. Difference of Differences

Compare:

```text
A-B:
Visual = Far
Behavior = Near
```

with:

```text
C-D:
Visual = Near
Behavior = Far
```

The difference between these mismatches reveals:

```text
visual geometry
is not the governing geometry
for this planning problem.
```

This is higher-order differential intelligence.

---

# 22. Candidate Principle

The evidence supports a candidate:

> ## Behavioral Geometry Principle
>
> **When observation-space proximity and action-space reachability diverge, planning should preserve task-relevant transition structure rather than relying solely on perceptual or geometric similarity.**

This is a reusable structural hypothesis.

---

# 23. What the Principle Does Not Claim

It does not claim:

```text
visual representations are useless.
```

It does not claim:

```text
Euclidean geometry is wrong.
```

It does not claim:

```text
all planning requires a special metric.
```

Instead:

```text
Representation
must match
the relation required by the task.
```

---

# 24. Perspective Matters

The same pair of states can have multiple valid distances.

For A and B:

```text
Visual Distance:
Large

Behavioral Distance:
Small
```

Neither is necessarily incorrect.

They answer different questions.

This introduces:

> **Perspective-Bound Difference**

---

# 25. Perspective-Bound Difference

A Difference should often carry:

```text
Perspective

Task

Context
```

For example:

```text
Difference(A, B | Visual)
```

may differ from:

```text
Difference(A, B | Behavioral)
```

and:

```text
Difference(A, B | Risk)
```

may differ again.

---

# 26. Difference Is Not a Universal Scalar

A naive architecture asks:

```text
What is the distance between A and B?
```

A structural architecture asks:

```text
Distance with respect to what?
```

Possible answers include:

```text
appearance

reachability

energy

time

risk

policy

causal influence
```

This is a major conceptual upgrade.

---

# 27. Context-Bound Metric

The system may therefore represent:

```text
Metric {
    perspective:
        behavioral reachability

    context:
        environment E

    transition_model:
        current dynamics

    cost:
        action effort
}
```

The metric becomes context-bound rather than universal.

---

# 28. Principle → Metric Selection

The Behavioral Geometry Principle can produce:

```text
IF
planning depends on action reachability

THEN
prefer behavioral transition geometry
over raw visual proximity.
```

The Principle therefore influences representation selection.

---

# 29. Principle as Representation Controller

This is significant.

The Principle does not merely generate:

```text
an answer
```

or:

```text
an action
```

It can select:

```text
which geometry
future reasoning should use.
```

Thus:

```text
Principle
   ↓
Representation Choice
   ↓
Planning
```

---

# 30. Context Binding

Suppose the general Principle is applied to:

```text
Robot R
Maze M
Goal G
```

The Principle binds to this context.

It can now generate a CCC.

---

# 31. CCC-1 — Teleporter

```text
CCC-1

Context:
Robot R planning in Maze M

Condition:
A visually distant target is connected
through a verified low-cost transition

Consequence:
Treat the transition as behaviorally near
for route planning
```

The Principle has become operational.

---

# 32. CCC-2 — Wall

```text
CCC-2

Context:
Robot R planning in Maze M

Condition:
Two visually adjacent states
lack a valid direct transition

Consequence:
Do not treat visual adjacency
as behavioral adjacency
```

Same Principle.

Different context-bound consequence.

---

# 33. Principle as CCC Generator

```text
Behavioral Geometry Principle
              │
       ┌──────┴──────┐
       ▼             ▼
 Teleporter CCC    Wall CCC
       │             │
       ▼             ▼
 Shortcut Use     Barrier Avoidance
```

The Principle is more general than either CCC.

---

# 34. Planning Under Visual Geometry

Suppose:

```text
Start = A

Goal = B
```

Visual planner:

```text
A
↓
long route
↓
...
↓
...
↓
B
```

Estimated cost:

```text
100
```

---

# 35. Planning Under Behavioral Geometry

Behavioral planner:

```text
A
↓
Teleport
↓
B
```

Cost:

```text
1
```

The planner has not become better because it searched longer.

It became better because it searched in a better structural representation.

---

# 36. Representation Can Dominate Search

Suppose Algorithm X explores:

```text
1,000,000 paths
```

in the wrong geometry.

Algorithm Y knows:

```text
A → B
```

is behaviorally adjacent.

Y may solve the task almost immediately.

Therefore:

> **Better representation can outperform more search.**

---

# 37. Representation as Compiled Intelligence

Once the teleporter transition has been incorporated into behavioral geometry:

```text
A
and
B
```

become close in the planning representation.

Future planners no longer need to rediscover the shortcut from scratch.

Thus:

> **Representation can contain compiled action intelligence.**

---

# 38. Structural Compilation

The process is:

```text
Experience:
A → Teleport → B

        ↓

Structural Extraction:
Direct Behavioral Transition

        ↓

Representation Update:
A and B behaviorally near

        ↓

Future Planning:
Reduced Search
```

Past experience has been compiled into future geometry.

---

# 39. Two-Way Validation

But the system should verify the candidate Principle.

Suppose:

```text
A → B
```

was cheap once.

Can it conclude:

```text
A and B are behaviorally near?
```

Not necessarily.

The teleporter may be:

```text
one-way

temporarily active

policy-restricted

energy-dependent

state-dependent
```

Therefore Two-Way validation is required.

---

# 40. Forward Validation

The system tests:

```text
Teleporter Active
      ↓
A → B low cost?
```

If repeatedly supported:

```text
Evidence ↑
```

---

# 41. Reverse Validation

The system also asks:

```text
A → B low cost
      ↓
Why?
```

Possible explanations:

```text
teleporter

hidden corridor

measurement error

planner bug

temporary environment change
```

This prevents premature causal interpretation.

---

# 42. Reverse Reachability

CASE-001 adds another question:

```text
If A → B is cheap,
is B → A also cheap?
```

Perhaps:

```text
A → B = 1

B → A = 100
```

Now CASE-001 and CASE-002 combine.

Behavioral geometry may be both:

```text
non-visual
```

and:

```text
directional
```

---

# 43. Behavioral Geometry May Be Quasimetric

The runtime may need:

```text
q(A, B)
```

where:

```text
q(A, B)
≠
q(B, A)
```

Thus action geometry may depart from both:

```text
visual geometry
```

and:

```text
symmetric geometry
```

at the same time.

---

# 44. Counter-Evidence

Suppose the teleporter becomes disabled.

Previously:

```text
BehavioralCost(A → B) = 1
```

Now:

```text
BehavioralCost(A → B) = 100
```

This is counter-evidence against an unconditional structure:

```text
A and B are always behaviorally near.
```

The Principle must preserve context.

---

# 45. Contextual Specialization

The system revises:

```text
P0:
A and B are behaviorally near.
```

into:

```text
P1:
A and B are behaviorally near
when Teleporter T is active
and available to Agent R.
```

This is better structural knowledge.

---

# 46. State-Conditioned Geometry

Behavioral geometry may therefore depend on:

```text
teleporter state

agent capability

policy

energy

time

environment
```

Thus:

```text
BehavioralDistance(A, B)
```

may actually mean:

```text
BehavioralDistance(
    A,
    B,
    Context
)
```

---

# 47. Geometry Is Dynamic

If context changes:

```text
Teleporter ON
```

then:

```text
A → B = Near
```

If:

```text
Teleporter OFF
```

then:

```text
A → B = Far
```

Therefore the planning geometry itself may change over time.

---

# 48. Dynamic Structural Geometry

This suggests:

> **Action-relevant geometry can be a runtime structure rather than a permanently fixed property of the observation space.**

That is an important Open Structural Learning implication.

---

# 49. The Wrong Compression

Suppose the model tries to force all relations into one embedding.

It may compromise:

```text
visual similarity
```

against:

```text
behavioral reachability
```

and produce an ambiguous representation.

A structural alternative is to preserve multiple explicit relations.

---

# 50. Multi-Perspective Representation

Instead of:

```text
One Universal Distance
```

the system can maintain:

```text
Visual Metric

Behavioral Metric

Risk Metric

Energy Metric

Policy Metric
```

and select or compose them according to task.

---

# 51. Principle-Guided Metric Selection

A Principle may state:

```text
For navigation:
use Behavioral Metric.

For object recognition:
use Visual Metric.

For safety planning:
compose Behavioral + Risk.
```

This makes metric selection itself an intelligence operation.

---

# 52. Composite Difference

Some tasks may require:

```text
CompositeDifference
=
BehavioralCost
+
Risk
+
Energy
+
PolicyConstraint
```

The important point is not the exact formula.

It is that:

> **Difference can be structurally composed according to the task.**

---

# 53. Open-LHS

Suppose the original Principle system contains:

```text
Observation

VisualDistance

Action
```

but no:

```text
TeleportTransition
```

or:

```text
BehavioralReachability
```

The teleporter creates a structural mismatch.

The system asks:

```text
Missing Structure?
```

Answer:

```text
YES
```

---

# 54. Runtime Structural Generation

The runtime may generate:

```text
TransitionShortcut
```

or retrieve a compatible structure:

```text
BehavioralReachabilityMetric
```

Then:

```text
New Structure
    ↓
UTN Identity
    ↓
Interface Check
    ↓
Open-LHS Binding
```

The vocabulary has grown.

---

# 55. Before and After Open-LHS

Before:

```text
LHS {
    VisualState
    VisualDistance
    Action
}
```

After:

```text
LHS {
    VisualState
    VisualDistance
    BehavioralReachability
    TeleportTransition
    Action
}
```

The system has acquired new structural objects.

---

# 56. Principle Formation with the New LHS

The runtime can now express:

```text
TeleportTransition(A, B)
+
BehavioralReachabilityMetric
+
Goal(B)
→
PreferDirectTransition
```

This relation could not be expressed cleanly before the new structures existed.

---

# 57. Reasoning Creates the Representation It Needs

This demonstrates the PI-003 thesis:

> **Reasoning may create the representational structures required for its own reasoning.**

The teleporter exposes a missing concept.

The system creates or imports the concept.

The concept becomes part of future reasoning.

---

# 58. From Structural Residual to New Vocabulary

The complete transition is:

```text
Unexpected Cheap Transition
        ↓
Structural Residual
        ↓
Visual Geometry Insufficient
        ↓
Missing Behavioral Relation
        ↓
Generate Structure
        ↓
BehavioralReachability
        ↓
Open-LHS
```

The error has produced vocabulary growth.

---

# 59. Principle + New Structure

Now the candidate Principle can be expressed more precisely:

```text
IF
VisualDistance and BehavioralReachability diverge

THEN
Planning geometry should preserve
BehavioralReachability
for action-oriented tasks.
```

The new structure improves the Principle itself.

---

# 60. Principle Evolution

The lifecycle may be:

```text
P0:
Nearby appearance implies nearby action.

        ↓
Teleporter / Wall Evidence

P1:
Visual proximity does not guarantee
behavioral proximity.

        ↓
Context Evidence

P2:
Planning should use context-bound
behavioral reachability
when visual and behavioral geometry diverge.
```

The Principle becomes progressively more precise.

---

# 61. Counter-Evidence Improves the Geometry

Suppose most visual neighbors are behaviorally reachable.

That is not counter-evidence against P2.

P2 does not claim:

```text
visual distance is never useful.
```

It claims:

```text
visual distance should not be assumed
to universally determine action reachability.
```

Scope matters.

---

# 62. Avoiding Overcorrection

After discovering teleportation, the system should not conclude:

```text
Ignore visual geometry.
```

That would replace one bad universal assumption with another.

A better system preserves both:

```text
Visual Geometry
+
Behavioral Geometry
```

and learns when each is relevant.

---

# 63. Principle Intelligence as Perspective Governance

The deeper role of Principle Intelligence becomes:

```text
Which representation
should govern this decision?
```

This is not merely prediction.

It is structural perspective selection.

---

# 64. Perspective Error

A system can have accurate data but choose the wrong perspective.

For example:

```text
VisualDistance(A, B) = 100
```

may be perfectly correct.

The error occurs when the system uses that value to answer:

```text
How hard is A → B?
```

Thus:

> **A correct measurement can produce an incorrect decision when bound to the wrong structural perspective.**

---

# 65. Perspective-Binding Principle

A reusable Principle may therefore be:

> **A difference measure should be interpreted only within the perspective and task relation for which it preserves relevant structure.**

This is broader than the teleporter example.

---

# 66. Principle Hierarchy

The case may therefore produce two Principles:

```text
P1:
Behavioral Geometry Principle
```

and a more general:

```text
P0:
Perspective-Bound Difference Principle
```

where:

```text
P0
 ↓
P1
```

P1 is a specialization of P0.

---

# 67. Knowledge Root Growth

The root system may become:

```text
Perspective-Bound Difference
          │
          ├── Visual Difference
          │
          ├── Behavioral Difference
          │
          ├── Risk Difference
          │
          └── Policy Difference
```

The teleporter case has generated a larger structural family.

---

# 68. Principle as Knowledge Root

The Behavioral Geometry Principle can generate:

```text
Behavioral Metric

Teleport CCC

Barrier CCC

Route Trigger

Reachability Test

Counter-Evidence Search

PIRP

PIRU
```

Thus it becomes a reusable Knowledge Root.

---

# 69. PIRP Externalization

The learned behavioral metric may be externalized as:

```text
PIRP-Behavioral-Reachability
```

with:

```text
identity

metric semantics

context requirements

evidence

interface

validation state
```

This makes the structural discovery portable.

---

# 70. PIRU Externalization

If runtime computation is included:

```text
Input:
State A
State B
Context C

Output:
Behavioral reachability
Transition cost
Evidence trace
```

the structure may become:

```text
PIRU-Behavioral-Reachability-Evaluator
```

---

# 71. Agent-to-Agent Transfer

Agent A discovers:

```text
Visual proximity
≠
Behavioral proximity
```

and produces PIRU-X.

Agent B later encounters a different environment containing:

```text
wormholes

elevators

one-way gates

moving platforms
```

Agent B can import X.

---

# 72. UTN Recognition

Agent B does not need to know the history of Agent A's original teleporter.

It can inspect:

```text
Identity:
Behavioral-Reachability-Evaluator

Type:
Metric / Evaluator

Context:
Action Planning

Interface:
State × State × Context
→ Reachability
```

and determine whether X is structurally compatible.

---

# 73. Open-LHS Binding

Agent B can bind:

```text
PIRU-X
```

into:

```text
Principle LHS
```

alongside:

```text
local observation

local trajectory

local policy
```

The new structure immediately participates in reasoning.

---

# 74. Collective Learning

Agent B may discover a new case:

```text
MovingPlatform
```

where reachability changes periodically.

Now:

```text
BehavioralDistance(A, B, t)
```

depends on time.

Agent B contributes:

```text
Temporal Reachability Evidence
```

back to the shared Principle.

---

# 75. Principle Evolution Across Agents

The Principle may evolve:

```text
P-v1:
Visual ≠ Behavioral

P-v2:
Behavioral reachability is context-bound

P-v3:
Behavioral reachability can be directional

P-v4:
Behavioral reachability can be time-dependent
```

The Knowledge Root grows through distributed evidence.

---

# 76. Collective Structural Growth

Agent A discovered:

```text
Teleportation
```

Agent B discovered:

```text
Temporal Transition
```

Agent C may discover:

```text
Policy-Restricted Transition
```

Together:

```text
Behavioral Geometry
=
Dynamics
+
Direction
+
Time
+
Policy
+
Context
```

The collective representation becomes richer than any individual discovery.

---

# 77. Fold Back

The cycle becomes:

```text
Agent A
 ↓
Principle
 ↓
PIRU
 ↓
Agent B
 ↓
New Context
 ↓
Counter-Evidence / Extension
 ↓
Fold Back
 ↓
Principle Revision
```

Portable intelligence becomes evolvable intelligence.

---

# 78. Open Structural Learning

Initially the system possesses:

```text
Visual Geometry
```

After experience it acquires:

```text
Behavioral Geometry
```

Later:

```text
Directional Behavioral Geometry
```

Later:

```text
Temporal Behavioral Geometry
```

The representational space itself is growing.

---

# 79. Not Just Better Parameters

This is not merely:

```text
Weight 0.4
→
Weight 0.7
```

The system has learned that:

```text
a different relation
must exist.
```

That is structural growth.

---

# 80. Learning a New Dimension

The system originally organizes states according to:

```text
appearance
```

It later adds:

```text
reachability
```

This is equivalent to learning a new structural dimension.

---

# 81. Dimension Growth

Conceptually:

```text
Representation R0:

State
+
Visual Distance
```

becomes:

```text
Representation R1:

State
+
Visual Distance
+
Behavioral Reachability
```

and perhaps:

```text
Representation R2:

State
+
Visual Distance
+
Directional Reachability
+
Temporal Reachability
+
Risk
```

The representation evolves with experience.

---

# 82. Why This Matters for Open-Ended Growth

If all useful dimensions must be specified before training:

```text
Future Intelligence
⊆
Current Vocabulary
```

If new structural dimensions can emerge:

```text
Future Intelligence
=
Current Vocabulary
+
Validated Structural Novelty
```

This is Open Structural Learning.

---

# 83. Search Within Space vs Growth of Space

Before:

```text
Search routes
inside Visual Geometry.
```

After:

```text
Create Behavioral Geometry
then search within it.
```

The second process changes the search substrate.

---

# 84. A Small Example of Structural Possibility-Space Growth

Before teleporter discovery:

```text
Possible Planning Relation:

Spatial Neighbor
```

After:

```text
Possible Planning Relations:

Spatial Neighbor

Behavioral Neighbor
```

The system can now express a distinction that previously did not exist.

---

# 85. Intelligence Growth

The important growth event is therefore:

```text
not:
A → B shortcut learned
```

but:

```text
new relation:
Behavioral Neighbor
```

Once created, that relation can be applied to many future environments.

---

# 86. The Teleporter Is a Trigger, Not the Theory

Teleportation is intentionally extreme.

Its purpose is to expose a general principle cleanly.

The same structural issue appears with:

```text
doors

bridges

elevators

roads

currents

slopes

one-way systems

permissions

network routes

workflow transitions
```

Teleportation simply makes the mismatch impossible to ignore.

---

# 87. Beyond Navigation

The same pattern appears in software.

Two functions may look syntactically similar:

```text
Visual / Surface Similarity = High
```

but have very different behavioral consequences.

Conversely, two implementations may look very different while producing equivalent behavior.

Thus:

```text
Surface Similarity
≠
Behavioral Equivalence
```

---

# 88. Calling Graph Example

Two code nodes may be textually distant but connected by:

```text
one critical call
```

making them behaviorally close in execution.

Two adjacent source files may have no runtime interaction.

Again:

```text
File Proximity
≠
Execution Reachability
```

The Principle transfers.

---

# 89. Policy Example

Two actions may appear operationally similar.

But:

```text
Action A
```

may be policy-permitted while:

```text
Action B
```

is prohibited.

Therefore:

```text
Operational Similarity
≠
Policy Proximity
```

Another perspective-specific geometry appears.

---

# 90. Knowledge Example

Two concepts may be semantically similar but require very different evidence to justify.

Thus:

```text
Semantic Similarity
≠
Evidence Equivalence
```

Again, the task determines the relevant difference.

---

# 91. General Principle

The broadest reusable form is:

> ## Task-Relevant Geometry Principle
>
> **The geometry used by an intelligence system should preserve the relations relevant to the task being solved; proximity in one representation should not automatically be treated as proximity in another.**

Behavioral Geometry is one important specialization.

---

# 92. Principle Family

```text
Task-Relevant Geometry Principle
              │
      ┌───────┼─────────┐
      ▼       ▼         ▼
 Behavioral  Risk     Evidence
 Geometry   Geometry   Geometry
      │
      ▼
Directional / Temporal
Reachability
```

This demonstrates Knowledge Root expansion.

---

# 93. Structural Learning vs Memorization

Memorization:

```text
A teleports to B.
```

Structural Learning:

```text
Transition structure can override
observation-space proximity.
```

Principle Intelligence:

```text
When observation and action geometry diverge,
bind planning to the geometry
that preserves behavioral reachability.
```

Open Structural Learning:

```text
If that geometry does not yet exist,
create or import it.
```

---

# 94. The Full Case Pipeline

```text
VISUAL WORLD

A ------------------------- B
Far

C | WALL | D
Near

        ↓

RUNTIME EXPERIENCE

A → Teleport → B
Cheap

C → Wall → ... → D
Expensive

        ↓

DIFFERENTIAL EVIDENCE

Visual Far
but
Behavior Near

Visual Near
but
Behavior Far

        ↓

STRUCTURAL RESIDUAL

Visual Geometry
does not preserve
Action Reachability

        ↓

CANDIDATE PRINCIPLE

Behavioral Geometry Principle

        ↓

CONTEXT BINDING

        ↓

CCC

        ↓

TWO-WAY VALIDATION

        ↓

COUNTER-EVIDENCE

        ↓

CONTEXT-BOUND
BEHAVIORAL METRIC

        ↓

OPEN-LHS

        ↓

PIRP / PIRU

        ↓

COLLECTIVE LEARNING

        ↓

NEW STRUCTURAL DIMENSIONS
```

---

# 95. Relationship to CASE-001

CASE-001 showed:

```text
A → B
≠
B → A
```

Therefore:

```text
Direction Matters
```

CASE-002 shows:

```text
VisualDistance(A, B)
≠
BehavioralDistance(A, B)
```

Therefore:

```text
Perspective Matters
```

Together:

```text
Difference
=
Perspective-Bound
+
Potentially Directional
+
Context-Bound
```

This is a much richer notion than Euclidean subtraction.

---

# 96. Combined Principle

CASE-001 and CASE-002 together suggest:

> **Action-relevant difference should preserve the directional, contextual, and transition-dependent structure required by the task rather than being assumed to follow visual or symmetric geometry.**

This is a strong structural foundation for Principle Intelligence.

---

# 97. Relationship to PI-002

This case demonstrates:

```text
Sparse Critical Evidence
      ↓
Structural Residual
      ↓
New Principle
```

A rare teleporter can expose a representation error that thousands of ordinary transitions do not reveal.

---

# 98. Relationship to PI-003

The system may initially lack:

```text
BehavioralReachability
```

as a structural object.

Runtime experience creates the need.

The system generates or retrieves the missing structure and binds it into Open-LHS.

Thus:

> **The vocabulary itself can grow.**

---

# 99. Relationship to PI-004

The Behavioral Geometry Principle generates context-specific CCCs:

```text
Teleporter CCC

Wall CCC

Return-Path CCC
```

Two-Way CCC then tests whether the structural relation holds in the current context.

---

# 100. Relationship to PI-005

Counter-evidence may reveal:

```text
teleporter disabled

agent unauthorized

transition directional

transition time-dependent
```

forcing Principle specialization.

The Principle remains falsifiable and evolvable.

---

# 101. Relationship to PI-006

The mature Principle becomes a Knowledge Root with:

```text
identity

scope

perspective

evidence

counter-evidence

derived metrics

derived CCCs

revision history
```

It can generate multiple downstream structures.

---

# 102. Relationship to PI-007

The behavioral metric can become:

```text
PIRP
```

or:

```text
PIRU
```

and move between agents.

New environments provide additional evidence that can Fold Back into the shared Principle.

---

# 103. Relationship to PI-008

The system begins with one geometry:

```text
Visual Geometry
```

and learns another:

```text
Behavioral Geometry
```

It has expanded the structural possibility space available to future reasoning.

This is a concrete instance of Open Structural Learning.

---

# 104. The Deepest Lesson

The deepest lesson is not:

```text
Teleporters make paths shorter.
```

It is:

> **The representation in which two states appear close is not necessarily the representation in which they are close for action.**

This distinction reaches far beyond navigation.

---

# 105. Representation Is a Perspective

A representation emphasizes some relations and suppresses others.

Therefore every representation implicitly answers:

```text
What differences matter?
```

Principle Intelligence can make this question explicit.

---

# 106. Learning What Difference Means

A conventional learner may learn:

```text
the value of d(A, B)
```

A deeper learner may discover:

```text
d is the wrong relation.
```

This is a much larger intelligence event.

---

# 107. From Value Learning to Relation Learning

The transition is:

```text
Learn Value
```

to:

```text
Learn Relation
```

to:

```text
Learn Which Relation Matters
```

This progression captures the structural significance of the case.

---

# 108. Small Delta Intelligence

A single surprising transition:

```text
A → B
```

may reveal that an entire geometry is inappropriate.

Thus:

```text
Small Delta
   ↓
New Relation
   ↓
New Geometry
   ↓
New Planning Space
```

This is Small Delta Intelligence with large representational leverage.

---

# 109. Intelligence Before Full Explanation

The agent may initially know only:

```text
A → B is unexpectedly cheap.
```

It may not yet know:

```text
why the teleporter works.
```

Nevertheless, the structural relation:

```text
A → B is behaviorally near
```

can already improve planning.

Thus:

> **Useful structural intelligence can precede complete mechanistic explanation.**

---

# 110. Later Explanation

Later the system may discover:

```text
Teleport Device T
```

and refine the Principle.

Thus:

```text
Operational Structure
      ↓
Mechanistic Explanation
```

can be a legitimate learning trajectory.

---

# 111. Evidence Must Remain Attached

Because explanation may be incomplete, the system should preserve:

```text
what was observed

under what context

with what confidence

what alternatives exist
```

This prevents useful operational structure from being mistaken for universal truth.

---

# 112. Open Structural Learning Requires Epistemic Humility

A newly created metric should be represented as:

```text
current best structural model
```

not:

```text
final geometry of reality
```

Future evidence may reveal another perspective.

---

# 113. Geometry Can Continue Growing

Today:

```text
Visual
+
Behavioral
```

Tomorrow:

```text
Visual
+
Behavioral
+
Risk
```

Later:

```text
Visual
+
Behavioral
+
Risk
+
Policy
+
Temporal
```

There need not be a permanently final list.

---

# 114. Structural Possibility-Space Growth

Each new relation allows questions that were previously difficult or impossible to formulate explicitly.

Before:

```text
Which state looks closer?
```

After:

```text
Which state is behaviorally easier to reach?
```

Later:

```text
Which state is behaviorally reachable
under current risk and policy constraints?
```

The question space itself grows.

---

# 115. Intelligence Growth Through New Questions

A new structural dimension does more than improve answers.

It enables new questions.

Therefore:

> **Growth of representation can produce growth of inquiry.**

This is another form of Open-Ended Structural Growth.

---

# 116. Case Thesis

The central thesis of CASE-002 is:

> **Appearance does not determine reachability.**

When:

```text
Visual Geometry
```

and:

```text
Behavioral Geometry
```

diverge, the difference is not merely an error to be averaged away.

It may reveal that the intelligence system is using the wrong structural relation.

Sparse critical evidence can expose that mismatch.

Principle Intelligence can convert the mismatch into a reusable Knowledge Root.

Open-LHS can admit the newly required relation.

Runtime Structural Generation can create or retrieve a behavioral metric.

PIRP/PIRU can externalize it.

Collective Learning can refine it across agents and contexts.

The result is not merely a better route.

It is a better structural language for describing action.

---

# 117. Compact Case Formula

```text
Visual Far
+
Behavior Near
        │
        ▼
Structural Mismatch

Visual Near
+
Behavior Far
        │
        ▼
Structural Mismatch

        ↓

Visual Difference
≠
Behavioral Difference

        ↓

Behavioral Geometry Principle

        ↓

Task-Relevant Metric

        ↓

CCC

        ↓

Two-Way Validation

        ↓

Open-LHS

        ↓

PIRP / PIRU

        ↓

Collective Structural Growth
```

---

# 118. Final Insight

A system may know exactly where two states are and still misunderstand how they relate.

It may measure their visual distance perfectly and still plan badly.

The failure is not necessarily in measurement.

It may be in the choice of relation.

Therefore the deeper intelligence problem is not always:

```text
How accurately can we measure distance?
```

Sometimes it is:

```text
Which distance deserves to exist
for this task?
```

That question moves intelligence from parameter estimation toward structural learning.

---

## Repository Case Thesis

```text
Visual proximity
is not necessarily
behavioral proximity.

Behavioral proximity
is not necessarily
symmetric.

Difference is therefore
perspective-bound,
context-bound,
and potentially directional.

A rare transition can expose
a missing relation.

A missing relation can become
a new structural object.

A new structural object can enter
Open-LHS.

A validated structural object
can become portable intelligence.

Portable intelligence can acquire
new evidence across agents.

The resulting Principle can continue
to specialize and grow.
```

> **The important question is not only how far apart two states are. It is: far apart according to which structure, for which task, under which dynamics?**

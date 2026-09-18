# PI-002 — Sparse Evidence, Differential Intelligence, and Principle Extraction

## From Critical Differences to Reusable Structural Knowledge

**Repository:** Principle Intelligence and Open Structural Learning
**Document:** PI-002
**Status:** v1.0.0
**Authors:** Sizhe Tan & GPT-Obot

---

## Abstract

Modern machine learning has demonstrated extraordinary power by extracting statistical regularities from large datasets. However, many important intelligence problems do not arrive as large, representative, independently sampled datasets.

They arrive as rare failures, unusual transitions, asymmetric actions, anomalies, counterexamples, policy violations, sudden environmental changes, or a small number of highly informative observations.

In such settings, sample count alone is a poor measure of informational value.

A single transition may reveal irreversibility.

One failure may expose a hidden constraint.

Two trajectories may reveal a previously invisible behavioral difference.

A single counterexample may invalidate a broad generalization.

A rare structural discontinuity may matter more than millions of ordinary observations.

This document develops **Differential Intelligence** as a foundation for Principle Intelligence.

The central hypothesis is:

> **As evidence becomes sparse, the value of explicit structural leverage can increase.**

Rather than relying only on statistical regularity across many samples, an intelligent system can ask:

* What changed?
* What remained invariant?
* Which difference matters?
* Which relation became asymmetric?
* Which constraint was exposed?
* Which expected transition failed?
* Which observation is structurally inconsistent with the current explanation?

These questions transform observations into **differential evidence**.

Differential evidence can then support the formation of candidate Principles: reusable structural invariants, constraints, directional relations, or regularities intended to generalize beyond the observations that produced them.

The resulting pipeline is:

```text
Observation
    ↓
Localization
    ↓
Difference
    ↓
Differential Evidence
    ↓
Structural Compression
    ↓
Candidate Principle
```

The purpose is not to replace statistical learning.

It is to complement statistical learning with a structural learning regime capable of extracting disproportionate intelligence from small numbers of critical differences.

---

# 1. The Sample-Count Illusion

Machine learning often treats sample quantity as a central resource.

This is reasonable.

More representative observations can reduce uncertainty, expose regularities, improve estimation, and support generalization.

But sample count and structural information are not the same thing.

Consider two datasets.

Dataset A contains one million observations of essentially the same successful behavior.

Dataset B contains:

* one successful transition,
* one failed reverse transition,
* one obstacle-induced detour,
* and one unexpected shortcut.

Dataset A may provide stronger statistical confidence about the common behavior.

Dataset B may reveal more about the **structure of the environment**.

This suggests a distinction:

> **Statistical information density and structural information density are different quantities.**

A rare sample can have low frequency but high structural value.

---

# 2. Dense Evidence and Sparse Critical Evidence

Two broad learning regimes can therefore be distinguished.

## 2.1 Dense-Evidence Learning

When many representative samples are available:

```text
Large Sample Set
      ↓
Statistical Regularity
      ↓
Parameter Estimation
      ↓
Prediction / Classification / Generation
```

This is a major strength of modern neural learning.

## 2.2 Sparse Critical Evidence

When only a small number of structurally important observations are available:

```text
Rare Observation
      ↓
Difference
      ↓
Constraint / Failure / Asymmetry
      ↓
Structural Hypothesis
      ↓
Candidate Principle
```

The important variable changes.

Instead of asking primarily:

> How frequently does this pattern occur?

the system asks:

> What structural fact does this observation expose?

These regimes are complementary.

A capable intelligence system should be able to use both.

---

# 3. Structural Leverage

We define **Structural Leverage** informally as:

> **The amount of reusable structural knowledge that can be extracted from a limited amount of evidence.**

A highly redundant observation may have low structural leverage.

A rare observation that exposes a new invariant or constraint may have high structural leverage.

Conceptually:

```text
Observation Count ≠ Structural Value
```

and:

```text
Rare Evidence
     +
Critical Difference
     ↓
High Structural Leverage
```

This motivates a working heuristic:

> **Sample ↓ does not imply Intelligence ↓ if Structural Leverage ↑.**

This is not a universal law.

Some problems genuinely require many observations.

The point is narrower:

> Small-sample learning becomes substantially more powerful when the system can identify which differences carry reusable structure.

---

![Fig-003 — Sparse Evidence to Principle](../figures/Fig-003-Sparse-Evidence-to-Principle.png)

**Fig-003 — Sparse Evidence to Principle.**  
Sparse observations can contain structurally important differences. Differential extraction, residual analysis, and localization can elevate critical evidence into a Candidate Principle.

---

# 4. Difference as an Intelligence Primitive

A raw observation tells the system what occurred.

A difference can reveal what matters.

Suppose a robot observes:

```text
State A
State B
```

Knowing both states is useful.

But the transition:

```text
A → B
```

introduces additional information.

Now suppose the reverse transition is attempted:

```text
B → A
```

and fails.

The pair:

```text
A → B : easy
B → A : difficult
```

contains a structural fact that neither state independently contains.

The intelligence is in the **relation**.

This motivates a central proposition:

> **Difference is not merely a preprocessing operation. Difference can itself be an intelligence primitive.**

---

# 5. Difference Is Broader Than Subtraction

The term "difference" should not be interpreted as ordinary numerical subtraction.

A difference can exist in many representational spaces.

Examples include:

```text
Euclidean Difference
Metric Difference
Quasimetric Difference
Temporal Difference
State-Transition Difference
Behavioral Difference
Trajectory Difference
Policy Difference
Constraint Difference
Evidence Difference
Causal Difference
Counterfactual Difference
Semantic Difference
Context-Bound Difference
```

The appropriate difference depends on the problem.

Two states can be close in one space and far apart in another.

For example:

```text
Visual Distance(A,B) = small

but

Reachability Distance(A,B) = large
```

or:

```text
Reachability(A → B) = easy

but

Reachability(B → A) = difficult
```

Therefore:

> **Difference is perspective-, context-, and task-dependent.**

---

# 6. Similarity Is Not Reachability

This distinction is particularly important for embodied intelligence.

Two observations may look nearly identical while requiring radically different actions.

Consider two points separated by a transparent wall.

In image space:

```text
Visual Difference ≈ small
```

In action space:

```text
Direct Reachability = impossible
```

The agent may need to travel around the wall.

Therefore:

```text
Visual Similarity
      ≠
Behavioral Similarity
      ≠
Transition Cost
```

This is not merely a robotics problem.

The same distinction appears in:

* software execution,
* financial states,
* biological systems,
* policy systems,
* social behavior,
* causal reasoning,
* and planning.

A useful intelligence architecture must therefore resist the temptation to collapse all differences into one universal similarity measure.

---

# 7. Directional Difference

Many real-world relations are asymmetric.

For a symmetric metric:

```text
d(A,B) = d(B,A)
```

But many action costs satisfy:

```text
Cost(A → B) ≠ Cost(B → A)
```

Examples include:

```text
jump down ≠ climb back up

accelerate ≠ stop under identical conditions

deploy software ≠ restore previous state

break object ≠ reconstruct object

spend resource ≠ recover resource
```

This suggests another important source of Principle formation:

> **Directional asymmetry can itself be differential evidence.**

A small number of asymmetric transitions may support a candidate Principle such as:

```text
Transition costs in this environment may be directional.
```

The Principle is more reusable than the individual transition.

---

# 8. Differential Evidence

Not every observed difference should become a Principle.

We therefore distinguish:

```text
Difference
```

from:

```text
Differential Evidence
```

A **Difference** is an observed distinction.

**Differential Evidence** is a difference judged to be structurally relevant to a candidate relation, constraint, invariant, or Principle.

For example:

```text
Observation:
Robot position changed by 2 mm.
```

This may be a difference.

But if it does not affect planning, control, safety, or any relevant hypothesis, it may have little structural value.

By contrast:

```text
Observation:
The same command succeeds before contact
but fails after contact.
```

may reveal a hidden state transition or constraint.

Thus:

> **Differential Intelligence requires selection, not merely subtraction.**

---

# 9. Localization Before Principle Extraction

A critical difference is often local.

The entire system does not change.

One region changes.

One transition fails.

One branch becomes inconsistent.

One policy constraint activates.

One trajectory diverges.

Therefore Principle extraction benefits from **Localization**.

A minimal pipeline becomes:

```text
Observation
    ↓
Unexpected Result
    ↓
Localization
    ↓
Relevant Region
    ↓
Difference Extraction
    ↓
Differential Evidence
```

Localization reduces the search space.

Instead of asking:

> What explains the entire world?

the system asks:

> Where did the important structural change occur?

This is a major source of computational leverage.

---

# 10. Difference Before Explanation

Intelligent systems often attempt to generate explanations too early.

But explanation can be expensive and premature.

A more conservative pipeline is:

```text
Observe
  ↓
Locate
  ↓
Differentiate
  ↓
Preserve Evidence
  ↓
Form Candidate Relation
  ↓
Explain if useful
```

This ordering matters.

A system can detect:

```text
A → B works
B → A fails
```

without yet knowing why.

The asymmetry itself is useful.

Therefore:

> **Useful structural intelligence can precede complete explanation.**

This is especially important in sparse-data environments.

Waiting for a complete causal theory may delay the use of an already valuable structural constraint.

---

# 11. From Differential Evidence to Candidate Relation

Suppose an agent observes:

```text
Observation 1:
A → B succeeds.

Observation 2:
B → A requires substantially greater cost.

Observation 3:
C → D succeeds.

Observation 4:
D → C also requires substantially greater cost.
```

The agent can compress these observations into a candidate relation:

```text
Forward and reverse transition costs may differ.
```

This is already more useful than storing four isolated observations.

The next compression is:

```text
Candidate Principle:
Transition cost may be directional.
```

The progression is:

```text
Observation
    ↓
Difference
    ↓
Repeated / Critical Relation
    ↓
Structural Compression
    ↓
Candidate Principle
```

Principle extraction can therefore be understood partly as a form of **structural compression**.

---

# 12. Structural Compression

Statistical compression asks whether many observations can be represented by a smaller statistical model.

Structural compression asks whether multiple observations can be represented by a reusable relation.

For example:

```text
A → B expensive
C → D expensive
E → F expensive
```

may compress into:

```text
Transitions crossing structural boundary X are expensive.
```

The compression is valuable if the Principle helps with future cases.

Thus:

> **A good Principle compresses evidence while preserving actionable structural distinctions.**

This is closely related to Folding.

But Principle extraction adds an important requirement:

> The folded structure should remain identifiable and reusable as an explicit intelligence object.

---

# 13. Principle Extraction as Hypothesis Formation

A candidate Principle should not be confused with a proven truth.

The extraction process is closer to hypothesis formation.

Conceptually:

```text
Differential Evidence
        ↓
Pattern Candidate
        ↓
Structural Abstraction
        ↓
Candidate Principle
```

The candidate may later be:

```text
supported
specialized
weakened
merged
split
rejected
```

This separation is essential.

Otherwise, a system may turn every observed difference into an overgeneralized rule.

Principle Intelligence therefore separates:

```text
Principle Formation
```

from:

```text
Principle Validation
```

The latter will be developed in subsequent documents.

---

# 14. Minimal Principle Extraction Skeleton

A preliminary extraction skeleton can be written as:

```text
INPUT:
    observations
    context
    current structures

STEP 1:
    Localize relevant observations.

STEP 2:
    Compute or retrieve relevant differences.

STEP 3:
    Rank differences by structural significance.

STEP 4:
    Search for invariants, constraints,
    asymmetries, repeated relations,
    or discontinuities.

STEP 5:
    Compress selected differential evidence
    into a candidate structural relation.

STEP 6:
    Bind provenance and scope.

STEP 7:
    Emit Candidate Principle.

OUTPUT:
    Candidate Principle
    Supporting Evidence
    Context
    Scope
    Uncertainty
```

This is deliberately abstract.

Different domains may implement each stage differently.

---

# 15. What Makes a Difference Structurally Significant?

A useful system requires some mechanism for distinguishing important differences from noise.

Several signals may increase structural significance.

## 15.1 Prediction Failure

```text
Expected:
A → B

Observed:
A → C
```

The discrepancy may expose missing structure.

## 15.2 Directional Asymmetry

```text
A → B ≠ B → A
```

This may reveal irreversible or directional dynamics.

## 15.3 Constraint Activation

```text
Action succeeds
until condition X appears.
```

This may reveal a hidden boundary.

## 15.4 Counterexample

```text
Current belief predicts success.

One observation produces failure.
```

A single counterexample may have high structural value.

## 15.5 Trajectory Divergence

Two trajectories begin similarly but produce different outcomes.

The divergence point may localize an important structural difference.

## 15.6 Context Shift

The same action produces different outcomes under different contexts.

This may indicate a Context-Bound Principle.

## 15.7 Unexpected Shortcut

A transition believed to require many steps becomes possible in one step.

This may reveal a new edge in the behavioral topology.

---

# 16. Failure as High-Value Evidence

Failures are often treated merely as negative samples.

Principle Intelligence treats some failures differently.

A failure can reveal:

* a boundary,
* a missing condition,
* an incorrect assumption,
* a hidden variable,
* a directional constraint,
* a policy conflict,
* or an invalid Principle.

Therefore:

> **Failure can be structurally richer than ordinary success.**

If one million actions succeed under normal conditions, those successes may confirm an existing structure.

A single unusual failure may reveal an entirely new branch.

Conceptually:

```text
Success × 1,000,000
        ↓
Confidence in known structure
```

while:

```text
Unexpected Failure × 1
        ↓
Candidate new structure
```

The two forms of evidence serve different purposes.

---

# 17. Counterexamples and Small-Sample Intelligence

Counterexamples are especially important because their value is not proportional to frequency.

Suppose a system believes:

```text
All states satisfying X permit action A.
```

One verified state:

```text
X is true
but
A fails
```

may be sufficient to reject the universal formulation.

This demonstrates an important property of structural learning:

> **Some evidence has asymmetric epistemic value.**

A thousand confirming observations and one valid counterexample are not necessarily equivalent evidence units.

Principle Intelligence therefore needs to reason about the **role** of evidence, not merely its quantity.

---

# 18. Observation Value Is Principle-Dependent

There is no globally important observation.

An observation becomes important relative to a question or candidate structure.

For Principle P:

```text
Evidence E1 may be critical.
```

For Principle Q:

```text
the same E1 may be irrelevant.
```

Therefore evidence value is contextual:

```text
Evidence Value
    =
f(
  Principle Candidate,
  Context,
  Difference Type,
  Structural Role
)
```

No specific mathematical form is assumed here.

The point is architectural:

> **Evidence selection should be bound to the structural question being investigated.**

---

# 19. Context-Bound Differential Intelligence

The same difference can imply different Principles in different contexts.

For example:

```text
A → B fails
```

could mean:

* physical obstruction,
* insufficient energy,
* policy prohibition,
* temporary environmental condition,
* missing prerequisite,
* or incorrect state estimation.

Therefore Principle extraction should preserve context.

Conceptually:

```text
Difference
   +
Context
   ↓
Differential Evidence
```

rather than:

```text
Difference
   ↓
Universal Rule
```

This prevents premature universalization.

---

# 20. Baseline-Preserved Difference

A difference becomes more meaningful when the baseline is preserved.

Instead of storing only:

```text
Delta = changed feature
```

retain:

```text
Baseline
   +
Delta
   +
Result
```

For example:

```text
Before:
door unlocked

Action:
push

Result:
opens
```

versus:

```text
Before:
door locked

Action:
push

Result:
fails
```

The useful structure is not simply:

```text
open vs fail
```

It is the relationship among:

```text
Baseline
Action
Delta
Outcome
```

This supports more precise Principle formation.

---

# 21. Differential Tuples

A useful conceptual object is a **Differential Tuple**.

For example:

```text
DifferentialTuple {
    baseline
    context
    action_or_transition
    expected_result
    observed_result
    delta
    outcome
    provenance
}
```

Multiple Differential Tuples can support Principle extraction.

Conceptually:

```text
DT₁
DT₂
DT₃
 ↓
Structural Comparison
 ↓
Candidate Principle
```

This gives Principle Intelligence an explicit intermediate layer between raw observation and abstract Principle.

---

# 22. Differential Trees

When many related differences accumulate, a flat list becomes inefficient.

They can be organized structurally.

For example:

```text
Baseline
  │
  ├── Difference A
  │      ├── Context A1
  │      └── Context A2
  │
  ├── Difference B
  │      ├── Outcome B1
  │      └── Outcome B2
  │
  └── Difference C
         └── Exception C1
```

A Metric-Differential Tree or related differential structure can help localize:

* recurring deltas,
* branch-specific constraints,
* contextual exceptions,
* and candidate invariants.

Principle Intelligence does not require one specific differential-tree implementation.

The general idea is:

> **Organized differences can become a search substrate for Principle extraction.**

---

# 23. From Differential Tree to Principle

A possible structural pipeline is:

```text
Observations
     ↓
Differential Tuples
     ↓
Differential Tree
     ↓
Recurring / Critical Branch Pattern
     ↓
Structural Abstraction
     ↓
Candidate Principle
```

For example:

```text
ROOT: motion command
  │
  ├── free space → succeeds
  │
  ├── soft obstacle → partial motion
  │
  └── rigid obstacle → fails
```

A candidate Principle might be:

```text
Motion outcome depends on interaction constraints,
not only geometric target distance.
```

Again, the Principle is not yet guaranteed to be correct.

It is a compact structural hypothesis generated from differential evidence.

---

# 24. Principle Extraction Is Not Mere Pattern Matching

Pattern matching asks:

> Have I seen this pattern before?

Principle extraction asks a stronger question:

> What reusable structural relation explains or constrains these differences?

For example:

```text
Pattern:
A1 → B1
A2 → B2
A3 → B3
```

may simply be memorized.

Principle extraction attempts:

```text
Shared Structural Relation:
R(A,B)
```

and asks whether R can be reused beyond the original observations.

Thus:

```text
Pattern Recognition
        ↓
Similarity
```

is different from:

```text
Principle Extraction
        ↓
Reusable Structural Relation
```

Both are useful.

They solve different problems.

---

# 25. Principle Extraction Is Not Mere Natural-Language Summarization

A language model can summarize observations:

> "Reverse transitions appear more difficult."

That sentence may be useful.

But Principle Intelligence requires more than a sentence.

A candidate Principle should eventually bind:

```text
Identity
Structure
Scope
Context
Evidence
Provenance
Uncertainty
Validation State
```

Therefore:

> **Natural-language articulation may describe a Principle, but it is not the Principle itself.**

The Principle is the structured intelligence object behind the description.

---

# 26. Principle Extraction Is Not Necessarily Fully Explainable

An intelligent system may discover a useful structural relation before it can explain the underlying mechanism.

For example:

```text
Context X
   ↓
Transition A → B repeatedly fails
```

The system may not yet know whether the cause is:

* friction,
* geometry,
* policy,
* hidden state,
* or model error.

Nevertheless, it can preserve the structural relation:

```text
Under Context X,
A → B has low observed reachability.
```

This can already improve planning.

Therefore:

> **Structural usefulness can precede complete causal explanation.**

Later evidence may refine the Principle.

---

# 27. Principle Candidates Can Exist at Different Abstraction Levels

A Principle need not begin at maximum abstraction.

Consider:

```text
Level 0:
This door does not open.

Level 1:
This door does not open when locked.

Level 2:
Locked doors resist ordinary push actions.

Level 3:
State-dependent constraints alter action reachability.

Level 4:
Reachability is context-conditioned.
```

Each level has different scope and risk.

Higher abstraction increases potential reuse.

It also increases the possibility of overgeneralization.

Therefore Principle extraction must balance:

```text
Reuse
  ↕
Specificity
```

---

# 28. The Principle Abstraction Ladder

A useful conceptual ladder is:

```text
Raw Observation
      ↓
Localized Difference
      ↓
Differential Tuple
      ↓
Repeated Relation
      ↓
Contextual Constraint
      ↓
Candidate Principle
      ↓
Generalized Principle
```

Movement upward should not automatically destroy lower-level evidence.

The Principle should retain links back to its roots.

This is essential for later validation and revision.

---

# 29. Evidence-Preserving Abstraction

A common failure of abstraction is to discard the evidence that produced it.

Principle Intelligence should instead support:

```text
Principle
   │
   ├── Evidence Root 1
   ├── Evidence Root 2
   ├── Evidence Root 3
   └── Counter-Evidence Root
```

This produces **Evidence-Preserving Abstraction**.

The Principle can be compact while remaining traceable.

This matters for:

* debugging,
* scientific reasoning,
* governance,
* safety,
* revision,
* collective learning,
* and provenance.

---

# 30. Structural Compression Without Evidence Destruction

The goal is therefore not:

```text
Many Observations
      ↓
Principle
      ↓
Delete Observations
```

but:

```text
Many Observations
      ↓
Structural Compression
      ↓
Principle
      │
      └──── links to evidence roots
```

The Principle becomes a navigation structure over evidence rather than a replacement for evidence.

This is a significant difference from lossy knowledge summarization.

---

# 31. Candidate Principle Object

A minimal candidate Principle may contain:

```text
CandidatePrinciple {
    identity
    structural_statement
    scope
    context
    supporting_evidence
    source_differences
    provenance
    confidence
    validation_state
}
```

Later stages may add:

```text
counter_evidence
exceptions
derived_CCCs
compatible_triggers
revision_history
portable_interfaces
```

The important point in this document is that Principle extraction should emit more than a sentence.

It should emit an identifiable structural object.

---

# 32. Principle Extraction from Model Outputs

Differential evidence does not need to come only from direct physical observation.

It may come from:

```text
World Model
LLM
JEPA-like Predictor
Simulator
Calling Graph
Database
Sensor System
Human Report
Another Agent
PIRP / PIRU
```

For example:

```text
World Model Prediction
          ↓
Observed Outcome
          ↓
Difference
          ↓
Candidate Principle
```

Thus Principle Intelligence can operate **above learned models**.

The model does not need to be replaced.

Its outputs become potential evidence.

---

# 33. Model Error as Structural Opportunity

Prediction error is often treated only as a loss to minimize.

Principle Intelligence adds another interpretation.

A persistent localized prediction error may indicate:

```text
missing structure
hidden constraint
new context
incorrect metric
directional dynamics
model boundary
```

Therefore:

> **Model error can become a trigger for structural learning.**

Conceptually:

```text
Prediction
    ↓
Reality
    ↓
Delta
    ↓
Localized Failure
    ↓
Candidate Structural Explanation
    ↓
Candidate Principle
```

This creates a bridge between statistical learning and structural learning.

---

# 34. Residual Intelligence

After a model explains most observations, the remaining unexplained differences may be especially valuable.

Call these:

> **Structural Residuals**

Conceptually:

```text
Observation
   -
Model Expectation
   =
Residual
```

Again, this subtraction is conceptual rather than necessarily Euclidean.

Residuals may contain:

* anomalies,
* exceptions,
* new branches,
* hidden contexts,
* counterexamples,
* and emerging Principles.

This suggests:

> **What the current model cannot compress may become raw material for the next structural layer.**

---

# 35. Leftover → Growth

This creates a recurring growth loop:

```text
Current Intelligence
       ↓
Handles Known Structure
       ↓
Residual / Leftover
       ↓
Difference Extraction
       ↓
Candidate Principle
       ↓
New Structural Intelligence
       ↓
Expanded Capability
       ↓
New Residual
       ↓
...
```

This is an important connection between Differential Intelligence and Open-Ended Growth.

Growth is driven not only by success.

It is also driven by what existing intelligence leaves unexplained.

---

# 36. Principle Extraction as Fold-Back

When repeated runtime experience produces a reusable Principle, the system can fold the experience back into its intelligence structure.

```text
Runtime Experience
       ↓
Differences
       ↓
Candidate Principle
       ↓
Validation
       ↓
Fold Back
       ↓
Reusable Structural Intelligence
```

The next encounter no longer needs to begin from zero.

This is a major reason Principle extraction can reduce repeated computation.

---

# 37. The Small-Delta Hypothesis

A large environment may change only slightly between two situations.

Recomputing the entire intelligence structure may be wasteful.

Instead:

```text
Known Structure
      +
Small Delta
      ↓
Localized Structural Update
```

This motivates the **Small-Delta Hypothesis**:

> **A small structural difference can sometimes determine a disproportionately large change in intelligent behavior.**

Examples include:

* one new obstacle,
* one policy change,
* one failed dependency,
* one changed market regime,
* one counterexample,
* one new interface,
* one altered precondition.

Principle Intelligence should therefore pay special attention to small but consequential deltas.

---

# 38. Small Delta Does Not Mean Small Importance

Consider:

```text
99.9% of environment unchanged
0.1% changed
```

If the changed 0.1% is:

```text
bridge unavailable
```

the optimal route may change completely.

Therefore:

```text
Structural Magnitude
      ≠
Behavioral Impact
```

A small structural delta may produce a large policy delta.

This is one reason global similarity can be misleading.

---

# 39. Differential Intelligence and Trigger Extraction

Some differences recur in a way that suggests a trigger.

For example:

```text
Condition X appears
      ↓
Behavior changes sharply
```

Repeated observations may support:

```text
X is a candidate structural trigger.
```

This provides another extraction path:

```text
Difference
    ↓
Boundary
    ↓
Trigger Candidate
    ↓
Principle Candidate
```

The Principle may describe why or under what scope the trigger matters.

Thus Trigger Intelligence and Principle Intelligence are related but not identical.

---

# 40. Differential Intelligence and Trajectories

Individual states often hide important structure.

Trajectories expose it.

Consider:

```text
Trajectory A:
S0 → S1 → S2 → Goal

Trajectory B:
S0 → S1 → S3 → Failure
```

The important difference may be localized at:

```text
S1 → {S2, S3}
```

This branching point can reveal:

* a decision boundary,
* a hidden condition,
* a policy difference,
* a dynamic constraint,
* or a candidate Principle.

Therefore:

> **Trajectory difference is a powerful source of sparse structural evidence.**

---

# 41. Difference of Differences

A further level appears when the system compares differences themselves.

Suppose:

```text
Delta₁ = S1 → S2
Delta₂ = S2 → S3
Delta₃ = S3 → S4
```

The relation among these deltas may reveal:

* acceleration,
* curvature,
* trend,
* structural drift,
* phase transition,
* or behavioral instability.

Conceptually:

```text
Observation
   ↓
Difference
   ↓
Difference of Differences
   ↓
Higher-Order Structure
```

This is important because some Principles do not exist at the state level.

They exist at the level of changing relations.

---

# 42. Structural Curvature as Differential Evidence

Consider a trajectory represented by local transitions:

```text
v₁
v₂
v₃
```

If:

```text
direction(v₁) ≈ direction(v₂) ≈ direction(v₃)
```

the trajectory may have low local structural curvature.

If the direction changes sharply:

```text
v₂ ≠ expected continuation of v₁
```

that deviation itself becomes differential evidence.

This general idea applies beyond geometry.

A sudden change in:

* behavior,
* policy,
* causal relation,
* trajectory,
* cost,
* or evidence pattern

can signal a structural boundary.

Thus:

> **Curvature can be understood more generally as change in the structure of change.**

---

# 43. From Temporal Straightening to a General Differential Lesson

Recent latent-planning research provides a useful external example.

A learned representation can contain trajectories whose local geometry is poorly aligned with simple planning costs.

By explicitly examining relations among consecutive latent transitions, the representation can be encouraged toward a geometry that better supports downstream planning.

The broader lesson for Principle Intelligence is not that every problem should use one particular geometric regularizer.

It is:

> **Relations among local differences can reveal computationally useful structure that is invisible at the level of isolated states.**

This is a general differential principle.

---

# 44. Differential Evidence Can Change the Representation

An important consequence follows.

Difference extraction does not merely produce a new conclusion.

It may reveal that the existing representation itself is inadequate.

For example:

```text
Current Representation:
Visual similarity
```

but evidence shows:

```text
Visually close states
are behaviorally unreachable.
```

The system may need a new representation:

```text
Behavioral reachability
```

Therefore:

> **Differential Intelligence can trigger representational growth.**

This becomes important for Open Structural Learning.

---

# 45. From Learning Values to Learning Dimensions

A closed learning system changes values inside existing dimensions.

For example:

```text
Feature X = 0.7
Feature Y = 0.2
```

But a critical difference may reveal that the system lacks an entire dimension:

```text
Directionality
```

or:

```text
Policy Context
```

or:

```text
Reversibility
```

Then learning becomes:

```text
Old Representation
      ↓
Unexplained Difference
      ↓
New Structural Dimension
      ↓
Expanded Representation
```

This is deeper than parameter adjustment.

It is structural growth.

---

# 46. Principle Extraction and Open Structural Learning

We can now connect the pipeline:

```text
Observation
    ↓
Difference
    ↓
Differential Evidence
    ↓
Candidate Principle
    ↓
New Structural Object
    ↓
Expanded Structural Space
```

The Principle is not only an answer.

It may become a new object available to future reasoning.

This means:

> **Principle extraction can enlarge the vocabulary of intelligence.**

Once created, a Principle can participate in subsequent Principles.

This recursive possibility is developed more fully in the Open-LHS framework.

---

# 47. The Principle Extraction Loop

A complete high-level loop is:

```text
        WORLD / EXPERIENCE
               │
               ▼
          Observation
               │
               ▼
          Localization
               │
               ▼
           Difference
               │
               ▼
     Differential Evidence
               │
               ▼
      Structural Compression
               │
               ▼
      Candidate Principle
               │
               ▼
           Validation
               │
        ┌──────┴──────┐
        ▼             ▼
     Reject         Promote
                      │
                      ▼
             Reusable Structure
                      │
                      ▼
                 Application
                      │
                      ▼
                 New Evidence
                      │
                      └──────────→
```

This is not a one-time extraction process.

It is a continuing learning cycle.

---

# 48. Statistical Learning and Principle Learning

The two paradigms can be summarized as follows.

## Statistical Learning

```text
Many Samples
    ↓
Regularity
    ↓
Parameter Update
    ↓
Model
```

Primary strength:

> Robust learning from distributed statistical evidence.

## Principle Learning

```text
Critical Evidence
      ↓
Difference
      ↓
Structural Relation
      ↓
Candidate Principle
```

Primary strength:

> High leverage from structurally informative evidence.

A mature intelligence architecture may combine them:

```text
Statistical Substrate
        +
Differential Extraction
        +
Principle Formation
        +
Structural Validation
```

This hybrid is more important than arguing for either paradigm in isolation.

---

# 49. Neural Models as Principle Mines

A large model can be viewed not only as an inference engine.

It can also be viewed as a rich source of latent candidate structure.

Conceptually:

```text
Large Model
    ↓
Rich Learned Representation
    ↓
Observed Regularities / Failures / Contrasts
    ↓
Differential Extraction
    ↓
Candidate Principles
```

This suggests a different relationship between models and explicit intelligence.

Instead of:

```text
Model OR Structure
```

consider:

```text
Model
  ↓
Structure Mining
  ↓
Principle
```

The model becomes an upstream intelligence substrate.

---

# 50. The Principle Mine Is Not the Principle Store

This distinction is important.

A model may suggest a Principle.

That does not mean the Principle should immediately be trusted.

Therefore:

```text
Model Output
    ↓
Candidate Principle
```

must remain separate from:

```text
Validated Principle
```

The Principle needs:

* evidence,
* provenance,
* scope,
* validation,
* counter-evidence,
* and revision mechanisms.

This protects Principle Intelligence from turning model generations into unexamined rules.

---

# 51. Human Knowledge as Differential Evidence

Humans remain important participants.

A human can provide:

* observations,
* principles,
* exceptions,
* domain constraints,
* counterexamples,
* causal hypotheses,
* and critiques.

Principle Intelligence can treat these as structured inputs.

For example:

```text
Machine Observation
       +
Human Counterexample
       ↓
Differential Evidence
       ↓
Principle Revision
```

Thus the architecture supports human-machine collective learning rather than assuming purely autonomous knowledge formation.

---

# 52. AI-to-AI Differential Learning

The same logic extends across agents.

Suppose Agent A reports:

```text
Under Context X,
Transition A → B fails.
```

Agent B reports:

```text
Under Context Y,
Transition A → B succeeds.
```

The difference between the agents' experiences becomes new evidence:

```text
Context X
   vs
Context Y
```

which may produce:

```text
Candidate Principle:
Reachability of A → B is context-dependent.
```

Thus:

> **Difference between agents can itself become intelligence.**

This is a foundation for Collective Learning.

---

# 53. Principle Extraction Across Agents

A collective pipeline can be:

```text
Agent A Evidence
       │
Agent B Evidence
       │
Agent C Evidence
       │
       ▼
Cross-Agent Difference
       │
       ▼
Structural Localization
       │
       ▼
Candidate Principle
       │
       ▼
Collective Validation
```

The Principle need not originate from any single agent.

It can emerge from differences among their experiences.

This is a powerful form of distributed structural learning.

---

# 54. Differential Intelligence and Portability

Once a Principle is extracted, it can potentially be externalized.

The progression becomes:

```text
Experience
    ↓
Difference
    ↓
Principle
    ↓
Validation
    ↓
Portable Intelligence Structure
```

The ability to extract Principles therefore provides an upstream source for PIRP/PIRU-like portable intelligence.

Without extraction, portability is limited to structures already known.

With Principle extraction:

> **New reusable intelligence can be continuously generated from experience.**

---

# 55. From Sample Efficiency to Intelligence Efficiency

Machine learning often measures sample efficiency:

> How much performance can be obtained from how many examples?

Principle Intelligence introduces a related but different question:

> **How much reusable intelligence can be extracted from each structurally important observation?**

Call this informally:

**Intelligence Efficiency.**

A system may be sample-efficient at fitting a task but poor at producing reusable knowledge.

Another system may extract a Principle that benefits many future tasks.

Therefore evaluation may eventually need to distinguish:

```text
Task Performance
Sample Efficiency
Structural Reuse
Transfer Value
Principle Longevity
Counter-Evidence Robustness
```

---

# 56. Principle Value Is Downstream

A Principle is useful not merely because it compresses past observations.

Its real value appears downstream.

A good Principle may:

* reduce future search,
* prevent invalid actions,
* improve planning,
* expose missing context,
* generate CCCs,
* activate triggers,
* constrain policies,
* guide model queries,
* improve transfer,
* or become part of another Principle.

Thus:

> **Principle quality should eventually be evaluated by structural reuse, not only retrospective fit.**

---

# 57. The Risk of Premature Principle Formation

Sparse evidence creates leverage.

It also creates danger.

A system can overgeneralize from too little evidence.

For example:

```text
One failure
    ↓
"Action always fails."
```

This is not Principle Intelligence.

It is premature closure.

Therefore candidate Principles should preserve:

```text
scope
context
evidence count
evidence diversity
uncertainty
provenance
```

and remain open to challenge.

Sparse evidence should increase structural attention, not unjustified certainty.

---

# 58. The Risk of Perspective Collapse

Another danger is assuming that one observed difference is the only meaningful difference.

For example:

```text
Geometric Distance
```

may dominate planning while ignoring:

```text
Energy Cost
Safety
Policy
Time
Reversibility
```

A Principle extracted under one perspective may fail under another.

Therefore:

> **Principles should preserve the perspective under which their evidence was interpreted.**

This is especially important when Principles are transferred across agents or applications.

---

# 59. The Risk of Hidden Context

A candidate Principle may appear universal because the training context was narrow.

For example:

```text
A → B always succeeds
```

may actually mean:

```text
A → B succeeds
under Context C.
```

When Context C disappears, the Principle fails.

Therefore Principle extraction should prefer:

```text
Context-Bound Principle
```

over premature:

```text
Universal Principle
```

unless broader evidence justifies generalization.

---

# 60. The Risk of Structural Hallucination

Just as generative models can hallucinate facts, a structural learner can hallucinate Principles.

A plausible relation may be:

* unsupported,
* coincidental,
* overgeneralized,
* context-confused,
* or generated from model error.

Therefore Principle extraction must be separated from Principle promotion.

The system should support:

```text
Candidate
    ≠
Validated
```

This distinction is foundational.

---

# 61. Principle Extraction as an Evidence Contract

A useful design principle is:

> **Every candidate Principle should carry an evidence contract.**

At minimum:

```text
What observations produced it?

What differences were extracted?

What context was active?

What abstraction was performed?

What scope is claimed?

What uncertainty remains?
```

This makes Principle formation auditable.

It also prepares the Principle for later Two-Way validation and counter-evidence search.

---

# 62. Minimal Evidence-Preserving Pipeline

A practical conceptual pipeline is:

```text
RAW EXPERIENCE
      │
      ▼
OBSERVATION
      │
      ▼
LOCALIZATION
      │
      ▼
DIFFERENCE
      │
      ▼
DIFFERENTIAL TUPLE
      │
      ▼
STRUCTURAL COMPARISON
      │
      ▼
CANDIDATE RELATION
      │
      ▼
CANDIDATE PRINCIPLE
      │
      ├── Context
      ├── Scope
      ├── Evidence
      ├── Provenance
      └── Uncertainty
```

No evidence is required to disappear merely because abstraction occurred.

---

# 63. A General Principle Extraction Template

The following template can guide future implementations:

```text
1. OBSERVE
   Collect relevant experience.

2. LOCALIZE
   Identify where the important change,
   failure, asymmetry, or novelty occurred.

3. DIFFERENTIATE
   Compare against baseline, expectation,
   reverse transition, alternate context,
   or competing trajectory.

4. STRUCTURE
   Represent the difference in a form
   suitable for comparison.

5. COMPARE
   Search for repeated relations,
   invariants, constraints, boundaries,
   asymmetries, or higher-order changes.

6. ABSTRACT
   Compress the selected relation into
   a candidate Principle.

7. BIND
   Preserve context, scope, provenance,
   evidence, and uncertainty.

8. EMIT
   Produce a Candidate Principle.

9. VALIDATE
   Hand the candidate to downstream
   evidence and counter-evidence mechanisms.

10. FOLD BACK
    If promoted, make the Principle
    reusable by future intelligence.
```

This is not intended as a fixed universal algorithm.

It is a structural reference path.

---

# 64. The Differential Intelligence Thesis

The core thesis of this document can now be stated more precisely:

> **Intelligence does not depend only on the number of observations available. It also depends on the ability to identify which differences carry structural significance, preserve their context and provenance, compress them into reusable candidate relations, and expose those relations to validation.**

This leads to:

```text
Sparse Evidence
      +
High-Value Difference
      +
Structural Extraction
      ↓
Candidate Principle
```

The value comes from leverage, not magic.

---

# 65. The Principle Extraction Thesis

A second thesis follows:

> **Principles need not be authored exclusively from outside the intelligent system. They can be generated from localized differential evidence produced by interaction among the world, learned models, humans, and other agents.**

Thus:

```text
World
Model
Human
Agent
PIRU
  │
  ▼
Evidence
  │
  ▼
Difference
  │
  ▼
Principle
```

Principle formation becomes a general intelligence operation.

---

# 66. The Open-Growth Thesis

A third thesis follows:

> **Once extracted, a Principle can become a new structural object available to future learning.**

Therefore:

```text
Experience₁
   ↓
Principle₁
   ↓
New Structural Vocabulary
   ↓
Experience₂
   ↓
Principle₂
   ↓
Expanded Structural Vocabulary
   ↓
...
```

The intelligence system is no longer learning only values inside a fixed representational space.

It can participate in the growth of that space.

---

# 67. From Data Learning to Structural Learning

The transition can be summarized as:

```text
DATA LEARNING
Many observations
      ↓
Statistical regularity
      ↓
Model
```

```text
DIFFERENTIAL LEARNING
Critical observations
      ↓
Important differences
      ↓
Structural relation
```

```text
PRINCIPLE LEARNING
Structural relation
      ↓
Abstraction
      ↓
Candidate Principle
      ↓
Validation
      ↓
Reusable Intelligence
```

Together:

```text
Statistical Learning
        +
Differential Intelligence
        +
Principle Intelligence
        ↓
Hybrid Structural Learning
```

---

# 68. Conclusion

Large-scale statistical learning has transformed artificial intelligence.

But intelligence also encounters worlds in which the most important evidence is rare.

A single failure can expose a hidden boundary.

A single reverse transition can reveal asymmetry.

A small trajectory divergence can expose a critical decision point.

One counterexample can challenge a broad generalization.

A new context can reveal that an apparently universal relation was only local.

These cases motivate Differential Intelligence.

The central move is simple:

> Do not ask only what is common.

Also ask:

> **What changed?**

> **What failed?**

> **What became asymmetric?**

> **What remained invariant?**

> **What difference carries structural meaning?**

From these questions emerges a path:

```text
Observation
    ↓
Localization
    ↓
Difference
    ↓
Differential Evidence
    ↓
Structural Compression
    ↓
Candidate Principle
```

The resulting Principle is not automatically true.

It is an evidence-bound structural hypothesis.

Its value lies in the possibility that a small amount of critical evidence can be transformed into intelligence that is:

* reusable,
* testable,
* revisable,
* composable,
* transferable,
* and capable of participating in further structural growth.

This leads directly to the next problem.

If a Principle can emerge from experience, what kinds of structures may participate in its formation?

Must the Principle operate only over a vocabulary defined before deployment?

Or can newly generated CCCs, Principles, trajectories, triggers, PIRPs, PIRUs, model outputs, and delegated structures enter its evidence space at runtime?

That question leads from differential learning to **Open-LHS Principle Intelligence**.

---

## Next Document

**PI-003 — Open-LHS Principles and Runtime Structural Generation**

The next document develops the central open-structure hypothesis of this repository:

> **The left-hand side of a Principle need not be restricted to a predefined symbolic vocabulary. Existing, retrieved, composed, delegated, and runtime-generated intelligence structures may participate directly in Principle formation and evaluation.**

This transforms Principle Intelligence from a fixed-vocabulary reasoning system into an open structural learning system whose representational objects can grow together with its intelligence.

---

## Repository Thesis

> **Large samples reveal regularity.
> Critical differences reveal structure.
> Structure can become Principle.
> Principle can become reusable intelligence.
> Reusable intelligence can become the substrate of further growth.**

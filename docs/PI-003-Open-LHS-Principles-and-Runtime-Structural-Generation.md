# PI-003 — Open-LHS Principles and Runtime Structural Generation

## Reasoning in a Structural Space That Can Grow While Reasoning

**Repository:** Principle Intelligence and Open Structural Learning
**Document:** PI-003
**Status:** v1.0.0
**Authors:** Sizhe Tan & GPT-Obot

---

## Abstract

Most computational reasoning systems operate over a structural vocabulary substantially defined before reasoning begins.

Predicates are declared.

Variables have known types.

Rules reference known relations.

Ontologies establish admissible concepts.

Functions accept predefined classes of inputs.

Even when values change dynamically, the kinds of objects that may participate in reasoning are usually constrained by a relatively stable representational system.

Principle Intelligence proposes a more open alternative.

A Principle should not require its left-hand side, or **LHS**, to consist only of predefined symbolic facts or predicates.

Its evidence space may contain any identifiable and structurally compatible intelligence object, including:

* observations,
* differences,
* differential tuples,
* metrics,
* trajectories,
* CCCs,
* Two-Way CCC results,
* counter-evidence,
* triggers,
* policies,
* Calling Graphs,
* Principles,
* world-model outputs,
* PIRPs,
* PIRUs,
* delegated computational results,
* and structures generated during the evaluation of the Principle itself.

This document calls this architecture the **Open-LHS Principle**.

The deeper implication is that reasoning no longer needs to operate only inside a structural space completely specified before execution.

If a required structure is missing, the system may:

```text id="1f5l7a"
Search
Retrieve
Generate
Compose
Unfold
Delegate
Validate
Bind
```

the missing structure at runtime and allow it to participate immediately in the Principle's evidence space.

This leads to a second concept:

> **Runtime Structural Generation**

and to a broader thesis:

> **Reasoning can create the representational structures required for its own reasoning.**

Principle Intelligence therefore moves beyond the idea of computing only over a fixed ontology.

The vocabulary of intelligence itself may grow through experience, structural extraction, composition, delegation, and Collective Learning.

This transforms Principle evaluation from closed-space predicate matching into **open structural computation**.

---

# 1. The Closed-LHS Assumption

A traditional rule can be represented as:

```text id="oxv4dq"
A ∧ B ∧ C → D
```

The system evaluates whether:

```text id="zytqbt"
A = true
B = true
C = true
```

and then produces D.

This model is extraordinarily useful.

But it normally assumes that A, B, C, and D already belong to a known representational system.

The rule engine may not know their values in advance.

But it generally knows what kinds of things they are.

This distinction is important.

A system can be dynamically evaluated while still being structurally closed.

---

# 2. Dynamic Values Are Not the Same as Dynamic Structure

Consider:

```text id="gj8h6u"
temperature = ?
pressure = ?
door_state = ?
```

The values may be unknown until runtime.

But the dimensions themselves are predefined:

```text id="j95vkt"
temperature
pressure
door_state
```

This is **dynamic value assignment**.

Open Structural Learning asks a different question:

> What if the system encounters an important structure for which no existing representational object yet exists?

For example:

```text id="czngwu"
new behavioral asymmetry

new trajectory pattern

new counter-evidence relation

new Principle

new PIRU

new policy interaction

new structural trigger
```

The problem is no longer:

> What is the value of X?

It becomes:

> **X did not previously exist. Can intelligence create X and use it immediately?**

---

# 3. From Closed Vocabulary to Open Structural Vocabulary

A closed-vocabulary reasoning system can be simplified as:

```text id="13vmj4"
Predefined Vocabulary
        ↓
Facts
        ↓
Rules
        ↓
Inference
```

An open structural system aims toward:

```text id="mkq5h4"
Existing Vocabulary
        ↓
Experience
        ↓
Novel Difference
        ↓
New Structural Object
        ↓
Expanded Vocabulary
        ↓
Further Reasoning
```

The important transition is:

> **The vocabulary is no longer merely the input to intelligence. It can also become an output of intelligence.**

---

# 4. Open-LHS Principle

We define the central design principle of this document as follows:

> ## Open-LHS Principle
>
> **The left-hand side of a Principle is not restricted to a predefined symbolic vocabulary. Any identifiable and structurally compatible intelligence object—including dynamically generated structures—may participate in Principle formation and evaluation.**

Conceptually:

```text id="1w8nd6"
Principle LHS
│
├── Observation
├── Fact
├── Difference
├── Differential Tuple
├── Metric Relation
├── Trajectory
├── CCC
├── Two-Way CCC Result
├── Counter-Evidence
├── Trigger
├── Policy
├── Calling Graph
├── Principle
├── World-Model Output
├── PIRP
├── PIRU
├── Delegated Result
└── Runtime-Generated Structure
```

This list is intentionally open.

The architecture should not assume that every future structural type is known today.

---

# 5. LHS as Structural Evidence Space

In a conventional rule:

```text id="r1zx8v"
LHS → RHS
```

the LHS is often understood primarily as a condition.

For Principle Intelligence, this is too narrow.

The LHS is better understood as:

> **a structural evidence space from which a Principle may be formed, instantiated, evaluated, challenged, or revised.**

Thus:

```text id="82i1yw"
LHS
 ≠
fixed list of predicates
```

Instead:

```text id="tubf8x"
LHS
 =
Open Structural Evidence Space
```

This space can contain heterogeneous intelligence structures.

---

# 6. Heterogeneous Structural Intelligence

Suppose a system is evaluating a candidate Principle concerning safe reachability.

Its evidence space might contain:

```text id="bf2e2r"
Trajectory T1

CCC C1

Policy P1

Metric M1

Counter-Evidence E1

PIRU R1

World-Model Prediction W1
```

These objects are not identical.

They may have different internal representations.

Yet they can participate in the same Principle if their interfaces and semantics allow meaningful structural binding.

Therefore:

> **Principle Intelligence does not require all intelligence to collapse into one homogeneous representation.**

It requires enough structural identity and interface information to compose heterogeneous evidence.

---

![Fig-004 — Open-LHS and Runtime Structural Generation](../figures/Fig-004-Open-LHS-and-Runtime-Structural-Generation.png)

**Fig-004 — Open-LHS and Runtime Structural Generation.**  
An Open-LHS may bind heterogeneous existing or runtime-generated intelligence structures. When required structure is missing, the runtime may retrieve, compose, generate, unfold, or delegate its creation before continuing Principle evaluation.

---

# 7. The Missing-Structure Problem

An Open-LHS system immediately encounters a new problem.

Suppose a Principle requires evidence of type:

```text id="pr2spk"
DirectionalReachability
```

but no such structure currently exists.

A closed system may return:

```text id="e38rqf"
UNKNOWN
```

or:

```text id="wxz43p"
TYPE NOT FOUND
```

An Open-LHS system has additional options.

It can ask:

```text id="zc1cll"
Can the missing structure be:

searched?

retrieved?

derived?

generated?

composed?

unfolded?

delegated?

measured?

validated?
```

This changes the nature of reasoning.

---

# 8. Runtime Structural Generation

We therefore define:

> ## Runtime Structural Generation
>
> **During Principle formation or evaluation, the system may create, retrieve, compose, unfold, or delegate the production of new structural objects required to continue reasoning.**

Conceptually:

```text id="as9z9a"
Principle Evaluation
        ↓
Required Structure Missing?
       / \
     YES  NO
      │    │
      ▼    │
Search / Retrieve
Generate / Compose
Unfold / Delegate
      │
      ▼
New Structure
      │
      ▼
Identity / Type / Context
      │
      ▼
Bind into LHS
      │
      └────────────→ Continue Evaluation
```

The Principle evaluation process can therefore alter the structural space in which it operates.

---

# 9. Reasoning Can Produce Its Own Representational Objects

This leads to the central thesis of this document:

> **Reasoning can create the representational structures required for its own reasoning.**

This is stronger than ordinary inference.

Ordinary inference may derive:

```text id="7e4lbd"
A + B → C
```

where C belongs to the existing language.

Open structural reasoning may instead encounter:

```text id="j5jrd8"
A + B
   ↓
Existing vocabulary insufficient
   ↓
Generate new structure X
   ↓
Bind X
   ↓
A + B + X
   ↓
Candidate Principle P
```

The reasoning process has changed its own usable structural vocabulary.

---

# 10. A Simple Example

Suppose an agent knows:

```text id="7zy63e"
A → B succeeds
```

and:

```text id="73y16d"
B → A fails
```

The existing system has no explicit concept of directional reachability.

Differential Intelligence detects:

```text id="53slfm"
A → B ≠ B → A
```

The system generates:

```text id="1rrvka"
DirectionalReachabilityRelation
```

This newly generated structure can then enter the LHS:

```text id="q3r0c7"
DirectionalReachabilityRelation
        +
Context C
        +
Trajectory Evidence T
        ↓
Candidate Principle:
Reachability may be directional under C.
```

The new representational object did not need to exist before the observations occurred.

---

# 11. Structure Creation Is Not Arbitrary Symbol Creation

Open-LHS does not mean that the system can invent arbitrary symbols and treat them as knowledge.

A new structure should have sufficient grounding.

At minimum, a runtime-generated structure should seek to preserve:

```text id="t0nyx2"
Identity
Type
Context
Evidence
Provenance
Interface
Semantics
Validation State
```

A newly named object without evidence or usable semantics is not necessarily intelligence.

Therefore:

> **Open structure requires disciplined binding.**

Freedom of structural generation must be paired with structural accountability.

---

# 12. Identity Before Reuse

A runtime-generated object becomes reusable only when it can be identified.

Conceptually:

```text id="uzhztw"
New Structure
      ↓
Identity
      ↓
Type
      ↓
Context
      ↓
Interface
      ↓
Reusable Object
```

Without identity, the structure may remain a transient local computation.

With identity, it can potentially:

* enter another Principle,
* be cached,
* be compared,
* be transported,
* be versioned,
* be validated,
* or be shared with another agent.

This creates a natural connection to Universal Typing and Naming.

---

# 13. UTN as an Open-LHS Binding Layer

An Open-LHS architecture cannot depend on every agent knowing every structural object in advance.

A typing and naming layer can help.

Conceptually:

```text id="3vlwj6"
Unknown Structure X
       ↓
UTN Identity
       ↓
Type / Context
       ↓
Interface Discovery
       ↓
Compatibility Check
       ↓
Principle LHS Binding
```

The Principle Engine does not necessarily need complete prior knowledge of X.

It needs enough information to determine:

> What is X?

> What does X claim?

> What evidence supports X?

> What interface does X expose?

> Under what context is X meaningful?

> Can X legally participate in this Principle?

Thus:

> **Open-LHS reasoning can operate over typed structural interfaces rather than a permanently closed vocabulary.**

---

# 14. From Ontology-First to Structure-First Learning

Traditional knowledge engineering often follows:

```text id="n2yr6f"
Define Ontology
      ↓
Define Relations
      ↓
Insert Knowledge
      ↓
Reason
```

Open Structural Learning can also support:

```text id="h9eg5m"
Observe
   ↓
Detect Difference
   ↓
Generate Structure
   ↓
Assign Identity / Type
   ↓
Integrate
   ↓
Reason
```

This does not eliminate ontology.

Instead, ontology can become partly emergent and extensible.

The system may maintain a stable core vocabulary while allowing new structural types to grow around it.

---

# 15. Core + Delta Vocabulary

A practical architecture need not choose between completely fixed and completely unconstrained representation.

A useful model is:

```text id="vxhfda"
CORE VOCABULARY
      +
STRUCTURAL DELTA
      ↓
CURRENT VOCABULARY
```

The Core provides:

* identity semantics,
* basic evidence contracts,
* compatibility rules,
* governance,
* lifecycle mechanisms.

The Delta contains:

* newly discovered relations,
* new Principles,
* new PIRUs,
* new context types,
* new triggers,
* new structural interfaces.

Thus:

> **Open does not mean structureless.**

It means the structure can grow without requiring complete redesign of the core.

---

# 16. CCC as an Open-LHS Object

A CCC can participate directly in a Principle LHS.

For example:

```text id="dyvz5m"
CCC-A:
Context X
  ↓
Condition Y
  ↓
Consequence Z
```

A Principle may use this CCC as evidence:

```text id="k6ej97"
CCC-A
   +
Trajectory T
   +
Evidence E
   ↓
Candidate Principle P
```

The Principle Engine does not need to flatten CCC-A into primitive facts if its structural interface is sufficient.

This preserves richer structure.

---

# 17. Runtime-Generated CCCs

More importantly, the CCC may not exist before Principle evaluation begins.

Suppose the Principle Engine identifies a missing contextual relation.

It can request:

```text id="23lrle"
Generate CCC for:
Context X
Condition Y
Observed Outcome Z
```

The resulting CCC can immediately enter the LHS:

```text id="h2fn6h"
Runtime CCC
     ↓
LHS Binding
     ↓
Principle Evaluation
```

This is a major difference from reasoning over a static rule database.

---

# 18. Principles Can Enter Principles

A Principle may itself participate in another Principle.

For example:

```text id="0cm3rl"
Principle P1:
Reachability may be directional.

Principle P2:
Energy cost increases under load.
```

A higher-level Principle might be formed from:

```text id="n9ofde"
P1
+
P2
+
Trajectory Evidence
↓
P3:
Directional reachability may be
energy-conditioned.
```

Thus:

```text id="x9ohhm"
Principle
   ↓
becomes evidence structure
   ↓
for another Principle
```

This enables hierarchical structural growth.

---

# 19. Recursive Principle Formation

The resulting architecture can become recursive:

```text id="trmm5v"
Evidence
   ↓
Principle P1
   ↓
Evidence + P1
   ↓
Principle P2
   ↓
Evidence + P1 + P2
   ↓
Principle P3
```

This is not merely recursive text generation.

Each Principle can preserve:

* evidence,
* scope,
* context,
* provenance,
* and validation state.

The structural ancestry remains available.

---

# 20. Principle Dependency Graphs

As Principles depend on other Principles, a graph naturally emerges.

```text id="r4mbfa"
Evidence E1 ──→ P1 ──┐
                     │
Evidence E2 ──→ P2 ──┼──→ P4
                     │
PIRU R1 ─────────────┘
```

This allows the system to ask:

> If P1 is weakened, which Principles depend on it?

> If E2 is invalidated, what downstream structure must be reconsidered?

Thus Open-LHS supports not only growth but also structural maintenance.

---

# 21. Counter-Evidence Can Enter the LHS

Counter-evidence should not be treated merely as an external rejection signal.

It can participate directly in Principle evaluation.

For example:

```text id="8twn9f"
Supporting Evidence E+
        +
Counter-Evidence E-
        +
Context C
        ↓
Principle Evaluation
```

This allows Principles to represent contested or conditional structures rather than forcing premature binary truth.

---

# 22. Evidence and Counter-Evidence as First-Class Objects

A mature system should be able to distinguish:

```text id="uvex8z"
EvidenceFor(P)
EvidenceAgainst(P)
EvidenceAboutScope(P)
EvidenceAboutException(P)
```

These may themselves be typed structural objects.

Then:

```text id="y9p2qe"
Principle P
     │
     ├── Evidence+
     ├── Evidence-
     ├── Scope Evidence
     └── Exception Evidence
```

The Principle becomes an evidence-bearing structure rather than an isolated proposition.

---

# 23. Trajectories Can Enter the LHS

A trajectory can also be treated as a first-class structural object.

For example:

```text id="v53qga"
Trajectory T1
Trajectory T2
```

may differ at one branching point.

The Principle LHS can contain:

```text id="4gycn1"
TrajectoryDifference(T1,T2)
      +
Policy P
      +
Context C
      ↓
Candidate Principle
```

This avoids reducing a trajectory to a single endpoint.

The structure of behavior itself becomes evidence.

---

# 24. Calling Graphs Can Enter the LHS

Software and agent behavior can be represented through Calling Graph structures.

Suppose:

```text id="2jq69v"
CallingGraph G1 succeeds.

CallingGraph G2 fails.
```

The Graph Minus operation identifies:

```text id="gk6gmk"
Delta G
```

That structural delta can participate directly in a Principle:

```text id="mbp7np"
Graph Delta
   +
Runtime Context
   +
Failure Evidence
   ↓
Candidate Principle
```

Thus Principle Intelligence is not limited to physical-world reasoning.

It can operate over computational structures.

---

# 25. Policies Can Enter the LHS

Policy is another important structural object.

Consider:

```text id="a6obgd"
Action A is physically possible.

Policy P prohibits A.
```

A purely physical reachability model may say:

```text id="qmt3bq"
reachable = true
```

But the Principle LHS may include:

```text id="f5nnjc"
Physical Reachability
       +
Policy P
       ↓
Permitted Reachability
```

This demonstrates why a single universal geometry is insufficient for many intelligence problems.

The relevant structural distance can be policy-conditioned.

---

# 26. Metrics Can Enter the LHS

Different tasks may require different metrics.

A Principle may combine:

```text id="ivpwsn"
Geometric Distance
Energy Cost
Risk Metric
Policy Cost
Reversibility
```

Instead of assuming one canonical distance:

```text id="2y2drx"
d(A,B)
```

the Principle may evaluate a structured set:

```text id="s24w09"
{
  d_geometry,
  d_behavior,
  d_energy,
  d_risk,
  d_policy
}
```

The choice of metric itself can become part of Principle reasoning.

---

# 27. World-Model Outputs Can Enter the LHS

A world model can supply:

```text id="unq4if"
Predicted State
Predicted Trajectory
Latent Relation
Estimated Dynamics
```

These outputs can participate as evidence.

For example:

```text id="a4ll7c"
World-Model Prediction
        +
Observed Outcome
        ↓
Prediction Delta
        ↓
Candidate Principle
```

The Principle system therefore sits naturally above learned models.

It does not require replacing them.

---

# 28. Model Predictions Are Evidence, Not Authority

This distinction is important.

A model output entering the LHS should not automatically dominate other evidence.

Conceptually:

```text id="a6a7em"
Model Prediction
      =
Evidence Object
```

not:

```text id="54kpsd"
Model Prediction
      =
Truth
```

The same applies to human statements, external PIRUs, and previously promoted Principles.

Every structure has provenance and scope.

---

# 29. PIRP as an Open-LHS Object

Portable Intelligence Runtime Pieces can participate directly in Principle evaluation.

A PIRP may carry:

```text id="4k5crs"
Metric
Constraint
Trigger
Evaluator
Policy
Evidence Adapter
Search Strategy
```

A Principle can bind one or more PIRPs:

```text id="z76ujc"
PIRP-A
  +
PIRP-B
  +
Local Evidence
  ↓
Principle Evaluation
```

This allows portable intelligence to become part of structural reasoning rather than merely an external tool call.

---

# 30. PIRU as an Active LHS Object

PIRUs create an even more important possibility.

A PIRU may contain not only static structure but:

```text id="b22n1i"
Identity
Interface
Behavior
Evidence
Policy
Lifecycle
Runtime Capability
```

Therefore a PIRU entering the LHS may actively compute.

For example:

```text id="8z3g45"
PIRU-A
   ↓
Generate Trajectory T

PIRU-B
   ↓
Evaluate Risk R

PIRU-C
   ↓
Search Counter-Evidence E
```

The Principle LHS becomes a computational ecosystem.

---

# 31. LHS Objects Can Be Active

This is a major conceptual shift.

Traditional LHS objects are often passive facts:

```text id="6m0ifb"
A = true
B = false
```

Open-LHS objects may be active:

```text id="abmnyr"
PIRU-A generates evidence

PIRU-B evaluates structure

PIRU-C delegates search
```

Therefore:

> **The LHS can contain intelligence, not merely data about intelligence.**

This is one of the strongest implications of Open-LHS Principle Intelligence.

---

# 32. A Principle LHS Can Compute Itself

Consider:

```text id="2euk7c"
Principle P requires:
    trajectory evidence
    policy evidence
    counter-evidence
```

Only trajectory evidence currently exists.

The LHS can initiate:

```text id="vyzgdt"
Missing Policy Evidence
        ↓
Search PIRP Registry
        ↓
Bind Policy PIRU
        ↓
Generate Policy Evaluation
```

and:

```text id="m7sczb"
Missing Counter-Evidence
        ↓
Delegate Search
        ↓
Receive Evidence Object
```

Then:

```text id="e74qle"
Trajectory
+
Policy Evaluation
+
Counter-Evidence
↓
Principle P Evaluation
```

Thus:

> **The LHS is not merely populated. It can participate in constructing itself.**

---

# 33. LHS Unfolding

This suggests the concept of **LHS Unfolding**.

Start with an incomplete structural requirement:

```text id="iqxfz4"
LHS₀
```

Then:

```text id="lztqzy"
LHS₀
  ↓
Identify Missing Structure
  ↓
Generate / Retrieve / Delegate
  ↓
LHS₁
  ↓
Identify Remaining Gap
  ↓
Generate / Retrieve / Delegate
  ↓
LHS₂
```

until:

```text id="3gk3t0"
Sufficient Evidence Structure
        ↓
Principle Evaluation
```

This connects Principle Intelligence directly to Unfolding.

---

# 34. Open-LHS Does Not Require Complete LHS

An important design choice is that Principle evaluation need not wait for perfect structural completion.

The system may classify the LHS as:

```text id="ilshhw"
Sufficient
Insufficient
Conflicted
Uncertain
Open
```

For example:

```text id="a5ghor"
Evidence+ = strong
Evidence- = unknown
Context = partial
```

may yield:

```text id="l55l17"
Candidate Principle:
provisional
```

This preserves uncertainty and avoids forcing premature closure.

---

# 35. Structural Sufficiency

The system therefore needs a concept of:

> **Structural Sufficiency**

not necessarily complete knowledge.

The question becomes:

> Is the current structural evidence sufficient for this stage of Principle use?

Different applications may require different thresholds.

Exploratory reasoning may tolerate provisional Principles.

Safety-critical action may require stronger validation.

Thus Principle evaluation can be policy-bound.

---

# 36. Delegated Structural Generation

A system may not know how to generate a required structure locally.

Instead:

```text id="lnhs6s"
Missing Structure X
       ↓
Delegation
       ↓
Agent / PIRU / Model / Service
       ↓
Generated Structure X'
       ↓
Evidence + Provenance
       ↓
Return
       ↓
LHS Binding
```

This is **Delegated Structural Generation**.

It makes Principle Intelligence naturally compatible with multi-agent systems.

---

# 37. AI-to-AI Structural Exchange

If Agent A can generate a structure needed by Agent B:

```text id="yug1ca"
Agent B
  ↓
Needs X
  ↓
Requests X
  ↓
Agent A
  ↓
Generates X
  ↓
Returns PIRU-X
  ↓
Agent B
  ↓
UTN Binding
  ↓
Open-LHS Use
```

This is more than message passing.

It is:

> **AI-to-AI exchange of reusable intelligence structure.**

That is a foundation for Collective Learning.

---

# 38. Newly Generated PIRUs Can Enter Immediately

Suppose PIRU-X did not exist anywhere before the request.

Agent A constructs it.

The sequence becomes:

```text id="75sw41"
Need
  ↓
Delegated Generation
  ↓
New PIRU-X
  ↓
Identity
  ↓
Interface
  ↓
Evidence
  ↓
Agent B LHS Binding
  ↓
Immediate Use
```

No global model retraining is required merely because a new intelligence object appeared.

This is a major potential advantage of structural externalization.

---

# 39. Collective Learning Without Global Retraining

A closed monolithic model often incorporates new intelligence through:

```text id="uxt50q"
New Data
   ↓
Training / Fine-Tuning
   ↓
New Model Version
```

Open Structural Learning may also support:

```text id="y3a07f"
New Experience
    ↓
New Principle / PIRU
    ↓
Validation
    ↓
Publish
    ↓
Bind
    ↓
Immediate Reuse
```

The two approaches can coexist.

But the second allows some forms of learning to propagate without modifying all model weights.

---

# 40. Open-LHS as a Collective Learning Interface

This leads to a major architectural proposition:

> **Open-LHS can function as a universal intake surface for Collective Structural Learning.**

New intelligence does not need to be known when the receiving agent was trained.

It needs to be:

```text id="8vvy92"
Identifiable
Typed
Contextualized
Interface-Compatible
Evidence-Bound
Policy-Compatible
```

Then it can potentially participate.

---

# 41. Structural Compatibility

Not every object should be allowed into every Principle.

Open-LHS therefore requires compatibility checks.

For example:

```text id="l3v41k"
Structure X
    ↓
Type Compatible?
Context Compatible?
Evidence Compatible?
Policy Compatible?
Version Compatible?
Interface Compatible?
```

Only then:

```text id="o0tnl3"
Bind into LHS
```

Open-LHS means extensible, not indiscriminate.

---

# 42. Evidence API

A new structural object should ideally expose an Evidence API.

Conceptually:

```text id="0t9ck8"
getIdentity()

getType()

getContext()

getEvidence()

getCounterEvidence()

getProvenance()

getConfidence()

getInterface()

getPolicy()

getVersion()
```

The exact implementation can vary.

The architectural principle is more important:

> **A receiving intelligence system should be able to interrogate the epistemic and operational status of an unfamiliar structural object.**

---

# 43. Behavior API

Active objects such as PIRUs may additionally expose behavior.

For example:

```text id="wr51cl"
evaluate()

search()

generate()

compare()

simulate()

validate()

delegate()
```

Thus a Principle LHS may bind both:

```text id="41vswe"
Declarative Structure
```

and:

```text id="ybd89q"
Executable Structure
```

This unifies knowledge and capability without requiring them to be identical.

---

# 44. Policy API

Because runtime-generated intelligence may execute actions or generate consequential structures, governance is required.

A structural object may expose:

```text id="vcd5jc"
allowedContexts

forbiddenActions

requiredEvidence

riskClass

executionLimits

humanApprovalRequirement
```

This allows Open Structural Learning to remain compatible with action governance.

---

# 45. Provenance Is Essential

A Principle should distinguish among:

```text id="qxunua"
direct observation

model prediction

human statement

imported Principle

external PIRU

simulation result

delegated computation
```

These are not epistemically identical.

Therefore every LHS object should preserve provenance whenever possible.

Without provenance, Collective Learning can amplify unsupported structures.

---

# 46. Runtime Generation Creates New Risks

Open structural systems gain flexibility.

They also introduce risks.

A generated structure may be:

```text id="oj8xre"
incorrect

mis-typed

unsupported

malicious

outdated

context-incompatible

circularly derived

overconfident
```

Therefore Runtime Structural Generation requires validation and governance.

Open does not mean trusted by default.

---

# 47. Circular Principle Dependencies

Recursive Principle formation can create cycles:

```text id="33d1hc"
P1 depends on P2

P2 depends on P3

P3 depends on P1
```

A system should detect such cycles.

Some cycles may represent legitimate mutually supporting structures.

Others may create unsupported self-confirmation.

Therefore dependency graphs and provenance are important.

---

# 48. Self-Support Is Not Independent Evidence

Suppose:

```text id="yrzg6k"
P1 generated P2

P2 is then used as evidence for P1
```

This should not automatically count as independent confirmation.

Otherwise the system can manufacture confidence through recursion.

A robust Principle architecture should distinguish:

```text id="ov5t3a"
derived evidence
```

from:

```text id="zwtqxe"
independent evidence
```

This becomes essential in open recursive systems.

---

# 49. Runtime Structure Sandboxing

New structures may initially enter a sandbox state.

For example:

```text id="nx9h4j"
Generated Structure
       ↓
Sandbox
       ↓
Interface Check
       ↓
Evidence Check
       ↓
Policy Check
       ↓
Limited Evaluation
       ↓
Promotion / Rejection
```

This allows experimentation without granting immediate full authority.

---

# 50. Structural Promotion

A useful lifecycle is:

```text id="dxz5la"
Generated
   ↓
Candidate
   ↓
Sandboxed
   ↓
Validated
   ↓
Promoted
   ↓
Reusable
```

Later:

```text id="t7um20"
Challenged
   ↓
Revalidated
   ↓
Revised / Deprecated / Rejected
```

This creates continuity between Runtime Structural Generation and Principle Lifecycle Management.

---

# 51. Temporary vs Persistent Structures

Not every generated structure needs to become permanent.

Some structures are:

```text id="xt9o40"
ephemeral
```

They exist only for one Principle evaluation.

Others are:

```text id="bnq6ej"
reusable
```

and should be preserved.

Thus:

```text id="p9l6b4"
Runtime Structure
      ↓
Reuse Potential?
     / \
   LOW  HIGH
    │     │
Discard  Candidate for Fold-Back
```

This prevents uncontrolled structural accumulation.

---

# 52. Structural Garbage Collection

An open structural system can accumulate obsolete objects.

Therefore it may require:

> **Structural Garbage Collection**

Candidates include structures that are:

```text id="h6ttke"
unused

superseded

invalidated

duplicate

expired

context-obsolete

unsupported
```

Deletion need not erase provenance.

A deprecated structure may remain archived for audit while being removed from active reasoning.

---

# 53. Structural Growth Requires Structural Maintenance

This produces an important general principle:

> **Open-Ended Growth without structural maintenance becomes structural entropy.**

Therefore Principle Intelligence needs both:

```text id="96kwwm"
Growth
```

and:

```text id="b76d8j"
Maintenance
```

including:

* identity,
* versioning,
* deduplication,
* dependency tracking,
* validation,
* deprecation,
* archival,
* and replacement.

---

# 54. Open-LHS and LISP

The relationship to LISP can now be stated carefully.

LISP demonstrated a profound capability:

> **Programs can operate on program structures.**

Open-LHS Principle Intelligence extends the ambition:

> **Intelligence can operate on intelligence structures, including structures not present when the original reasoning system was created.**

And further:

> **Intelligence can generate new intelligence structures required for its own reasoning.**

This is not a claim that LISP itself prohibited dynamic structure.

LISP is famously dynamic and metaprogrammable.

The difference lies primarily in the proposed **knowledge-growth architecture**:

```text id="ah14xs"
Experience
    ↓
Difference
    ↓
New Intelligence Structure
    ↓
Identity / Evidence / Context
    ↓
Immediate Structural Computation
    ↓
Validation
    ↓
Portable Reuse
```

The novelty is not dynamic syntax.

It is open, evidence-bound structural intelligence growth.

---

# 55. Beyond Homoiconicity

Homoiconicity allows code to be represented in a form similar to data.

Open Structural Learning seeks something broader:

```text id="pjc02n"
Observation
Principle
CCC
Trajectory
PIRU
Policy
Evidence
Model Output
```

need not all be code in the same representation.

They can remain heterogeneous while exposing sufficient structural interfaces.

Thus the objective is not:

> Everything is a list.

It is:

> **Everything relevant to Principle reasoning can become an identifiable, inspectable, bindable intelligence object.**

---

# 56. Structural Polymorphism

This suggests a concept of **Structural Polymorphism**.

A Principle may request:

```text id="7bsldg"
EvidenceOfDirectionalCost
```

Different environments may satisfy it through:

```text id="bwhz06"
Trajectory Object

Metric PIRP

World-Model Estimate

Human Evidence

Simulation Result
```

The Principle depends on the structural contract rather than one concrete implementation.

This increases portability.

---

# 57. Principle Interface vs Principle Implementation

A Principle can therefore distinguish:

```text id="rnh26l"
Required Structural Role
```

from:

```text id="4kyrhr"
Specific Structure Providing It
```

For example:

```text id="22mw3e"
Required:
CounterEvidenceProvider
```

could be supplied by:

```text id="ijflg6"
CEDI module

PIRU

human reviewer

simulation

external agent
```

This is analogous to interface-based software design, but applied to intelligence structures.

---

# 58. Runtime Structural Dependency Injection

The analogy can be pushed further.

A Principle may declare:

```text id="cfhr1a"
needs:
    ReachabilityMetric
    CounterEvidenceProvider
    PolicyEvaluator
```

At runtime:

```text id="zzpgs7"
UTN / Registry / Search
        ↓
Find compatible structures
        ↓
Bind
        ↓
Evaluate Principle
```

This can be viewed as:

> **Runtime Structural Dependency Injection for Intelligence.**

The Principle does not need every implementation embedded inside itself.

---

# 59. Principle as an Open Structural Program

A Principle can therefore be viewed not merely as a proposition.

It can behave like an **open structural program**.

Conceptually:

```text id="izt70b"
Principle {
    structural requirements
    evidence requirements
    context
    scope
    compatible interfaces
    validation logic
    lifecycle
}
```

At runtime it can bind available structures.

This makes Principle Intelligence both declarative and computational.

---

# 60. From Rule Matching to Structural Assembly

Traditional:

```text id="zmyn4g"
Match Facts
    ↓
Fire Rule
```

Open-LHS:

```text id="45mw1w"
Inspect Structural Need
        ↓
Bind Existing Objects
        ↓
Identify Gaps
        ↓
Generate / Retrieve / Delegate
        ↓
Assemble Structural Evidence
        ↓
Evaluate Candidate Principle
```

The dominant operation changes from:

> **matching**

toward:

> **structural assembly.**

---

# 61. From Structural Assembly to Structural Growth

If the assembled structure proves reusable:

```text id="1u8gbp"
Runtime Assembly
      ↓
Validation
      ↓
Fold Back
      ↓
Persistent Structural Object
```

Then runtime computation becomes long-term learning.

Thus:

```text id="axzyti"
Assembly
   ↓
Reuse
   ↓
Growth
```

This is the bridge from Principle evaluation to Open Structural Learning.

---

# 62. Open Structural Learning Loop

The complete loop becomes:

```text id="5zv0xi"
WORLD / EXPERIENCE
        │
        ▼
    Observation
        │
        ▼
     Difference
        │
        ▼
Candidate Principle
        │
        ▼
     Open LHS
        │
        ├── Bind Existing Structure
        │
        ├── Retrieve Structure
        │
        ├── Generate Structure
        │
        ├── Compose Structure
        │
        ├── Delegate Structure
        │
        └── Import Portable Structure
        │
        ▼
Two-Way / Evidence Validation
        │
        ▼
    Principle State
        │
        ▼
     Application
        │
        ▼
    New Experience
        │
        ▼
      Fold Back
        │
        ▼
Expanded Structural Intelligence
```

The structural space grows through use.

---

# 63. Open-LHS and Two-Way Search

Open-LHS naturally interacts with Two-Way CCC.

Forward reasoning asks:

```text id="jnjybx"
Given these structures,
what Principle or consequence follows?
```

Reverse reasoning asks:

```text id="ktdvfg"
Given this candidate Principle,
what structures would need to exist
for it to be supported or challenged?
```

The reverse question can trigger runtime generation.

For example:

```text id="8cehdo"
Candidate Principle P
        ↓
What would falsify P?
        ↓
Missing Counter-Evidence Search Structure
        ↓
Generate / Delegate
        ↓
New Evidence
```

Thus Two-Way reasoning can become a generator of new LHS structure.

---

# 64. Reverse Search as Structure Generator

This is deeper than verification.

A reverse query can expose missing representational objects.

```text id="kpm7hd"
RHS / Principle
      ↓
Reverse Search
      ↓
Missing Condition X
      ↓
X has no current representation
      ↓
Generate Structure X
```

Therefore:

> **Reverse reasoning can create new structural vocabulary.**

This is one of the strongest links between Two-Way CCC and Open Structural Learning.

---

# 65. Principle Evaluation as Active Inquiry

Traditional rule evaluation is often passive:

```text id="rq01b8"
Are conditions present?
```

Open-LHS Principle evaluation can be active:

```text id="2hfb2u"
What evidence is missing?

What structure would distinguish
between competing Principles?

Can that structure be generated?

Can an experiment produce it?

Can another agent provide it?
```

Thus Principle Intelligence becomes a form of **active structural inquiry**.

---

# 66. Experiments Can Be Generated from Missing Structure

Suppose two candidate Principles cannot be distinguished with current evidence.

```text id="9yiz86"
P1
vs
P2
```

The system can ask:

```text id="k9a7lu"
What observation would distinguish P1 from P2?
```

This may generate:

```text id="qk20hh"
Experiment E
```

The experiment becomes a runtime structure:

```text id="e05yc7"
P1 + P2
    ↓
Discriminating Experiment E
    ↓
Observation
    ↓
Differential Evidence
```

Reasoning therefore generates not only internal structures but potentially new interactions with the world.

---

# 67. From Passive Learning to Structural Experimentation

The loop becomes:

```text id="rcoklz"
Candidate Principle
        ↓
Missing Evidence
        ↓
Generate Experiment
        ↓
Action
        ↓
Observation
        ↓
Difference
        ↓
Principle Update
```

This is a powerful route toward autonomous scientific and engineering learning.

It also increases governance requirements.

---

# 68. Structural Freedom and Constraint

Open-LHS introduces freedom:

```text id="rb3x9g"
new objects
new relations
new Principles
new PIRUs
new experiments
```

But useful freedom requires constraints.

The system remains bounded by:

```text id="ubqq1f"
physical reality

available evidence

interface compatibility

policy

resources

validation

governance
```

Thus:

> **Open Structural Learning is not unconstrained imagination. It is structural growth under evidence and reality constraints.**

---

# 69. Closed-Space Optimization vs Open-Space Growth

A fixed optimization problem assumes:

```text id="h29z8u"
State Space S
Action Space A
Objective J
```

Then searches:

```text id="3w6xk7"
arg best within S × A
```

Open Structural Learning asks what happens when experience reveals that:

```text id="3jtdhz"
S is incomplete

A is incomplete

J is incomplete

or

the representation itself is inadequate
```

Then intelligence may need to create:

```text id="8ayqzq"
S'
A'
J'
```

or new structural objects connecting them.

Therefore:

> **Optimization chooses within a represented world. Open Structural Learning can revise the represented world in which future optimization occurs.**

---

# 70. Growth of the Possibility Space

This provides a more precise interpretation of open-ended intelligence.

Growth is not merely:

```text id="qqtyod"
more answers
```

It can be:

```text id="8v5vkk"
more representational objects

more structural relations

more executable intelligence units

more Principles

more interfaces

more possible compositions
```

Thus:

> **Growth can enlarge the space in which future answers become possible.**

---

# 71. Open-LHS and Biological Analogy

Biological intelligence does not appear to operate entirely through a fixed human-authored ontology.

Organisms encounter novel situations.

They form new distinctions.

They acquire new behaviors.

They reorganize internal representations.

Human civilization extends this process dramatically by creating:

* new concepts,
* new tools,
* new institutions,
* new scientific theories,
* new languages,
* and new computational systems.

The analogy should not be overstated.

But it motivates an architectural lesson:

> **Intelligence may require not only better calculation inside existing structures, but the ability to create new structures when existing ones are insufficient.**

---

# 72. Intelligence Before Complete Explanation

A newly generated structure can be useful before the system has a complete theory of why it works.

For example:

```text id="3nkhcc"
Observed:
A → B works
B → A fails
```

The system can preserve:

```text id="iv1n1m"
DirectionalRelation(A,B)
```

before explaining the physical cause.

This supports:

> **Intelligence Before Explanation**

in a limited engineering sense.

Useful structure can precede complete theory.

Later explanation may refine the structure.

---

# 73. Explanation as One Structural Projection

A Principle may support multiple explanations under different perspectives.

For example:

```text id="d2w05x"
Behavioral Principle
```

may later receive:

```text id="h84hmu"
Physical Explanation

Energy Explanation

Policy Explanation

Causal Explanation
```

No single explanation necessarily exhausts the Principle's operational value.

Thus:

> **Explanation can be treated as one perspective-bound structural projection of intelligence rather than the entirety of intelligence itself.**

---

# 74. Open-LHS and Perspective Binding

Because different perspectives may introduce different structures, the LHS should preserve perspective.

For example:

```text id="dqcrsp"
Physical Perspective:
friction

Planning Perspective:
transition cost

Safety Perspective:
risk

Policy Perspective:
permission
```

All may refer to the same underlying situation.

An Open-LHS Principle can combine them without pretending they are identical.

---

# 75. Multi-Perspective Principle Formation

A candidate Principle may therefore emerge from:

```text id="e4nb7w"
Physical Evidence
       +
Behavioral Evidence
       +
Policy Evidence
       +
Counter-Evidence
       ↓
Multi-Perspective Principle
```

This is another advantage of heterogeneous structural objects.

A single representation need not dominate all reasoning.

---

# 76. Open-LHS and Structural Civilization

Once intelligence structures can be:

```text id="2mktsf"
created

identified

validated

transported

combined

challenged

revised
```

they begin to behave less like private model activations and more like cumulative cultural artifacts.

Human civilization externalized intelligence into:

```text id="ajh7nq"
language

writing

mathematics

books

science

software

institutions
```

Machine intelligence may similarly require persistent external intelligence structures.

Open-LHS provides a mechanism by which newly externalized structures can immediately become usable by other intelligence.

---

# 77. From Model Monolith to Intelligence Ecology

A monolithic architecture tends toward:

```text id="e0r9hq"
Model
 ├── perception
 ├── memory
 ├── reasoning
 ├── policy
 ├── planning
 └── knowledge
```

An open structural architecture may increasingly resemble:

```text id="51xrz6"
Model Substrate
      │
      ▼
Structural Runtime
      │
      ├── Principles
      ├── CCCs
      ├── Metrics
      ├── Triggers
      ├── Policies
      ├── PIRPs
      ├── PIRUs
      ├── Evaluators
      └── Evidence Objects
```

The result is not necessarily a smaller model.

It is a more distributed location of intelligence.

---

# 78. Where Should Intelligence Live?

Open-LHS exposes a deeper architectural question:

> **Which intelligence should remain inside model weights, and which intelligence should become explicit runtime structure?**

Some intelligence is naturally distributed:

```text id="3yd41m"
perception

low-level representation

high-dimensional prediction
```

Other intelligence may benefit from externalization:

```text id="06f4j1"
Principles

constraints

policies

metrics

triggers

evidence

evaluators

search strategies
```

The boundary need not be fixed.

Open Structural Learning allows intelligence to migrate toward the representation most useful for reuse.

---

# 79. Externalization Criterion

A candidate structure may be worth externalizing when it can preserve:

```text id="tcnkpb"
Semantics
Identity
Context
Evidence
Interface
Reuse Value
```

while becoming independently:

```text id="cm3mzk"
testable

portable

composable

revisable
```

This gives a preliminary criterion:

> **If intelligence can be externalized without destroying its useful semantics, and the externalized form increases validation, portability, or reuse, it is a candidate structural intelligence object.**

---

# 80. Open-LHS Principle API

A conceptual Principle interface may include:

```text id="ng8ex6"
Principle {
    identity
    type

    lhs_requirements
    lhs_bound_structures
    lhs_missing_structures

    structural_statement
    scope
    context
    perspective

    evidence
    counter_evidence
    provenance

    compatible_interfaces
    generation_options
    delegation_options

    validation_method
    confidence
    lifecycle_state

    derived_structures
    revision_history
}
```

The important additions for Open-LHS are:

```text id="8nlx4h"
lhs_requirements

lhs_bound_structures

lhs_missing_structures

compatible_interfaces

generation_options

delegation_options
```

These make the LHS explicitly extensible.

---

# 81. Open-LHS Evaluation Skeleton

A conceptual runtime can be written as:

```text id="uxd4ex"
INPUT:
    Candidate Principle P
    Current Context C
    Available Structures S

STEP 1:
    Inspect P's structural requirements.

STEP 2:
    Bind compatible structures from S.

STEP 3:
    Identify missing structural roles.

STEP 4:
    For each missing role:
        search
        retrieve
        generate
        compose
        unfold
        or delegate.

STEP 5:
    Validate newly obtained structures.

STEP 6:
    Bind accepted structures into the LHS.

STEP 7:
    Evaluate structural sufficiency.

STEP 8:
    Search supporting and counter-evidence.

STEP 9:
    Evaluate or revise P.

STEP 10:
    Identify reusable runtime structures.

STEP 11:
    Fold back validated reusable structures.

OUTPUT:
    Principle State
    Evidence State
    New Structural Objects
    Reuse Candidates
```

This is a structural reference architecture rather than a fixed implementation.

---

# 82. The Open-LHS Grand Loop

The complete architecture can be summarized as:

```text id="k92bsz"
                  EXPERIENCE
                      │
                      ▼
                  DIFFERENCE
                      │
                      ▼
             CANDIDATE PRINCIPLE
                      │
                      ▼
                 OPEN LHS
                      │
       ┌──────────────┼──────────────┐
       ▼              ▼              ▼
   Existing       Retrieved       Imported
   Structure      Structure       Structure
       │              │              │
       └──────────────┼──────────────┘
                      │
                Missing Structure?
                  /          \
                YES           NO
                 │             │
                 ▼             │
      Generate / Compose       │
      Unfold / Delegate        │
                 │             │
                 ▼             │
          New Structure        │
                 │             │
                 └──────┬──────┘
                        ▼
                  LHS Binding
                        │
                        ▼
               Two-Way Validation
                        │
                        ▼
                Principle State
                        │
                        ▼
                 Runtime Use
                        │
                        ▼
                  New Evidence
                        │
                        ▼
                    Fold Back
                        │
                        ▼
             STRUCTURAL GROWTH
                        │
                        └────→ EXPERIENCE
```

This is the core Open Structural Learning loop.

---

# 83. Three Design Axioms

The architecture can be compressed into three design axioms.

## Axiom 1 — Open-LHS Principle

> **A Principle may operate over any identifiable and structurally compatible intelligence object, including structures that did not exist when the Principle system was created.**

## Axiom 2 — Runtime Structural Extension

> **Principle evaluation may retrieve, generate, compose, unfold, or delegate the creation of new structures required to complete or improve its structural evidence space.**

## Axiom 3 — Evidence-Bound Structural Growth

> **Newly generated structures do not become trusted intelligence merely by existing; they require identity, context, provenance, evidence, compatibility, and an appropriate validation lifecycle.**

Together:

```text id="74ihr7"
OPENNESS
   +
GENERATION
   +
ACCOUNTABILITY
   ↓
Open Structural Learning
```

---

# 84. The Deeper Transition

The progression can now be stated as:

```text id="ovb7kl"
Rule Engine
    ↓
Reason over predefined conditions
```

```text id="w0kb2j"
Learning System
    ↓
Learn values and representations
```

```text id="fgn2pq"
Principle Intelligence
    ↓
Extract reusable structure
```

```text id="khdv3e"
Open-LHS Principle Intelligence
    ↓
Reason over extensible intelligence structures
```

```text id="zwag7x"
Open Structural Learning
    ↓
Generate new structures required
for future intelligence
```

This is not simply more inference.

It changes what inference is allowed to operate on.

---

# 85. Conclusion

Principle Intelligence begins with a simple idea:

> Reusable structural knowledge can emerge from experience.

Open-LHS Principle Intelligence adds a stronger claim:

> **The structures participating in Principle formation and evaluation need not all be known before reasoning begins.**

A Principle may operate over:

* observations,
* differences,
* trajectories,
* CCCs,
* Principles,
* counter-evidence,
* policies,
* Calling Graphs,
* world-model outputs,
* PIRPs,
* PIRUs,
* and runtime-generated structures.

If a required structural object is missing, the system may search for it, retrieve it, generate it, compose it, unfold it, or delegate its creation.

The new structure can then be identified, typed, contextualized, validated, and bound into the Principle's LHS.

This creates a fundamentally different learning loop:

```text id="idb8mf"
Reason
  ↓
Discover Missing Structure
  ↓
Create Structure
  ↓
Reason With New Structure
  ↓
Validate
  ↓
Preserve Reusable Structure
  ↓
Expand Future Reasoning Space
```

The central proposition is therefore:

> **Reasoning can create the representational structures required for its own reasoning.**

This does not mean unrestricted self-invention.

Reality remains a constraint.

Evidence remains a constraint.

Policy remains a constraint.

Structural compatibility remains a constraint.

Validation remains a constraint.

But inside those constraints, the representational space need not remain frozen.

The result is a transition from:

```text id="hdmrlm"
Closed-Space Computation
```

toward:

```text id="q8wm3l"
Open-Space Structural Growth
```

and from:

```text id="m80iwb"
Intelligence operating on data
```

toward:

```text id="56ws30"
Intelligence operating on intelligence structures
```

and ultimately:

```text id="1jbp5k"
Intelligence generating new intelligence structures
required for its own continued growth.
```

This is the central computational foundation of **Open Structural Learning**.

---

## Next Document

**PI-004 — Principle, CCC, and Two-Way CCC**

The next document separates three related but distinct structural mechanisms:

* Principle as reusable invariant, constraint, or relation;
* CCC as context-bound operational structure;
* Two-Way CCC as reverse structural search, validation, competing-explanation, and counter-evidence mechanism.

It develops the relationship:

```text id="vp4m9c"
Principle
    ↓
Context Binding
    ↓
CCC Instantiation
    ↓
Two-Way Search
    ↓
Evidence / Counter-Evidence
    ↓
Principle Revision
```

and examines how Two-Way reasoning can both validate Principles and expose the missing structures required for further Open-LHS growth.

---

## Repository Thesis

> **Do not freeze the language of intelligence before intelligence begins.
> Let evidence create structure.
> Let structure enter reasoning.
> Let reasoning request new structure.
> Let validated structure become reusable intelligence.
> Let the structural space grow with experience.**

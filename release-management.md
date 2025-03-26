[Home](README.md) | [Why](why.md) | **[Pillars](pillars.md)** | [Systems](systems.md) | [Team](team-model.md)

# Release Management

**Release Management** is a critical pillar of the Released Method. It ensures every software release is reliable, production-ready, and aligned with quality expectations — without dragging delivery timelines or relying on luck. This pillar covers five core areas:

- **Quality Bar**  
- **Automated Release Process**  
- **Staging and Production Environments**  
- **Release Authorization**  
- **Version Control**

---

## Quality Bar

The **Quality Bar** defines what “ready to release” actually means. It provides a clear, objective threshold for when software is stable enough to ship — balancing quality with time-to-market.

Your bar should be high, but realistic. Typical criteria include:

- Remaining open tasks  
- Open bug count and severity  
- Percentage of features tested  
- Percentage of features documented  

Each feature/task progresses through tracked phases to ensure nothing is missed.

### Task Lifecycle

- **New** – Proposed and awaiting triage or assignment  
- **In Development** – Actively being built; iterated until code complete  
- **In Test** – Undergoes validation, regression, and coverage checks (see [Testing & QA](testing-qa.md))  
- **In Documentation** – Features documented and docs tested for clarity and completeness  
- **Closed** – Task fully delivered; ongoing bug fixes tracked separately  

### Quality Bar Metrics

- ✅ **All tasks closed** – No active development pending  
- 🐞 **No open Sev 1 / Pri 1 bugs** – Showstoppers are resolved or blocked  
- 🚩 **Punting** – Deliberate deferral of tasks that no longer meet release scope or timing  
- 👥 **Triage Team sign-off** – Final approval from the cross-functional release authority

This gives you a shared, unambiguous definition of “done” at release scale.

---

## Automated Release Process

Manual deployments are slow, error-prone, and unsustainable. The Released Method mandates **automation by default** — from build to release.

Automation should include:

- Build pipelines (CI/CD)  
- Automated tests (unit, integration, regression)  
- Packaging and deployment scripts  
- Environment validation checks  

Your goal is repeatable, reliable, hands-off releases.

---

## Staging and Production Environments

You ship with confidence when your testing environment mirrors the real world. That’s why the Released Method separates:

- **Staging** – Mirrors production as closely as possible; used for final validation  
- **Production** – The live, customer-facing environment

Staging is not optional. It’s your last safety net.

---

## Release Authorization

Shipping software is a team sport. **Release authorization** is a structured process led by the Triage Team, which includes engineering, QA, product, and sometimes support or marketing.

- Any member can veto a release based on serious concerns  
- Final go/no-go is based on agreed Quality Bar metrics  
- Releasing is a decision — not a default

This ensures accountability without bureaucracy.

---

## Version Control

Version control underpins all of this. It’s more than just source history — it’s the foundation for traceability, rollback, and collaboration.

Your version control strategy should:

- Support parallel development (branching model)  
- Tie changes to tasks and bugs (issue tracking integration)  
- Maintain clean release tags and history  
- Be accessible to all team members, including QA and support

Git is the standard. Use it well.

---

## Final Word

Release Management isn’t just a checkpoint at the end — it’s a continuous discipline. The Released Method bakes it in from day one to ensure every build is production-worthy, every release is predictable, and your customers never get a “rough edge” build again.

# Testing and Quality Assurance

In the Released Method, **Testing and Quality Assurance (QA)** are not afterthoughts — they’re embedded into the development process from day one. This pillar ensures your software is reliable, robust, and ready for real-world use, with a disciplined, layered approach to testing and a streamlined system for managing bugs.

---

## 🔍 Testing Methodologies

The Released Method applies multiple layers of testing to catch issues early, reduce risk, and improve maintainability.

### ✅ Unit Tests
- **What**: Test individual components, functions, or classes in isolation
- **Why**: Catch bugs early at the smallest level of code
- **How**: Automated, fast, and run continuously in CI pipelines

---

### 🔬 Code Analysis
- **What**: Static analysis tools that scan source code without executing it
- **Why**: Identify syntax issues, bugs, vulnerabilities, and style violations
- **Tools**: ESLint, SonarQube, StyleCop, etc.

---

### 🤖 Automated UI & Integration Tests
- **What**: Simulate real user flows and system-level interactions
- **Why**: Validate end-to-end functionality, catch regressions early
- **When**: Run on each build or deployment

---

### 🧪 Manual Testing
- **What**: Human-driven exploratory and scenario testing
- **Why**: Catch issues automation misses (usability, edge cases, design quirks)
- **When**: Especially valuable before major releases or after new features

---

## 🐛 Bug Reporting and Management

A good bug tracking system enables fast resolution and accountability. Every bug should include:

- **Title** – Short and descriptive
- **ID** – Unique identifier for tracking
- **Description** – What went wrong, steps to reproduce, expected vs actual behaviour
- **Severity & Priority** – Set during triage
- **Repro Steps** – Clear instructions to consistently recreate the issue
- **Labels** – For categorisation and workflow automation
- **Comments** – For status updates and team communication
- **Originator** – Who reported the bug
- **Owner** – Who is currently assigned to fix it

---

## 🧨 Severity Levels

Severity defines how badly the bug impacts the product:

1. **Critical** – System is down, data loss, or security risk
2. **Major** – Key functionality broken, but with a workaround
3. **Minor** – Cosmetic or non-blocking issue

---

## 📌 Priority Levels

Priority defines how urgently the bug should be fixed. Set during triage:

- **P1** – Fix immediately
- **P2** – Fix in next sprint
- **P3** – Low urgency, fix when convenient
- **Deferred** – Logged, but not scheduled

---

## 🩺 Triage Process

Triage is a regular session to assess, prioritise, and assign bugs or feature requests.

- **Actions**: Investigate, Approve, Reject, or Defer
- **Assignment**: Allocated to a developer, tester, or analyst
- **Review Loop**: Continuous reassessment ensures relevance and proper priority

---

## 🔁 Post-Triage: Fix, Validate, Regress

Once fixed, bugs go through validation and regression checks:

- **Validation** – The originator or QA confirms the bug is resolved
- **Regression Testing** – New tests are added to ensure the issue doesn’t return
- **Closure** – The bug is marked as Closed only after confirmation and coverage

---

## 🧠 Why It Matters

QA in the Released Method isn’t about bureaucracy — it’s about confidence. Testing ensures:

- Your product behaves as expected
- Your team isn’t firefighting post-release bugs
- Your users trust your software
- Your business avoids downtime, rework, and customer churn

---

## Final Word

Testing and QA in the Released Method are disciplined, automated where possible, and reinforced by strong bug triage and feedback loops. It’s a system that scales with your team — and protects your reputation as you ship faster, smarter, and with fewer surprises.

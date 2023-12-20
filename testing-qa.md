[Home](README.md) | [Why](why.md) | **[Pillars](pillars.md)** | [Systems](systems.md) | [Team](team-model.md)

# Testing and Quality Assurance

In the Released Method, Testing and Quality Assurance are pivotal for ensuring software reliability and customer satisfaction. This process follows a comprehensive and structured approach, encompassing various types of testing and a systematic handling of bugs.

## Testing Methodologies
The testing process incorporates multiple layers to ensure thorough evaluation:

### Unit Tests
- **Purpose**: Tests individual components or functions for expected operation.
- **Automation**: Typically automated to run frequently during development cycles.

### Code Analysis
- **Objective**: Identifies potential issues at a code level using automated tools.
- **Scope**: Includes checking for syntax errors, potential bugs, and style inconsistencies.

### Automated Tests
- **Focus**: Simulates user interactions with the UI to verify functionality.
- **Benefits**: Reduces the need for manual testing and ensures repeatability.

### Manual Tests
- **Role**: Performed by human testers to catch issues that automated tests may miss.
- **Importance**: Critical for assessing usability and real-world application scenarios.

## Bug Reporting and Management
A structured approach to bug reporting enhances the efficiency of resolving issues:

### Bug Report Components
- **Title**: Concise summary of the issue.
- **Id**: Unique identifier for tracking.
- **Description**: Detailed account of the issue, reproduction steps, and impact.
- **Severity and Priority**: Assessed to prioritize bug fixing efforts.
- **Comments**: For ongoing updates and communication regarding the bug.
- **Labels**: For categorizing and workflow management.
- **Originator and Owner**: Denoting the reporter and current handler of the issue.

### Reproduction (Repro)
- **Necessity**: Clear, step-by-step instructions to replicate the bug.
- **Details**: Includes conditions under which the bug occurs and why the behavior is incorrect.

## Severity Levels
Defines the impact of the bug on user experience or product functionality:

1. **Critical**: Renders the product unusable or causes major malfunctions.
2. **Major**: Significant impact but with potential workarounds.
3. **Minor**: Annoying issues that do not significantly impede normal operation.

## Priority Setting
- **Determined in Triage**: Prioritization is essential for effective bug resolution order.
- **Categories**: Ranging from high urgency (priority 1) to lower urgency (priority 2, 3, etc.).

## Triage Process
Triage is a crucial stage where bugs and requests are evaluated and actioned:

- **Actions**: Include Investigate, Approve, Reject, or Defer.
- **Resolver Assignment**: Allocates a team member to address the approved issues.
- **Review and Feedback Loop**: Ensures continual assessment and action on bugs.

## Post-Triage Actions
Once a bug is resolved, validation and regression testing are key:

- **Validation**: The originator verifies the resolution of the issue.
- **Regression Testing**: Development of tests to prevent recurrence of the same issue.

## Closing the Loop
After successful validation and regression testing, the bug is marked as closed, indicating a complete resolution. This comprehensive approach to Testing and Quality Assurance in the Released Method ensures that software products are robust, reliable, and meet the highest standards of quality.
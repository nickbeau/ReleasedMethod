[Home](README.md) | [Why](why.md) | **[Pillars](pillars.md)** | [Systems](systems.md) | [Team](team-model.md)

# Release Management

Release Management is a critical component of the Released Method, encompassing various processes and checks to ensure that each software release is robust, reliable, and meets quality standards. This pillar includes key elements such as Quality Bar, Automated Release Process, Staging and Production Platforms, Release Authorization, and Version Control.

## Quality Bar
The Quality Bar defines the criteria for determining when a product or release is ready for deployment. It balances the need for perfection with the practicality of meeting release deadlines. The Quality Bar is essential for guiding teams on when the software is sufficiently refined and tested to be considered "shippable". This criterion varies but typically includes measures like:

- Number of outstanding tasks.
- Number of outstanding bugs.
- Proportion of tasks tested.
- Proportion of tasks documented.

Each task in a user story or feature undergoes various states from New (Unassigned) to Closed, ensuring comprehensive development, testing, and documentation.

### Task Phases
- **New**: The task is proposed and awaiting approval.
- **In Development**: Once assigned, the developer iterates until the task reaches code completion.
- **In Test**: The task undergoes thorough testing. Bugs are identified and logged. Testing metrics, such as code coverage, are considered (see [Testing & QA](testing-qa.md)).
- **In Documentation**: Post-testing, the task moves to documentation, where its usage and functionalities are detailed. Documentation itself is tested for completeness and accuracy.
- **Closed**: The task is deemed complete, with ongoing bug resolution.

### Quality Bar Metrics
1. **All Tasks Closed**: Signifies the end of active development for the release.
2. **No Open Bugs**: Indicates that no critical bugs are pending for the current release.
3. **Punting**: Deciding to move a task to a subsequent release based on its severity and priority.

### Released Method Quality Bar
In the Released Method, the quality bar is defined by:
1. Completion of all tasks.
2. Absence of open Sev 1, Pri 1 Bugs.
3. Consensus from the Triage Team for release.

## Automated Release Process
Implementing an automated release process streamlines deployment, reducing human error and enhancing efficiency. This involves automated builds, testing, and deployment scripts, ensuring consistent and reliable release cycles.

## Staging and Production Platforms
Separating staging and production environments is crucial for safe testing and deployment. Staging environments replicate production settings for final testing, while production environments host the live, user-facing application.

## Release Authorization
Release authorization is a collaborative decision-making process, often involving a Triage Team. Any member can veto a release to address significant concerns, ensuring thorough review and consensus before deployment.

## Version Control
Effective version control is indispensable for managing changes in software development. It tracks modifications, supports concurrent work, and facilitates collaboration, ensuring a coherent and organized development process.

The Release Management pillar is fundamental in ensuring that each software version is released with confidence, meeting the high standards of quality and reliability that are hallmarks of the Released Method.
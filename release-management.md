[Home](README.md) | [Why](why.md) | **[Pillars](pillars.md)** | [Systems](systems.md) | [Team](team-model.md)
# Release Management
The Release Management pillar consists of the following:

* Quality Bar
* Automated Release Process
* Staging and Production Platforms
* Release Authorization
* Version Control

## Quality Bar
It's really difficult to decide when a release or product is "done". In fact it's pretty easy to keep going making things incrementally bettwe without ever really achieving a release.

Most successful startup companies reward the release or "ship" with an award, because for a company, releasing software is the most important task a development team can perform.

However, with the pressure on making the software "perfect" coupled with the pressure of releasing the software, leaders need a way to understand when the software is good enough to ship.

This is the role of the Quality bar. Once software has met the quality bar, it is ready to release.

I espouse a certain quality bar, but you are, of course free to implement whichever quality bar you wish.

There are certain things we can measure in software development and items we cannot. Items we can measure are:

* Number of outstanding tasks
* Number of outstanding Bugs
* How many tasks have been tested
* How many tasks have been documented.

If we were to take a single **user story** or **feature**, this will have a number of tasks. A task should go through the following states:

* New [Unassigned]
* New [Assigned]
* In Development
* In Test
* In Documentation
* Closed

The phases are as follows:

### New
A New task has been considered, and *requested* but is not currently approved or in active development. Once a task has been approved, it is assigned to a developer. The developer moves it between New [Assigned] and In Development until the task is considered "code complete"

## In Test
Once a task is code complete, it is moved to the test team who *attempt to test as much of the results as they can*. Commonly testing will have target metrics such as code coverage or features coverage. See [Testing & QA](testing-qa.md) for more information.

Once all bugs have been raised (not they have been solved), the task is considered tested and moves to the In Documentation phase, even while bugs are being fixed.

## In Documentation
Once a task has been tested, it is released to the User Education team to write documentation on how to use the individual feature within the task. Once the documentation is written, it too goes through a similar test process. Once the documentation is written (complete) and all bugs have been raised (tested), the task is marked as closed - even if there are still outstanding bugs.

## Closed
The task is complete. Even if there are bugs to resolve, the task is finished and we are just fixing bugs and issues. 

## Measure 1
One Measure of a quality bar is: **All tasks slated for this release are closed** - That means there is no more development to do in this release and every item has been tested and documented.

## Bugs
I wont' go into why we call problems with software or documentation bugs, but a bug is something wrong with the software or documentation. Bugs are identified and move through a formal process to be resolved.

## Measure 2
One measure of a quality bar is **There are no open bugs for this release** - It should be noted that this doesn't mean there are no bugs, quite the contrary, it means there are no bugs considered important enough to block this release.

## The art of punting
Punting is the process of moving a work item from this release to a future release (commonly the next). It is used by triage to determine if an items **priority** or **severity** warrants fixing.

## Measure 3
Severity and Priority items are considered in the quality bar, for example, any bug under severity one, priority one will be able to be punted to the next release.

## Our Quality Bar
Following on from this one defines the released method quality bar as follows:

1. All tasks are closed
2. There are no open Sev 1, Pri 1 Bugs
3. The Triage Team agrees to release

As Triage is a team of peers, it is common practice to include triage in a release authorisation process, ensuring that everyone agrees to release or not.

## Release Authorisation
Release Authorisation is the process whereby Triage agrees to release (or not release) this version of the software or solution. Commonly, any individual can block the release, without repercussion, their issues will be reviewed and docuemnted by triage and resolved to their satisfaction.

Following that, release can occur.
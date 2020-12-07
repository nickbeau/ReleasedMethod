[Home](README.md) | [Why](why.md) | **[Pillars](pillars.md)** | [Systems](systems.md) | [Team](team-model.md)
# Testing and Quality Assurance
Testing and Quality Assurance follows a cyclical model as follows:

## Testing
  * **Unit Tests** are automated components of electronic testing of the software to ensure functions operate as desired 
  * **Code Analysis** is the process of analysing code for defects at a line by line level using automated tools. 
  * **Automated Tests** commonly automate the user interface and test the UI does what is required. 
  * **Manual Tests** are manual tests performed by humans to ensure the application works as desired.

The person (or manager of a system) which creates a bug is called the **originator**

## Bug

The result of testing is a **bug**. A **bug** is a record of something being wrong with the software. Bugs should include the following detail:

| Item | Description |
| -- | -- |
| Title | One line, simple description of the Bug |
| Id | Preferably an integer, representing the bug number |
| Description | a detailed description of the bug, describing the issue, how to **reproduce it** and the impact |
| Severity | The impact of this bug to the software or customer |
| Priority | The order in which the fix should be developed |
| Comments | An ongoing commentary of this issue |
| Labels | Additional Labels depending on workflow |
| Originator | The individual who created the bug report |
| Owner | The individual who currently owns this bug report |




People are commonly very poor at creating bug records that can be resolved easily by a developer. In order for a bug to be a "good bug" it needs to have a **repro**

## Repro

Repro or reproduction is step-by-step instructions a developer can take to reproduce or recreate the behavior classified as a bug. 

The Repro should be described in discrete steps, showing a developer how to execute enough to reproduce the errant behavior. It should then describe why the observed behavior is errant.

## Severity

Severity is the impact this bug has on the product or customer experience as a whole, severities are as follows:

1. Cannot use the product. This bug breaks the product or feature
2. Difficult to use the product. This bug makes it unintuitive or difficult to use the product and requires a work around.
3. Annoying, but does not stop a workflow.

*the severity is commonly chosen by the bug originator*

## Priority

The Priority is how important the development team consider this bug to be and in which order it will be addressed. Development staff are encouraged to resolve priority 1 items first, followed by 2 and so on.

Priority is set in Triage.

## Triage
Triage is the process of analysing requests to the project team and managing them in a highly efficient manner. In short, anyone can raise a request or issue for the team and it is the triage team which uses the triage process to manage and process the request. 
 
During a short meeting the team agrees one of the following actions on a request. 
 
- **Investigate** - the request will be investigated further
-  **Approve** - the request will be done by the team. An approved request is always assigned to a **resolver**.
-  **Reject** - the request will be denied. This is normally done if the issue cannot be reproduced (called no repro) or it is designed to work that way and is not a bug (by design). 
-  **Defer** - the request will be deferred. Triage have the power to defer (punt) a bug report to a future version of the software, especially if that report has low priority and/or severity.
  
Once the bug has been assigned, a **resolver** will attempt to 1resolve the bug. Once they believe they have resolved the bug, they makr the bug report as **resolved** and re-assign it to the **originator**

The **resolver** or **originator** both have the ability to revert the bug for discussion at triage. Commonly this is performed by unassigning the bug, however it can be done by adding a label called Triage.


Once the bug has been resolved, the **originator** is responsible for ensuring the bug has been fixed. They do this by:

- **Validate** the originator ensures that the bug is no longer present
- **Regression Test** - it is best practice for the test team or originator to develop a regression test to ensure this issue never occurs again.

Once ths bug is resolved, it is marked as closed.
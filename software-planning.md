[Home](README.md) | [Why](why.md) | **[Pillars](pillars.md)** | [Systems](systems.md) | [Team](team-model.md)

# Software Planning and Development

The Software Planning and Development is run according to a cyclical life cycle model as follows:

* Envision
* Prototype
* Architect
* Validate

The Released Method adheres to the principles of the [Agile Manifesto](https://agilemanifesto.org/). It does this by running this model across a series of **sprints**. Sprints are defined as a time boxed, discrete work output that fulfils the Agile Manifesto by:

> Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.

Released Method sprints always deliver valuable working software for the customer to work with to allow them to understand what is possible and adapt their requirements based on their new understanding.

> Welcome changing requirements, even late in development. Agile processes harness change for
the customer's competitive advantage.

The Released Group Specification, automatically documented by the tools at [Project Documentor](https://github.com/nickbeau/project-documentor) allows us to host specification items as GitHub issues and change them as necessary.

> Deliver working software frequently, from a couple of weeks to a couple of months, with a 
preference to the shorter timescale.

Released Group Sprints take a week of full time work, from everyone, but can occur over 1 to four weeks elapsed and always deliver a release of working software.

> Business people and developers must work together daily throughout the project.

The Released Method Team model is a single team, regardless of discipline.

> Build projects around motivated individuals. Give them the environment and support they need,
and trust them to get the job done.

The Released Method team model is a single team, highly motivated to deliver results. The job of the process is to get out of the way and enjoy the results.

> Working software is the primary measure of progress.

> Agile processes promote sustainable development. The sponsors, developers, and users should be able
to maintain a constant pace indefinitely.

> Continuous attention to technical excellence and good design enhances agility.

> Simplicity--the art of maximizing the amount of work not done--is essential.

> The best architectures, requirements, and designs emerge from self-organizing teams.

> At regular intervals, the team reflects on how to become more effective, then tunes and adjusts
its behavior accordingly.

These phases are defined below

## Envision

In this phase the project is initially defined, it consists of three major processes:

* Brainstorm
* Hypothesis
* Wild Ideas

For most, the process of envisioning software is a boring process that involves lots of documentation. The Released Method involves asking ourselves, what do we want to solve, and ignores the how do we solve it. The team should be allowed to hypothesise anything. History, opinions and other external influences should not be allowed to interject here. This is why commonly, long term development teams employ a short term agile team to launch them into a new trajectory wherein they take over.

The output of Envisioning is a set of github issues labelled as follows:

- **FunctionalReq** - A functional requirement is something needed to work for the end user. It should describe how a user achieves an outcome by using the software, and needs to be better than the alternatives.
- **NonFunctionalReq** - A Non functional requirement is something like scalability, security, performance, design which does not affect the function but is as important.
- **Pri1** - A Priority One issue must be done immediately for the product to have any value
- **Pri2** - A Priority two issue is very important for commercial success
- **Pri3** - A Priority three issue is a "nice to have"
- **SpecRequired** - It's something we want but we haven't fully documented it yet


## Prototype
In this phase, initial prototypes are developed to see if the product is feasible. There are thre
e major processes:

* Build
* Verify
* Fail Fast

We work to construct a working version of the different components. Initially, where experimentations is required, these can be rapidly developed prototypes. Should the concept of feature be feasible, the team should note the results and move to the next one. At all times, these prototypes should be available to the customer.

## Architect

Once out of the prototype phase, the build of the product components starts for real. Developers follow the processed below:

* Develop
* Document
* Refine

To develop, we take a prototype and add the items necessary for commercial code, including security, logging, error checking and bounds checking. We normally write unit tests here to ensure the feature or item works robustly. Finally we document what a 3rd party needs to know about the feature or item.

Unit tests force us to refine the component for security speed and performance.


## Validate

Once the product component is ready, it goes through the following major processes:

* Validate
* Optimize
* Enhance

We validate the component against the written and agreed specification. If it meets it, we discuss if it is what the client wants or needs. We make sure its what everyone wants, then we run through the code, reviewing and improving where we can and raise issues for future refactoring. The code gets released and the burndown now contains new items to perform.


## The Sprint

A spring contains all the items above, for one or more features. Sprints are initially articulated based on a defined specification, but as the project continues can be used differently based on the changing customer requirements.

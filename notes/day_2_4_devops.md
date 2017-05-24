# Brownfields DevOps in Practice

- Damian Brady (@damovisa)

## Establish a baseline

How do we work, build, deploy, measure now? 

A step-by-step documentation document doesn't always get done.
You should document/scribe how a deployment actually goes, so that you can automate it.
Be honest, don't blame, so that you can accurately automate.

## Get a good state

How do you modify software so that it can be agile?

- Get to __one__ codebase
    - Branching stategies too
    - Code on master as much as possible
    - The releasable version of your software should be from master
- Isolate variations 
- Externalize Configurations (web.config appsettings or connection strings)
    - Set the configuration at deployment time
    - Read the configuration at runtime
    - Choose an implementation at runtime
- Build once, deploy many
    - The same btyes everwhere
    - The same deployment process everywhere
- Get your versioning right
    - Semantic versioning (Semver)
    - Every version has a unique version
    - Newer code has a higher version
- Measure in production
    - Seq, Seary log ? 
    - New relic ? 

## Deploy Without Drama

Deployments should be stateless, and we shouldn't be attached to a particular version.

Database backups are terrible idea, because they give you false sense of security.

Automated deployments to databases: 

- Migration Scripts
    - DbUp
    - EF Migrations
    - Readyroll
- Compary and Apply
    - SqlCompare

### Transistional Deployments

An acknowledgement of "maybe i'll have to rollback"

Database compatibility __one__ version back

## Improve your cycle time

How fast can you push a fix?

### Automation is key.

- Humans make mistakes, but scripts are great at doing things over and over again
- Automate one thing at a time

### Build a pipeline.

- Automation and filters (oppounities to stop bad stuff to production)

- Build
    - Does it merge/compile?
- Test
    - Do the tests past?
- Deploy+Test
    - Do the tests still pass?
    - Does the UI work?
    - Can we still talk to our DB?
    - Did our deployment work?
- Production

Use "Red, Green, Refactor" with the pipeline.
Prevent a mistake in the pipeline from happening again.
Fix your pipeline as you go.

### Feature Flags

Branch by Abstraction pattern.

- Deploy it turned off (even if it's turned off)
    - As long as you have fine grained control, you can turn if on.
- Test in production
- Separate "Launch" from "Deploy"

## Culture Shift

- No Silos
    - Developers shouldn't be separate from Operations
    - Prevent separating people by names
    - Instead, create a "Task Force"
        - A team to workout what goes wrong, that can be a managers idea
- Fix it for the next time

People and tools, working together, to do the right thing, faster. 

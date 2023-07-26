# Project checklist

### From architecture to release


## Introduction 

The idea of this checklist is to serve as a reminder of all the tiny steps in the software creation process. By taking note of all these steps we try to achieve higher quality and reduce delays caused by missing elements.

The list is not exhaustive and may not be applicable for every project feel free to modify it according to your specific needs or propose enhancements by opening an issue or a PR. 

It should serve as a guide for the whole team during the software creation process from the architecture to the release phases.


## Why should we use it

 - To have a guide for through each step of the process from architectural proposal, build, release and maintenance
 - To provide a basic set of rules to ensure the quality of the service 
 - To help reviewers identify possible problems on both implementation and architectural level as early as possible
 - To help with the project estimation by bringing up early, tasks that are often missed in the planning process

# Checklist

## Architecture
- Gathering requirements
  - Functional - what we expect the system to do
  - Non-functional - how the system should behave
  - Constraints - limitations imposed by the environment or 3rd party rules e.g. GDPR
  - Dependencies - both internal and external dependencies e.g. compatibility with existing systems
  - Success metrics - how we measure the success of the project
- System design
  - High level architecture - how the system will be structured
  - Components - what are the components of the system
  - Interfaces - how the components will communicate with each other
  - Data model - how the data will be stored
  - Security - general security requirements, identifying private and public data
  - Scalability - how the system will scale

- Component design
  - Low coupling - how to reduce the dependencies between components
  - High cohesion - how to group related functionality together
  - Single responsibility - components should do one thing and do it well
  - Reuse and extendability - how to ensure that the components can be reused and extended


### Implementation
 - Code quality - styleguide, linters, review processes,
 - Versioning
 - Stability - unit testing, end-to-end & integration tests, load testing
 - Documentation
   - Data models documentation - what different attributes represent
   - APIs documentation - what the endpoints do, what are the expected inputs and outputs
   - Business logic - why certain decisions were made 
 - Security
   - authentication & authorization
   - data validation & sanitization
   - data protection
   - protection of paid features
 - Monitoring
   - logging
   - metrics

### Deployment & operation
 - Automated deployment - deployment should be as easy as possible and require minimal human interaction
   - Single command deployment
   - Deployment rollback
   - Deployment pipeline
 - Availability monitoring - are you sure your system is running?
 - Metrics reporting - how to measure the system performance
 - Error logging - operation logs should be easy to access and understand
 - Noiseless services - the system should not generate unnecessary noise e.g. logs, emails, notifications as it may hide real problems

### Evolution & maintenance
 - Test before fix - before fixing a bug write a test that reproduces it
 - Evaluate before change - before making a change evaluate the impact on the system
   - (de)coupling with existing codebase
   - Compatibility with existing systems
   - Migration policies
   - Deprecation policies
 - Avoid bloating - avoid creating huge components that do too many things


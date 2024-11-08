## Branching

Branches for the monolith solution, and the micro services are different

For the enterprise solution the branching strategy works as follows:

Master -> Staging -> Develop -> Feature

In practise, this means that to create a feature branch, a branch is created off of develop
Once the feature is completed, it merges to develop

When the develop branch is ready to be tested, it will go to staging, and once released that branch will be promoted to Master

if work completes while you have WIP, merge from staging into develop then into your feature branch.